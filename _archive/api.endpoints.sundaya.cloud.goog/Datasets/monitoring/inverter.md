# monitoring.inverter
---

# Dataset Source

![Inverter Data](../../images/InverterData.png)

# Request Message

The following snippet shows the structure of an `inverter` request:

```json
{
  "datasets": [
    { "inverter": { "id": "SPI-B2-01-001" }, 
      "data": [
        { "time_local": "20190209T150006.032+0700",
          "pv": { "volts": [48.000, 48.000], "amps": [6.0, 6.0] },
          "battery": { "volts" : 55.1, "amps": 0.0 }, 
          "load": { "volts": [48.000, 48.000], "amps": [1.2, 1.2] }, 
          "grid": { "volts": [48.000, 48.000, 48.000], "amps": [1.2, 1.2, 1.2], "pf": [0.92, 0.92, 0.92] }
        },
```

### Message Attributes

The inverter request message attributes are specified below. 

Attribute | Metric | Data | Constraint | Description
--- | --- | --- | --- | ---
`inverter.id` | - | string | - | Id of the Inverter charge controller. *(__Note__: a site can have any number of Inverter controllers, and each controller can have multiple PV strings and Loads)*.
`time_local` | - | datetime | RFC 3339 | The local time of the event which produced this data sample, represented with a mandatory `+/-` offset from UTC for the device's location, in compressed `ISO 8601/RFC3339` (YYYYMMDDThhmmss±hhmm).
`pv.volts` | volts | float *(array)* | *array size 1-4* | An ordered set of Voltage readings for PV strings connected to this Inverter. Each value in the data array applies to a numbered PV string based on its position in the array. For example the 2nd value in the data array is the data for the 2nd PV string. The array size depends on the number of PV strings. Presently upto 4 PV strings per controller are supported. In future each string will have its own dedicated controller.
`pv.amps` | amps | float *(array)* | *array size 1-4* | An ordered set of Current readings for PV strings (corresponding to voltage readings in `pv.volts`).  
`batt.volts` | volts | float | - | The voltage of the connected Battery.
`batt.amps` | amps | float [+/-] | - | The current for the connected Battery. The value is positive for charge current and negative when discharging.
`load.volts` | volts | float *(array)* | *array size 1-2* | An ordered set of Voltage readings for connected Loads. Each value in the data array applies to a Load number based on its position in the array. For example the 2nd value in the data array is the data for the 2nd Load. The array size depends on the number of loads. Each load and its ordinal position must be declared in this API documentation.
`load.amps` | amps | float *(array)* | *array size 1-2* | An ordered set of Current readings for connected Loads (corresponding to values in `load.volts`).  
`grid.volts` | volts | float *(array)* | *array size 1-3* | An ordered set of up to 3 Voltage readings for each phase of the connected grid supply. The array size depends on the number of phases in the supply. If the supply is single-phase there will be only one element in the array.
`grid.amps` | amps | float *(array)* | *array size 1-2* | An ordered set of Current readings for for each phase of the connected grid supply (corresponding to values in `grid.volts` and `grid.pf`).  
`grid.pf` | - | float *(array)* | *array size 1-2, maximum 1.0* | An ordered set of Power Factor readings for each phase of the connected grid supply (corresponding to values in `grid.volts` and `grid.amps`). 

--- 

# Dataset Structure 

While the request message structure described above is optimised to reduce size, the dataset structure is optimised to simplify queries for analytics.

In particular arrays in the request message structure are flattened and transformed into the following dataset structure, which includes additional elements.

- The added timestamps are based on `time_local` sent in the request message, which is replaced by these timestamps.  

- The timestamps are stored in the canonical format used for data storage ('YYYY-MM-DD HH:mm:ss.SSSS') as shown in the examples.

Attribute | Metric | Data | Constraint | Description
--- | --- | --- | --- | ---
`inverter_id` | - | string | - | Id of the Inverter charge controller. This attribute replaces `inverter.id` in the request message.
`pv[]` | - | object *(array)* | - | The `pv` array contains objects which aggregate `pv.volts` and `pv.amps` from the request message.
`pv[].volts` | volts | float | - | The value of `volts` in the `pv` object corresponds to an element in the `pv.volts` request message array.
`pv[].amps` | amps | float | - | The value of `amps` in the `pv` object corresponds to an element in the `pv.amps` request message array.
`pv[].watts` | watts | float | - | The product of `pv.volts` and `pv.amps`.
`battery.volts` | volts | float | - | _(no change from request message)_.
`battery.amps` | amps | float | - | _(no change from request message)_.
`battery.watts` | watts | float | - | The product of `battery.volts` and `battery.amps`.
`load[]` | - | object *(array)* | - | The `load` array contains objects which aggregate `load.volts` and `load.amps` in the request message.
`load[].volts` | volts | float | - | The value of `volts` in the `load` object corresponds to an element in the `load.amps` request message array.
`load[].amps` | amps | float | - | The value of `amps` in the `load` object corresponds to an element in the `load.amps` request message array.
`load[].nn_watts` | watts | float | - | The product of `load.volts` and `load.amps`.
`grid_nn_volts` | volts | float | - | The element number corresponding to nn in `grid.volts`.
`grid_nn_amps` | amps | float | - | The element number corresponding to nn in `grid.amps`.
`grid_nn_pf` | amps | float | *maximum 1.0* | The element number corresponding to nn in `grid.pf`.
`grid_nn_watts` | watts | float | - | Calculated for each supply phase, based on the formula: `grid.watts` = `grid.volts` * `grid.amps` * `grid.pf` * `√3`.
`sys.source` | - | string | - | The identifier of the data sender, based on the API key sent in the request header. The value is a foreign key to the `system.source` dataset table.
`time_event` | - | datetime | - | The UTC time of the event which produced this data sample.
`time_local` | - | datetime | - | The local time of the event which produced this data sample. Note that the timezone offset is discarded.
`time_processing` | - | datetime | - | The UTC time when the request was received and *processed* on the API host.


The transformed JSON structure which is sent to the message broker at the first stage of processing the `dataset/pms` POST message, and which is used to load data into the datawarehouse, is shown in the followng sample:

```
*** MESSAGE ***
Topic: inverter
Key: SPI-B2-01-001
Value:	
```

```json
{
    "inverter_id":"SPI-B2-01-002",
    "pv": [
        {"volts": 48, "amps": 6, "watts": 288 },
        {"volts": 48, "amps": 6, "watts": 288 } ],
    "battery": {"volts": 55.1, "amps": 0.0, "watts": 0 },
    "load": [
        { "volts": 48, "amps": 1.2, "watts": 57.6 },
        { "volts": 48, "amps": 1.2, "watts": 57.6 } ],
    "grid_01": {"volts": 48, "amps": 1.2, "pf": 0.92, "watts": 91.785 },
    "grid_02": {"volts": 48, "amps": 1.2, "pf": 0.92, "watts": 91.785 },
    "grid_03": {"volts": 48, "amps": 1.2, "pf": 0.92, "watts": 91.785 },
    "sys": {"source": "S000" },
    "time_event":"2019-02-09 08:00:17.0220",
    "time_local":"2019-02-09 15:00:17.0220",
    "time_processing":"2019-09-10 04:11:09.2930"
},
```

### Partitions and Clustering

__inverter__ dataset tables are partitioned based on `time_local` and clustered by `inverter_id`.
