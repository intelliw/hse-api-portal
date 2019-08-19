# System Overview
---

The Sundaya Device and Data Management platform consists of the following core components:

### Data Collection

1. **Trackable Devices** - _PMS_, _MPPT_, and _Inverters_ which continuously produce monitoring data.

2. **Device Controllers** - such as _BBC_ and _EHub Gateways_, which collect and upload data through an API.

3. **Trilateral API** - synchronous _Command/Query_, and asynchronous _Publish_ and _Subscribe_ API interfaces.

![Platform Devices](../images/platform-devices.jpg)

### Data Management

4. **Data Pipeline** - _Message Broker_ cluster, and real-time ingest and query _Analytics Engine_.

5. **Data Storage** - _Data Warehouse_ for SQL analytics (technical users), deep storage, view materialisation, and data retention management.

6. **Data Visualisation** - _Analytics Engine_ and _BI Dashboard_ for business intelligence reports and ad-hoc queries by business users.

![Real-Time Analytics](../images/platform-backend.jpg)

---