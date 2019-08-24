# monitoring.inverter Dataset
---

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
          "battery": { "volts" : 55.1 }, 
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

The following attributes are prepended to request message attributes at the first stage of processing the `/devices` POST request. 

The added timestamps are based on `time_local` sent in the request message, which is replaced by these timestamps.  

The dataset timestamps are stored in the canonical timestamp format used for data storage ('YYYY-MM-DD HH:mm:ss.SSSS') as shown in the examples.

Attribute | Metric | Data | Constraint | Description
--- | --- | --- | --- | ---
`id` | - | string | - | Id of the Inverter charge controller. This attribute replaces `inverter.id` in the request message.
`time_utc` | - | datetime | - | The UTC time of the event which produced this data sample.
`time_local` | - | datetime | - | The local time of the event which produced this data sample. Note that the timezone offset is discarded.
`time_processing` | - | datetime | - | The UTC time when the request was received and *processed* on the API host.

The dataset structure sent to the message broker at the first stage of processing is shown in the followng example:

```
*** MESSAGE ***
Topic: inverter
Key: SPI-B2-01-001
Value:	
```

```json
{ 
    "id": "SPI-B2-01-001",
    "time_utc": "2019-02-09 09:30:00.0200",
    "time_local": "2019-02-09 16:30:00.0200",
    "time_processing":"2019-02-09 09:31:05.0110",
    "pv": { "volts": [48.000, 48.000], "amps": [6.0, 6.0], "watts": 288.01 },
    "battery": { "volts" : 55.1 }, 
    "load": { "volts": [48.000, 48.000], "amps": [1.2, 1.2], "watts": 57.60 },
    "grid": { "volts": [48.000, 48.000, 48.000], "amps": [1.2, 1.2, 1.2], "pf": [0.92, 0.92, 0.92], "watts": [91.782, 91.782, 91.782] }
},
```

### Derived Values

The value of `watts` is calculated for each supply phase, based on the following formula:

    `grid.watts` = `grid.volts` * `grid.amps` * `grid.pf` * `√3`