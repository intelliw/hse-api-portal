# Energy
---

### GET /energy response

[/energy/hse/period/week/20190204/1](http://api.endpoints.sundaya.cloud.goog/energy/hse/period/week/20190204/1?site=999)


```    
*** RESPONSE ***	
200 OK HTTP/1.1	
Content-Type: application/vnd.collection+json	
Content-Length: 3495	
```

```json
[
  {
    "collection": {
      "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/period/week/20190204/1?site=999",
      "version": "0.2",
      "links": [
        { "rel": "self", "name": "week", "prompt": "Week 06 2019", 
          "title": "04/02/19 - 10/02/19", "description": "hse",
          "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/period/week/20190204/1?site=999", 
          "render": "link"
        },
        { "rel": "collection", "name": "week.day", "prompt": "Mon Feb 4th - Sun Feb 10th", 
          "title": "04/02/19 - 10/02/19", "description": "Mon Tue Wed Thu Fri Sat Sun",
          "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/period/day/20190204/7?site=999"
        },
        { "rel": "collection", "name": "day.timeofday", "prompt": "Feb 4 Night - Feb 10 Evening", 
          "title": "04/02/19 00:00 - 10/02/19 23:59", "description": "Morning Afternoon Evening Night",
          "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/period/timeofday/20190204T0000/28?site=999"
        },
        { "rel": "up", "name": "month", "prompt": "Feb 2019", "title": "01/02/19 - 28/02/19",
          "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/period/month/20190201/1?site=999",
          "render": "link"
        },
        { "rel": "next", "name": "week", "prompt": "Week 07 2019", "title": "11/02/19 - 17/02/19",
          "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/period/week/20190211/1?site=999",
          "render": "link"
        },
        { "rel": "prev", "name": "week", "prompt": "Week 05 2019", "title": "28/01/19 - 03/02/19",
          "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/period/week/20190128/1?site=999",
          "render": "link"
        }
      ],
      "items": [
        { "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/period/day/20190204/1?site=999",
          "links": [
            { "rel": "self", "name": "day", "prompt": "Mon Feb 4th", "title": "04/02/19",
              "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/period/day/20190204/1?site=999",
              "render": "link"
            },
            { "rel": "collection","name": "day.timeofday", "prompt": "Feb 4 Night - Feb 4 Evening",
              "title": "04/02/19 00:00 - 04/02/19 23:59", 
              "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/period/timeofday/20190204T0000/4?site=999"
            }
          ],
          "data": [
            { "name": "day", "value": "20190204/1",
              "data": [
                { "name": "harvest", "value": "42.343" },
                { "name": "store.in", "value": "57.695" },
                { "name": "store.out", "value": "54.046" },
                { "name": "enjoy", "value": "31.117" },
                { "name": "grid.in", "value": "37.646" },
                { "name": "grid.out", "value": "39.620" }
              ]
            },
            { "name": "day.timeofday", "value": "20190204T0000/4",
              "data": [
                { "name": "harvest", "value": "9.850 8.610 8.546 15.337" },
                { "name": "store.in", "value": "18.894 17.784 18.056 2.961" },
                { "name": "store.out", "value": "5.501 11.502 20.281 16.762" },
                { "name": "enjoy", "value": "6.933 7.893 11.819 4.472" },
                { "name": "grid.in", "value": "7.878 5.242 19.804 4.722" },
                { "name": "grid.out", "value": "15.968 9.152 9.046 5.454" }
              ]
            }
          ]
        },
        { "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/period/day/20190205/1?site=999",
          "links": [
            { "rel": "self", "name": "day", "prompt": "Tue Feb 5th", "title": "05/02/19",
              "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/period/day/20190205/1?site=999",
              "render": "link"
            },
            { "rel": "collection", "name": "day.timeofday", "prompt": "Feb 5 Night - Feb 5 Evening",
              "title": "05/02/19 00:00 - 05/02/19 23:59", 
              "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/period/timeofday/20190205T0000/4?site=999"
            }
          ],
          "data": [
            { "name": "day", "value": "20190205/1",
              "data": [
                { "name": "harvest", "value": "49.723" },
                { "name": "store.in", "value": "54.910" },
                { "name": "store.out", "value": "62.107" },
                { "name": "enjoy", "value": "47.133" },
                { "name": "grid.in", "value": "53.736" },
                { "name": "grid.out", "value": "26.970" }
              ]
            },
            { "name": "day.timeofday", "value": "20190205T0000/4",
              "data": [
                { "name": "harvest", "value": "9.695 10.039 13.514 16.475" },
                { "name": "store.in", "value": "13.306 17.020 17.867 6.717" },
                { "name": "store.out", "value": "18.423 18.045 19.547 6.092" },
                { "name": "enjoy", "value": "9.838 6.235 10.747 20.313" },
                { "name": "grid.in", "value": "5.371 15.965 20.025 12.375" },
                { "name": "grid.out", "value": "2.981 4.699 14.417 4.873" }
              ]
            }
          ]
        },
        { "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/period/day/20190206/1?site=999",
          "links": [
            { "rel": "self", "name": "day", "prompt": "Wed Feb 6th", "title": "06/02/19",
              "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/period/day/20190206/1?site=999",
              "render": "link"
            },
            { "rel": "collection", "name": "day.timeofday", "prompt": "Feb 6 Night - Feb 6 Evening",
              "title": "06/02/19 00:00 - 06/02/19 23:59", 
              "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/period/timeofday/20190206T0000/4?site=999"
            }
          ],
          "data": [
            { "name": "day", "value": "20190206/1",
              "data": [
                { "name": "harvest", "value": "67.639" },
                { "name": "store.in", "value": "25.213" },
                { "name": "store.out", "value": "33.823" },
                { "name": "enjoy", "value": "29.285" },
                { "name": "grid.in", "value": "53.710" },
                { "name": "grid.out", "value": "33.133" }
              ]
            },
            { "name": "day.timeofday", "value": "20190206T0000/4",
              "data": [
                { "name": "harvest", "value": "14.478 16.617 19.221 17.323" },
                { "name": "store.in", "value": "2.837 2.723 16.514 3.139" },
                { "name": "store.out", "value": "6.511 14.162 5.087 8.063" },
                { "name": "enjoy", "value": "3.633 8.573 10.174 6.905" },
                { "name": "grid.in", "value": "13.049 12.058 17.291 11.312" },
                { "name": "grid.out", "value": "8.218 11.163 10.753 2.999" }
              ]
            }
          ]
        },
        { "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/period/day/20190207/1?site=999",
          "links": [
            { "rel": "self", "name": "day", "prompt": "Thu Feb 7th", "title": "07/02/19",
              "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/period/day/20190207/1?site=999",
              "render": "link"
            },
            { "rel": "collection", "name": "day.timeofday", "prompt": "Feb 7 Night - Feb 7 Evening",
              "title": "07/02/19 00:00 - 07/02/19 23:59", 
              "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/period/timeofday/20190207T0000/4?site=999"
            }
          ],
          "data": [
            { "name": "day", "value": "20190207/1",
              "data": [
                { "name": "harvest", "value": "40.487" },
                { "name": "store.in", "value": "46.285" },
                { "name": "store.out", "value": "36.414" },
                { "name": "enjoy", "value": "42.065" },
                { "name": "grid.in", "value": "60.249" },
                { "name": "grid.out", "value": "65.810" }
              ]
            },
            { "name": "day.timeofday", "value": "20190207T0000/4",
              "data": [
                { "name": "harvest", "value": "12.562 14.355 4.785 8.785" },
                { "name": "store.in", "value": "11.959 19.973 8.048 6.305" },
                { "name": "store.out", "value": "3.482 16.666 4.611 11.655" },
                { "name": "enjoy", "value": "14.435 11.439 7.516 8.675" },
                { "name": "grid.in", "value": "10.436 19.600 16.107 14.106" },
                { "name": "grid.out", "value": "9.612 15.357 20.516 20.325" }
              ]
            }
          ]
        },
        { "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/period/day/20190208/1?site=999",
          "links": [
            { "rel": "self", "name": "day", "prompt": "Fri Feb 8th", "title": "08/02/19",
              "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/period/day/20190208/1?site=999",
              "render": "link"
            },
            { "rel": "collection", "name": "day.timeofday", "prompt": "Feb 8 Night - Feb 8 Evening",
              "title": "08/02/19 00:00 - 08/02/19 23:59", 
              "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/period/timeofday/20190208T0000/4?site=999"
            }
          ],
          "data": [
            { "name": "day", "value": "20190208/1",
              "data": [
                { "name": "harvest", "value": "41.209" },
                { "name": "store.in", "value": "50.381" },
                { "name": "store.out", "value": "39.778" },
                { "name": "enjoy", "value": "44.251" },
                { "name": "grid.in", "value": "45.893" },
                { "name": "grid.out", "value": "48.455" }
              ]
            },
            { "name": "day.timeofday", "value": "20190208T0000/4",
              "data": [
                { "name": "harvest", "value": "15.999 4.729 13.717 6.764" },
                { "name": "store.in", "value": "8.614 12.059 19.861 9.847" },
                { "name": "store.out", "value": "11.394 12.397 3.823 12.164" },
                { "name": "enjoy", "value": "6.922 4.351 19.691 13.287" },
                { "name": "grid.in", "value": "20.120 11.357 5.306 9.110" },
                { "name": "grid.out", "value": "7.101 5.056 18.218 18.080" }
              ]
            }
          ]
        },
        { "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/period/day/20190209/1?site=999",
          "links": [
            { "rel": "self", "name": "day", "prompt": "Sat Feb 9th", "title": "09/02/19",
              "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/period/day/20190209/1?site=999",
              "render": "link"
            },
            { "rel": "collection", "name": "day.timeofday", "prompt": "Feb 9 Night - Feb 9 Evening",
              "title": "09/02/19 00:00 - 09/02/19 23:59", 
              "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/period/timeofday/20190209T0000/4?site=999"
            }
          ],
          "data": [
            { "name": "day", "value": "20190209/1",
              "data": [
                { "name": "harvest", "value": "64.347" },
                { "name": "store.in", "value": "41.775" },
                { "name": "store.out", "value": "44.196" },
                { "name": "enjoy", "value": "25.758" },
                { "name": "grid.in", "value": "24.605" },
                { "name": "grid.out", "value": "70.239" }
              ]
            },
            { "name": "day.timeofday", "value": "20190209T0000/4",
              "data": [
                { "name": "harvest", "value": "14.000 20.016 15.037 15.294" },
                { "name": "store.in", "value": "8.812 11.568 14.192 7.203" },
                { "name": "store.out", "value": "13.611 7.758 10.496 12.331" },
                { "name": "enjoy", "value": "7.070 9.485 5.213 3.990" },
                { "name": "grid.in", "value": "4.032 4.707 7.169 8.697" },
                { "name": "grid.out", "value": "19.473 18.050 18.175 14.541" }
              ]
            }
          ]
        },
        { "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/period/day/20190210/1?site=999",
          "links": [
            { "rel": "self", "name": "day", "prompt": "Sun Feb 10th", "title": "10/02/19",
              "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/period/day/20190210/1?site=999",
              "render": "link"
            },
            { "rel": "collection", "name": "day.timeofday", "prompt": "Feb 10 Night - Feb 10 Evening",
              "title": "10/02/19 00:00 - 10/02/19 23:59", 
              "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/period/timeofday/20190210T0000/4?site=999"
            }
          ],
          "data": [
            { "name": "day", "value": "20190210/1",
              "data": [
                { "name": "harvest", "value": "43.586" },
                { "name": "store.in", "value": "66.581" },
                { "name": "store.out", "value": "36.583" },
                { "name": "enjoy", "value": "57.136" },
                { "name": "grid.in", "value": "36.819" },
                { "name": "grid.out", "value": "35.975" }
              ]
            },
            { "name": "day.timeofday", "value": "20190210T0000/4",
              "data": [
                { "name": "harvest", "value": "18.626 7.612 4.609 12.739" },
                { "name": "store.in", "value": "19.577 19.504 7.257 20.243" },
                { "name": "store.out", "value": "11.503 15.791 5.494 3.795" },
                { "name": "enjoy", "value": "19.316 16.143 4.695 16.982" },
                { "name": "grid.in", "value": "11.176 2.974 11.926 10.743" },
                { "name": "grid.out", "value": "18.414 6.662 4.577 6.322" }
              ]
            }
          ]
        }
      ]
    }
  }
]
```
