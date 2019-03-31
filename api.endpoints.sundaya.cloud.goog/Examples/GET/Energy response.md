# Energy
---

### GET response - HSE

[/energy/hse/periods/week/20190204/1?site=999](http:/api.endpoints.sundaya.cloud.goog/energy/hse/periods/week/20190204/1?site=999)

```
*** REQUEST ***	
GET /energy/hse/periods/week/20190204/1?site=999 HTTP/1.1	
Host: api.endpoints.sundaya.cloud.goog
Accept: application/vnd.collection+json, application/vnd.sundaya.v1.0+yaml
    
*** RESPONSE ***	
200 OK HTTP/1.1	
Content-Type: application/vnd.collection+json	
Content-Length: 3495	

```


```json
[
  {
    "collection": {
        "version": "0.2",
        "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/periods/week/20190304/1?site=999",
        "links": [
          { "rel": "self", "name": "week", "prompt": "Week 10 2019", "title": "04/03/19 - 10/03/19",
            "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/periods/week/20190304/1?site=999", "render": "link" 
          },
          { "rel": "collection", "name": "week.day", "prompt": "Mon Mar 4th - Sun Mar 10th", "title": "04/03/19 - 10/03/19",
            "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/periods/day/20190304/7?site=999" 
          },
          { "rel": "collection", "name": "week.day.timeofday", "prompt": "Mar 4 Night - Mar 10 Evening", "title": "04/03/19 00:00 - 10/03/19 23:59",
            "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/periods/timeofday/20190304T0000/28?site=999" 
          },
          { "rel": "up", "name": "month", "prompt": "Mar 2019", "title": "01/03/19 - 31/03/19",
            "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/periods/month/20190301/1?site=999", "render": "link" 
          },
          { "rel": "next", "name": "week", "prompt": "Week 11 2019", "title": "11/03/19 - 17/03/19",
            "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/periods/week/20190311/1?site=999", "render": "link" 
          },
          { "rel": "prev", "name": "week", "prompt": "Week 09 2019", "title": "25/02/19 - 03/03/19",
            "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/periods/week/20190225/1?site=999", "render": "link" 
          }
        ],
        "items": [
        { "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/periods/day/20190304/1?site=999",
          "links": [
            { "rel": "self", "name": "day", "prompt": "Mon Mar 4th", "title": "04/03/19",
              "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/periods/day/20190304/1?site=999", "render": "link" 
            },
            { "rel": "collection", "name": "day.timeofday", "prompt": "Mar 4 Night - Mar 4 Evening", "title": "04/03/19 00:00 - 04/03/19 23:59",
              "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/periods/timeofday/20190304T0000/4?site=999" 
            }
          ],          
           "data": [
            { "name": "day", "value": "20190304/1",
              "data": [
                { "name": "harvest", "value": "66.22849" },
                { "name": "store.in", "value": "58.514396" },
                { "name": "store.out", "value": "68.799968" },
                { "name": "enjoy", "value": "11.50717" },
                { "name": "grid.in", "value": "64.885491" },
                { "name": "grid.out", "value": "37.994182" }
              ]
            },
            { "name": "day.timeofday", "value": "20190304T0000/4",
              "data": [
                { "name": "harvest", "value": "3.176898 7.2012 15.628647 10.042905" },
                { "name": "store.in", "value": "13.129662 13.186528 16.55937 8.149107" },
                { "name": "store.out", "value": "12.975158 11.931583 12.944902 20.53711" },
                { "name": "enjoy", "value": "8.477666 17.046609 16.842825 4.249814" },
                { "name": "grid.in", "value": "11.766934 7.712132 10.934318 20.614763" },
                { "name": "grid.out", "value": "14.374344 12.54626 5.215394 20.051709" }
              ]
            }
          ]
        },
        { "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/periods/day/20190305/1?site=999",
          "links": [
            { "rel": "self", "name": "day", "prompt": "Tue Mar 5th", "title": "05/03/19",
              "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/periods/day/20190305/1?site=999", "render": "link" 
            },
            { "rel": "collection", "name": "day.timeofday", "prompt": "Mar 5 Night - Mar 5 Evening", "title": "05/03/19 00:00 - 05/03/19 23:59",
              "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/periods/timeofday/20190305T0000/4?site=999" 
            }
          ],          
           "data": [
            { "name": "day", "value": "20190305/1",
              "data": [
                { "name": "harvest", "value": "26.436251" },
                { "name": "store.in", "value": "63.909699" },
                { "name": "store.out", "value": "12.457034" },
                { "name": "enjoy", "value": "59.145589" },
                { "name": "grid.in", "value": "82.166283" },
                { "name": "grid.out", "value": "55.174077" }
              ]
            },
            { "name": "day.timeofday", "value": "20190305T0000/4",
              "data": [
                { "name": "harvest", "value": "20.615137 7.326639 12.46651 9.254191" },
                { "name": "store.in", "value": "8.564526 10.939749 11.391637 7.367083" },
                { "name": "store.out", "value": "19.796106 10.931281 16.385781 3.157805" },
                { "name": "enjoy", "value": "9.741077 6.190103 18.031921 17.934737" },
                { "name": "grid.in", "value": "3.191509 18.346396 16.372902 19.490546" },
                { "name": "grid.out", "value": "7.132912 9.320653 6.571962 15.075899" }
              ]
            }
          ]
        },
        { "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/periods/day/20190306/1?site=999",
          "links": [
            { "rel": "self", "name": "day", "prompt": "Wed Mar 6th", "title": "06/03/19",
              "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/periods/day/20190306/1?site=999", "render": "link" 
            },          
            { "rel": "collection", "name": "day.timeofday", "prompt": "Mar 6 Night - Mar 6 Evening", "title": "06/03/19 00:00 - 06/03/19 23:59",
              "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/periods/timeofday/20190306T0000/4?site=999" 
            }
          ],          
           "data": [
            { "name": "day", "value": "20190306/1",
              "data": [
                { "name": "harvest", "value": "30.926496" },
                { "name": "store.in", "value": "74.783501" },
                { "name": "store.out", "value": "32.297718" },
                { "name": "enjoy", "value": "34.386959" },
                { "name": "grid.in", "value": "79.446243" },
                { "name": "grid.out", "value": "44.384287" }
              ]
            },
            { "name": "day.timeofday", "value": "20190306T0000/4",
              "data": [
                { "name": "harvest", "value": "18.391145 19.950918 9.293566 6.706101" },
                { "name": "store.in", "value": "18.652257 10.304759 18.669559 20.573746" },
                { "name": "store.out", "value": "20.21856 14.617149 9.202237 17.11726" },
                { "name": "enjoy", "value": "6.472653 5.783513 10.16323 12.631774" },
                { "name": "grid.in", "value": "8.522498 8.621227 20.553783 8.711874" },
                { "name": "grid.out", "value": "12.702724 4.628987 17.164084 15.074929" }
              ]
            }
          ]
        },
        { "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/periods/day/20190307/1?site=999",
          "links": [
            { "rel": "self", "name": "day", "prompt": "Thu Mar 7th", "title": "07/03/19",
              "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/periods/day/20190307/1?site=999", "render": "link" 
            },          
            { "rel": "collection", "name": "day.timeofday", "prompt": "Mar 7 Night - Mar 7 Evening", "title": "07/03/19 00:00 - 07/03/19 23:59",
              "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/periods/timeofday/20190307T0000/4?site=999" 
            }
          ],          
           "data": [
            { "name": "day", "value": "20190307/1",
              "data": [
                { "name": "harvest", "value": "15.444935" },
                { "name": "store.in", "value": "62.301678" },
                { "name": "store.out", "value": "47.274096" },
                { "name": "enjoy", "value": "14.127181" },
                { "name": "grid.in", "value": "80.53107" },
                { "name": "grid.out", "value": "74.244653" }
              ]
            },
            { "name": "day.timeofday", "value": "20190307T0000/4",
              "data": [
                { "name": "harvest", "value": "10.703824 9.914132 17.000571 9.897278" },
                { "name": "store.in", "value": "7.60888 5.212308 18.386099 3.628459" },
                { "name": "store.out", "value": "11.347071 9.069319 9.991322 14.170555" },
                { "name": "enjoy", "value": "19.390523 7.634764 15.970957 14.710604" },
                { "name": "grid.in", "value": "14.105133 12.056239 6.095306 11.818765" },
                { "name": "grid.out", "value": "15.580144 12.738289 15.42021 13.406179" }
              ]
            }
          ]
        },
        { "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/periods/day/20190308/1?site=999",
          "links": [
            { "rel": "self", "name": "day", "prompt": "Fri Mar 8th", "title": "08/03/19",
              "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/periods/day/20190308/1?site=999", "render": "link" 
            },
            { "rel": "collection", "name": "day.timeofday", "prompt": "Mar 8 Night - Mar 8 Evening", "title": "08/03/19 00:00 - 08/03/19 23:59",
              "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/periods/timeofday/20190308T0000/4?site=999" 
            }
          ],          
           "data": [
            { "name": "day", "value": "20190308/1",
              "data": [
                { "name": "harvest", "value": "12.719724" },
                { "name": "store.in", "value": "73.263752" },
                { "name": "store.out", "value": "38.71842" },
                { "name": "enjoy", "value": "23.884102" },
                { "name": "grid.in", "value": "52.534576" },
                { "name": "grid.out", "value": "31.597264" }
              ]
            },
            { "name": "day.timeofday", "value": "20190308T0000/4",
              "data": [
                { "name": "harvest", "value": "18.729289 17.914527 20.059188 8.140313" },
                { "name": "store.in", "value": "9.924167 5.087406 8.770273 9.617282" },
                { "name": "store.out", "value": "5.675334 19.075555 16.116441 19.688873" },
                { "name": "enjoy", "value": "13.133929 15.522048 5.122403 7.841037" },
                { "name": "grid.in", "value": "11.502622 3.11603 15.729893 17.543545" },
                { "name": "grid.out", "value": "8.100806 9.409088 3.73809 20.159826" }
              ]
            }
          ]
        },
        { "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/periods/day/20190309/1?site=999",
          "links": [
            { "rel": "self", "name": "day", "prompt": "Sat Mar 9th", "title": "09/03/19",
              "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/periods/day/20190309/1?site=999", "render": "link" 
            },
            { "rel": "collection", "name": "day.timeofday", "prompt": "Mar 9 Night - Mar 9 Evening", "title": "09/03/19 00:00 - 09/03/19 23:59",
              "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/periods/timeofday/20190309T0000/4?site=999" 
            }
          ],          
           "data": [
            { "name": "day", "value": "20190309/1",
              "data": [
                { "name": "harvest", "value": "74.552949" },
                { "name": "store.in", "value": "68.642359" },
                { "name": "store.out", "value": "74.137932" },
                { "name": "enjoy", "value": "11.864298" },
                { "name": "grid.in", "value": "29.030307" },
                { "name": "grid.out", "value": "23.022573" }
              ]
            },
            { "name": "day.timeofday", "value": "20190309T0000/4",
              "data": [
                { "name": "harvest", "value": "14.382511 9.487058 9.232671 7.22704" },
                { "name": "store.in", "value": "4.707961 18.4667 17.184756 16.477832" },
                { "name": "store.out", "value": "12.762247 9.276065 14.986351 15.378647" },
                { "name": "enjoy", "value": "9.705695 6.837791 6.804945 4.925647" },
                { "name": "grid.in", "value": "9.709284 17.573599 8.243218 3.082698" },
                { "name": "grid.out", "value": "16.157007 16.682969 14.981557 12.980072" }
              ]
            }
          ]
        },
        { "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/periods/day/20190310/1?site=999",
          "links": [
            { "rel": "self", "name": "day", "prompt": "Sun Mar 10th", "title": "10/03/19",
              "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/periods/day/20190310/1?site=999", "render": "link" 
            },
            { "rel": "collection", "name": "day.timeofday", "prompt": "Mar 10 Night - Mar 10 Evening", "title": "10/03/19 00:00 - 10/03/19 23:59",
              "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/periods/timeofday/20190310T0000/4?site=999" 
            }
          ],          
           "data": [
            { "name": "day", "value": "20190310/1",
              "data": [
                { "name": "harvest", "value": "48.782865" },
                { "name": "store.in", "value": "25.013671" },
                { "name": "store.out", "value": "81.93385" },
                { "name": "enjoy", "value": "31.095812" },
                { "name": "grid.in", "value": "78.628968" },
                { "name": "grid.out", "value": "25.389898" }
              ]
            },
            { "name": "day.timeofday", "value": "20190310T0000/4",
              "data": [
                { "name": "harvest", "value": "2.875021 14.529194 7.434935 8.899906" },
                { "name": "store.in", "value": "5.782927 15.90789 3.302618 14.765098" },
                { "name": "store.out", "value": "14.352198 8.286343 13.003692 13.351521" },
                { "name": "enjoy", "value": "14.479015 20.074154 7.317592 14.283507" },
                { "name": "grid.in", "value": "6.1719 18.515942 16.878188 5.766506" },
                { "name": "grid.out", "value": "9.734833 8.137267 17.634835 10.106176" }
              ]
            }
          ]
        }
      ] 
    }
  }
]
  ```
