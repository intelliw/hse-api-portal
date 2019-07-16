# Standards & Conventions
---

## Versions
The API endpoint host is [http://api.endpoints.sundaya.cloud.goog](http://api.endpoints.sundaya.cloud.goog). 

All requests to the API endpoint receive the latest version of the API.     

Client applications may request a specific version through the `Accept` header.

    Accept: application/vnd.sundaya.v1.0+yaml

## Date-time Format
Date and time parameters must be expressed in [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format and must conform to [RFC3359](https://tools.ietf.org/html/rfc3339) .

    http://api.endpoints.sundaya.cloud.goog/energy/{type}/{period}/{epoch}

e.g. [http:/api.endpoints.sundaya.cloud.goog/energy/hse/period/week/20190210](http:/api.endpoints.sundaya.cloud.goog/energy/hse/period/week/20190210)

The compressed version of ISO 8601 is required, without semi colons and with `T` as the time designator, as shown in examples below.

## Timezones
Timezones are not assumed and must be explicitly specified where API parameters allow for a timestamp to be provided. 

The Timezone can be specified in UTC or local time as shown:

- __UTC__, expressed with a trailing `Z` 

    e.g. [http://api.endpoints.sundaya.cloud.goog/energy/hse/period/minute/20190209T0930Z](http://api.endpoints.sundaya.cloud.goog/energy/hse/period/minute/20190209T0930Z "Z signifies time zone as UTC") == 09:30 UTC

- __Local__ time in Jakarta with +/- offset 

    http://api.endpoints.sundaya.cloud.goog/energy/hse/period/minute/YYYYMMDDTHHmmss.SSS±HHmm

    e.g. [http://api.endpoints.sundaya.cloud.goog/energy/hse/period/minute/20190209T1630-0700](http://api.endpoints.sundaya.cloud.goog/energy/hse/period/minute/20190209T1630-0700 "-0700 is JKT offset from  UTC") == 09:30 UTC

## Media types
Request `Body` parameters and all response objects are sent and received in JSON. 

Clients should specify and consume `Accept` and `Content-Type` request and response headers in their applications. This ensures that an expected response is received, even as new media types or hypermedia schemes are introduced and designated as default in future.

These media types are currently supported in requests with an `Accept` header:

    application/vnd.collection+json
    application/json 
    text/html
    text/plain

- If an `Accept` header is *not* specified (or is wildcarded with '*/*') the default `application/vnd.collection+json` media type will be returned. 

- If multiple `Accept` headers are sent the response will select the first matching media type in the list shown above, in the order shown.

- If the request `Accept` headers do not contain a type from the list above a `415`response (*Unsupported Media Type*) will be returned.


## Headers
This following example shows a sample HTTP request and response.
```
*** REQUEST ***	
GET /energy/hse/period/week/20190204/ HTTP/1.1	
Host: api.endpoints.sundaya.cloud.goog
Accept: application/vnd.collection+json	
api_key: X2zaSyASFGxf4PmOitVS1Dt911PcZ4IQ8PUUMqA
    
*** RESPONSE ***	
200 OK HTTP/1.1	
Content-Type: application/vnd.collection+json	
Content-Length: 10757	
    
[{ "collection": {...}, ... }]
```
 

## Operations
The API supports basic CRUD operations (create, read, update, and delete) using standard HTTP method requests, as summarized in the following table.

Operation | Definition
--- | --- 
`GET` | Retrieve information about the resource.
`POST` | Create, backup, or restore the resource.
`PUT` | Update the resource.
`DELETE` | Delete the resource. 

## Response codes
The API supports a limited set of responses for each API path, based on the following.

Code | Status | Definition
--- | --- | ---
`200` | OK | Data retrieved. 
`201` | Created | Resource created.
`400` | Bad Request | The client specified an invalid argument. 
`401` | Unauthorized | The client does not have sufficient permission. 
`404` | Not Found | The resource was not found.
`415` | Unsupported Media Type | The requested Accept header type is not supported.
`500` | Internal Server Error | The server encountered an unexpected condition.

---