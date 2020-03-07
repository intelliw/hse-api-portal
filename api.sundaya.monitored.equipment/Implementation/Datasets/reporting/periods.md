
# reporting.periods
---

The **periods** dataset contains period-aligned tranforms of monitoring data received through the _devices/datasets_ POST API.

The dataset contains the following data:

- **Energy data** - period-aligned energy data aggregates.

- **Monitoring data** - raw monitoring data, the same data is stored in the `analytics` OLAP repository, but replicated here in `reporting` for fast OLTP access.



### Repository types

Storage for this dataset may be provided by either of the following repository technologies:

- a Wide-column key-value repository for very high scale and performance.
- a Document database for low cost.

The equivalent schema elements and recommended value for the above repository types are shown below.

Wide-column repo.       | Document db.              | Recommended Value
---                     | ---                       | ---
Instance ID             |                           | `reporting`
Table name              |                           | `periods`
Column Families         | Kind                      | _`<period_name>`_
Row Id                  | Ancestry<br>Entity ID     | _`<device_type>#<device_id>#<YYYYMMDDHHmm>`_<br>_`<device_id>#<YYYYMMDDHHmm>`_
Column Qualifier        | Property                  | _see below_



### Column families

Column familes are based on categorical period_names as summarised in the table below. 

The table also lists the type of data contained in each column family.  

Note that the `SECOND` period is not applicable and therefore does not have a column family. 

This is because the smallest aggregation period for a row is a 1 minute.

Column family   | Data
---             | ---| 
`INSTANT`       | **monitoring**
`MINUTE`<br>`QTRHOUR`<br>`HOUR`<br>`TIMEOFDAY`<br>`DAY`<br>`WEEK`<br>`MONTH`<br>`QUARTER`<br>`YEAR`<br>`FIVEYEAR` | **energy**<br><br><br><br><br><br><br><br>

Every row has an `INSTANT` _column family_ which contains **monitoring** data. 

All column families other than `INSTANT` contain **energy** data.

Every row has a `MINUTE` _column family_ as each row is exclusively scoped to 1 minute. 

- The `MINUTE` column family contains **energy** data aggregates for the minute indicated by the row id (_YYYYMMDDHHmm_).

The rest of the _column families_ will be present in a row only if the date-time component of the row id (_YYYYMMDDHHmm_) coincides with the period epoch (the start) of the period. 

- For example a row with an id of **PMS-01-006#202002091500** will have _column families_ for `HOUR` and `MINUTE` as the date-time in the id (**1500**) coincides with the epoch (start) of an hour and minute period.

- Similarly a row with an id of **PMS-01-006#202002090000** will have _column families_ for `DAY`, `HOUR`, and `TIMEOFDAY` as the date-time in the id (**090000**) coincides with the start of all three periods.




---

### Monitoring columns

Monitoring data is stored in the `INSTANT` _column family_.

Monitoring _column qualifiers_ are different for each device type (based on `<device_type>` in the row id) as shown in the table below.


PMS qualifiers  | MPPT qualifiers   | Inverter qualifiers
---             | ---               | ---   
`pms_id`<br>`sender`<br>`time_zone`<br>`time_processing`<br>`dataitem`<br>`pack_id`<br>`pack_volts`<br>`pack_amps`<br>`pack_watts`<br>`pack_vcl`<br>`pack_vch`<br>`pack_dock`<br>`pack_temp_top`<br>`pack_temp_mid`<br>`pack_temp_bottom` | `mppt_id`<br>`sender`<br>`time_zone`<br>`time_processing`<br>`dataitem`<br><br><br><br><br><br><br><br><br><br> | `inverter_id`<br>`sender`<br>`time_zone`<br>`time_processing`<br>`dataitem`<br><br><br><br><br><br><br><br><br><br>

`time_event` is stored for each data element in the cell _timestamp_ property.  

The `dataitem` column contains a complete monitoring message including the cell _timestamp_, as described in the following `analytics` dataset pages.

- _[pms_monitoring](/docs/api.sundaya.monitored.equipment/0/c/Implementation/Datasets/analytics/pms_monitoring)_
- _[mppt_monitoring](/docs/api.sundaya.monitored.equipment/0/c/Implementation/Datasets/analytics/mppt_monitoring)_
- _[inverters_monitoring](/docs/api.sundaya.monitored.equipment/0/c/Implementation/Datasets/analytics/inverter_monitoring)_




---

### Energy columns

Energy _column qualifiers_ are closely aligned to the [Energy API response](/docs/api.sundaya.monitored.equipment/0/c/Examples/GET/energy%20GET%20example).

The _columnn qualifiers_ are different for each device type (based on `<device_type>` in the row id) as shown in the table below. 


PMS qualifiers  | MPPT qualifiers   | Inverter qualifiers
---             | ---               | ---
`pack_in_joules`<br>`pack_out_joules`<br><br><br><br><br><br><br><br><br><br><br><br><br>            | `battery_in_joules`<br>`battery_out_joules`<br>`pv_1_joules`<br>`pv_2_joules`<br>`pv_3_joules`<br>`pv_4_joules`<br>`load_1_joules`<br>`load_2_joules`<br><br><br><br><br><br><br>               | `battery_in_joules`<br>`battery_out_joules`<br>`pv_1_joules`<br>`pv_2_joules`<br>`pv_3_joules`<br>`pv_4_joules`<br>`load_1_joules`<br>`load_2_joules`<br>`grid_1_in_joules`<br>`grid_1_out_joules`<br>`grid_2_in_joules`<br>`grid_2_out_joules`<br>`grid_3_in_joules`<br>`grid_3_out_joules`



--- 