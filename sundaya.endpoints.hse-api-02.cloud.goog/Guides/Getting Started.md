# Getting Started
---

### Creating an API key
1. [Create an API key](https://console.developers.google.com/apis/credentials) in the Google APIs Console.
2. Click **Create credentials**, then select **API key**.
3. Copy the key.
4. Click **Close**.

### Using the API

Browse the reference section of this site to see examples of what you can do with this API and how to use it. You can use the **Try this API** tool on the right side of an API method page to generate a sample request.

# Introduction
The HSE Energy Management API is based on REST / Hypermedia and specified in [OpenAPI v2.0](https://github.com/OAI/OpenAPI-Specification/blob/master/versions/2.0.md). 

The API provides energy metrics for four **Flow** types:`harvest`, `store`, `enjoy`, `grid`. 

The API response consolidates all four energy flow types based on a period (week, month etc.).

- Clients can use the API to manage **Energy Assets** through graphical views and by scheduling energy use at preferred times.

- Vendor device integrations can use the API to monitor and control their **Energy Management Devices**.

Energy Type | Energy Assets | Energy Management Devices
--- | --- | ---
`harvest` | Renewables | PV Modules, PV Grid-interactive Inverter
`store` | Storage | Busbar Controler (BBC), Pack Management System (PMS)
`enjoy` | Appliances | Multicore-Cable Current Sensors, Clamp-on Current Sensors
`grid` | Mains Electricity | Smart Meters

The API and documentation is available through the *Sundaya Developer Portal* at https://developer.sundaya.com. 

# Overview

## Data element names

The following provides names of all data elements used in the API, in the context of each flow. 

- `store.in` and `store.out` indicate *charge* and *discharge* flows for batteries.

- `grid.out` and `grid.in` indicate mains use, and feed-in flows into the public grid.

- `harvest` indicates renewable generation and always implies `.out`. 

- `enjoy` indicates energy use and always implies `.in`. 

## Double-entry format 

Energy flows are based on a "double entry" format (each flow has an opposite flow). 

These equal and opposite flows are summarised in the following table: 

Flow | From-To   
--- |---
`harvest` |`store.in` `enjoy` `grid.in`
`store.out` | `enjoy`
`enjoy`  |  `harvest` `store.out` `grid.out`
    
To query specific assets, clients can filter requests by `category`, `subcategory`, and `product-type` (in the request *Body*).


## Versions
The API endpoint host is http://api.sundaya.com. 

All requests to the API endpoint receive the latest version of the API.     

Client applications may request a specific version through the `Accept` header.

    Accept: application/vnd.sundaya.v1+yaml

## Date-time Format
Date and time parameters must be expressed in [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format and must conform to [RFC3359](https://tools.ietf.org/html/rfc3339) .

    http://api.sundaya.com/energy/{energyTpe}/period/{periodType}/{endDateTime}

e.g. http:/api.sundaya.com/energy/hse/period/week/20190210

The compressed version of ISO 8601 is required, without semi colons and with `T` as the time designator, as shown in examples below.


## Timezones
Timezones are not assumed and must be explicitly specified where API parameters allow for a timestamp to be provided. 

The Timezone can be specified in UTC or local time as shown:

- __UTC__, expressed with a trailing `Z` 

    e.g. http://api.sundaya.com/energy/hse/period/minute/20190209T0930Z == 09:30 UTC

- __Local__ time in Jakarta with offset 

    http://api.sundaya.com/energy/hse/period/week/YYYYMMDDThhmmss±hhmm
    e.g. http://api.sundaya.com/energy/hse/period/minute/20190209T1630-0700 == 09:30 UTC
## Media types
Request `Body` parameters and all response objects are sent and received in JSON. 

Clients should use `Accept` and `Content-Type` headers to preserve backward compatibility (in case a new media type or hypermedia scheme is introduced and designated as default).

These media types are supported:

    application/json 
    application/vnd.collection+json

## Headers
This following example shows a sample HTTP request and response.
```
*** REQUEST ***	
GET /energy/hse/period/week/20190210/ HTTP/1.1	
Host: api.sundaya.com	
Accept: application/vnd.collection+json	
    
*** RESPONSE ***	
200 OK HTTP/1.1	
Content-Type: application/vnd.collection+json	
Content-Length: xxx	
    
{ "collection" : {...}, ... }
```

## Link-relation types
Link-relations in Response objects are based on [RFC8288](https://tools.ietf.org/html/rfc8288#page-6). 

The following registered types are referenced in the `rel` attribute of the links in an `application/vnd.collection+json` response. 
- **self**	- Identifies the link"s context.

    In `collection.links` it identifies the collection (name = *week*)            

    - e.g. href=<a>http:/api.sundaya.com/energy/hse/period/week/20190210</a>

    In `collection.items.links` it identifies an item in the collection (name = *day*).
    - e.g. href=<a>http:/api.sundaya.com/energy/hse/period/day/20190204</a>

- **collection** - in `collection.links` it targets the item series whiich make up the collection (name = *week.days*).
    
    - e.g. href=<a>http:/api.sundaya.com/energy/hse/interval/day/20190204/20190210</a>

- **item** - in `collection.items.links` it targets subitems of the item in that context (name = *day.hours*).

    - e.g. href=<a>http:/api.sundaya.com/energy/hse/interval/hour/201902050600/201902050500</a>

- **up** - Identifies the parent the collection or item represented by the link"s context (name = *week.month*).
    
- **next** - Identifies the next sibling of the collection or item series represented by the link"s context (name = *week.next*).

- **prev** - Identifies the previous siblings of the collection or item series represented by the link"s context (name = *week.previous*).
    
