# Energy
---

### GET response - HSE

[/energy/hse/periods/week/20190204/1?site=9999](http:/api.endpoints.sundaya.cloud.goog/energy?site=9999)

```
*** REQUEST ***	
GET /energy/hse/periods/week/20190204?site=9999 HTTP/1.1	
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
         "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/periods/week/20190204/1?site=999",
         "links": [
           { "rel": "self", "name": "week", "prompt": "Week 06 2019", "title": "04/02/19 - 10/02/19",
             "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/periods/week/20190204/1?site=999"
           },
           { "rel": "collection", "name": "week.day", "prompt": "Mon Feb 4th - Sun Feb 10th", "title": "04/02/19 - 10/02/19",
             "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/periods/day/20190204/7?site=999"
           },
           { "rel": "up", "name": "month", "prompt": "Feb 2019", "title": "01/02/19 - 28/02/19",
             "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/periods/month/20190201/1?site=999", "render": "link"
           },
           { "rel": "next", "name": "week", "prompt": "Week 07 2019", "title": "11/02/19 - 17/02/19",
             "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/periods/week/20190211/1?site=999", "render": "link"
           },
           { "rel": "prev", "name": "week", "prompt": "Week 05 2019", "title": "28/01/19 - 03/02/19",
             "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/periods/week/20190128/1?site=999", "render": "link"
           }
        ],
        "items": [
          { "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/periods/day/20190204/1?site=999",
            "links": [
             { "rel": "self", "name": "day", "prompt": "Mon Feb 4th", "title": "04/02/19",
               "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/periods/day/20190204/1?site=999", "render": "link"
             },
             { "rel": "collection", "name": "day.timeofday", "prompt": "Feb 4 Night - Feb 4 Evening", "title": "04/02/19 00:00 - 04/02/19 23:59",
               "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/periods/timeofday/20190204T0000/4?site=999"
             }
           ],          
            "data": [
             { "name": "harvest.day", "value": "21.133881" },
             { "name": "store.in.day", "value": "26.500302" },
             { "name": "store.out.day", "value": "46.664185" },
             { "name": "enjoy.day", "value": "21.965303" },
             { "name": "grid.in.day", "value": "22.92243" },
             { "name": "grid.out.day", "value": "72.374014" },
             { "name": "harvest.day.timeofday", "value": "20.227483 6.297591 18.853748 8.047184" },
             { "name": "store.in.day.timeofday", "value": "4.986878 17.92982 10.781232 7.655939" },
             { "name": "store.out.day.timeofday", "value": "14.488899 3.26788 5.645879 12.476284" },
             { "name": "enjoy.day.timeofday", "value": "12.986113 13.379268 13.032179 13.859057" },
             { "name": "grid.in.day.timeofday", "value": "10.679414 17.290549 8.281113 9.166056" },
             { "name": "grid.out.day.timeofday", "value": "15.205374 12.402503 12.635302 13.723077" }
           ]
          },
       
          { "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/periods/day/20190205/1?site=999",
            "links": [
             { "rel": "self", "name": "day", "prompt": "Tue Feb 5th", "title": "05/02/19",
               "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/periods/day/20190205/1?site=999", "render": "link"
             },
             { "rel": "collection", "name": "day.timeofday", "prompt": "Feb 5 Night - Feb 5 Evening", "title": "05/02/19 00:00 - 05/02/19 23:59",
               "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/periods/timeofday/20190205T0000/4?site=999"
             }
           ],          
            "data": [
             { "name": "harvest.day", "value": "11.039792" },
             { "name": "store.in.day", "value": "81.717935" },
             { "name": "store.out.day", "value": "14.860573" },
             { "name": "enjoy.day", "value": "55.103325" },
             { "name": "grid.in.day", "value": "72.07423" },
             { "name": "grid.out.day", "value": "11.997864" },
             { "name": "harvest.day.timeofday", "value": "12.191019 8.02447 7.558786 8.075648" },
             { "name": "store.in.day.timeofday", "value": "16.603728 11.46813 16.972553 12.162093" },
             { "name": "store.out.day.timeofday", "value": "15.143538 17.554213 17.520763 14.94898" },
             { "name": "enjoy.day.timeofday", "value": "15.365327 4.875735 6.437416 12.907601" },
             { "name": "grid.in.day.timeofday", "value": "19.551429 16.185555 3.222114 17.667317" },
             { "name": "grid.out.day.timeofday", "value": "17.093486 9.621871 17.99346 7.610456" }
           ]
          },
          { "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/periods/day/20190206/1?site=999",
            "links": [
             { "rel": "self", "name": "day", "prompt": "Wed Feb 6th", "title": "06/02/19",
               "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/periods/day/20190206/1?site=999", "render": "link"
             },
             { "rel": "collection", "name": "day.timeofday", "prompt": "Feb 6 Night - Feb 6 Evening", "title": "06/02/19 00:00 - 06/02/19 23:59",
               "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/periods/timeofday/20190206T0000/4?site=999"
             }
           ],          
            "data": [
             { "name": "harvest.day", "value": "23.152329" },
             { "name": "store.in.day", "value": "35.660656" },
             { "name": "store.out.day", "value": "71.771244" },
             { "name": "enjoy.day", "value": "62.261981" },
             { "name": "grid.in.day", "value": "19.449194" },
             { "name": "grid.out.day", "value": "76.236531" },
             { "name": "harvest.day.timeofday", "value": "12.516541 10.049257 19.858797 7.300562" },
             { "name": "store.in.day.timeofday", "value": "15.328287 14.817654 7.47053 4.625065" },
             { "name": "store.out.day.timeofday", "value": "17.995133 10.049335 19.918784 7.382297" },
             { "name": "enjoy.day.timeofday", "value": "9.371441 8.220574 3.776384 6.484257" },
             { "name": "grid.in.day.timeofday", "value": "4.621802 11.150176 11.875279 4.386746" },
             { "name": "grid.out.day.timeofday", "value": "8.321272 7.791462 3.881439 14.652837" }
           ]
          },
          { "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/periods/day/20190207/1?site=999",
            "links": [
             { "rel": "self", "name": "day", "prompt": "Thu Feb 7th", "title": "07/02/19",
               "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/periods/day/20190207/1?site=999", "render": "link"
             },
             { "rel": "collection", "name": "day.timeofday", "prompt": "Feb 7 Night - Feb 7 Evening", "title": "07/02/19 00:00 - 07/02/19 23:59",
               "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/periods/timeofday/20190207T0000/4?site=999"
             }
           ],          
            "data": [
             { "name": "harvest.day", "value": "74.541264" },
             { "name": "store.in.day", "value": "48.260928" },
             { "name": "store.out.day", "value": "53.096994" },
             { "name": "enjoy.day", "value": "52.178096" },
             { "name": "grid.in.day", "value": "52.894455" },
             { "name": "grid.out.day", "value": "21.451133" },
             { "name": "harvest.day.timeofday", "value": "14.106008 17.124244 17.590686 17.935181" },
             { "name": "store.in.day.timeofday", "value": "8.653198 8.267208 12.275318 13.308442" },
             { "name": "store.out.day.timeofday", "value": "16.94193 6.060651 17.37325 11.900468" },
             { "name": "enjoy.day.timeofday", "value": "14.65374 9.89641 3.196515 19.634621" },
             { "name": "grid.in.day.timeofday", "value": "17.775864 6.955405 6.863084 4.095699" },
             { "name": "grid.out.day.timeofday", "value": "10.010593 9.620064 9.747363 20.59841" }
           ]
          },
          { "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/periods/day/20190208/1?site=999",
            "links": [
             { "rel": "self", "name": "day", "prompt": "Fri Feb 8th", "title": "08/02/19",
               "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/periods/day/20190208/1?site=999", "render": "link"
             },
             { "rel": "collection", "name": "day.timeofday", "prompt": "Feb 8 Night - Feb 8 Evening", "title": "08/02/19 00:00 - 08/02/19 23:59",
               "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/periods/timeofday/20190208T0000/4?site=999"
             }
           ],          
            "data": [
             { "name": "harvest.day", "value": "71.85934" },
             { "name": "store.in.day", "value": "16.730765" },
             { "name": "store.out.day", "value": "17.784198" },
             { "name": "enjoy.day", "value": "67.56808" },
             { "name": "grid.in.day", "value": "80.506569" },
             { "name": "grid.out.day", "value": "82.091402" },
             { "name": "harvest.day.timeofday", "value": "12.843441 6.937956 6.878024 2.743876" },
             { "name": "store.in.day.timeofday", "value": "18.868205 12.351783 5.351746 3.083962" },
             { "name": "store.out.day.timeofday", "value": "3.350201 13.785468 15.996737 9.794333" },
             { "name": "enjoy.day.timeofday", "value": "18.184508 8.763629 7.499887 13.31969" },
             { "name": "grid.in.day.timeofday", "value": "6.184032 19.764243 19.968035 6.687072" },
             { "name": "grid.out.day.timeofday", "value": "10.41211 4.892776 9.835627 12.92249" }
           ]
          },
          { "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/periods/day/20190209/1?site=999",
            "links": [
             { "rel": "self", "name": "day", "prompt": "Sat Feb 9th", "title": "09/02/19",
               "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/periods/day/20190209/1?site=999", "render": "link"
             },
             { "rel": "collection", "name": "day.timeofday", "prompt": "Feb 9 Night - Feb 9 Evening", "title": "09/02/19 00:00 - 09/02/19 23:59",
               "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/periods/timeofday/20190209T0000/4?site=999"
             }
           ],          
            "data": [
             { "name": "harvest.day", "value": "46.057653" },
             { "name": "store.in.day", "value": "82.332075" },
             { "name": "store.out.day", "value": "20.558368" },
             { "name": "enjoy.day", "value": "39.512444" },
             { "name": "grid.in.day", "value": "31.375409" },
             { "name": "grid.out.day", "value": "28.011426" },
             { "name": "harvest.day.timeofday", "value": "3.105644 16.107461 16.145148 10.541794" },
             { "name": "store.in.day.timeofday", "value": "11.665631 16.227515 10.227591 20.568639" },
             { "name": "store.out.day.timeofday", "value": "10.205591 2.940063 8.69389 3.716086" },
             { "name": "enjoy.day.timeofday", "value": "8.558258 7.300411 14.124559 7.674574" },
             { "name": "grid.in.day.timeofday", "value": "18.39727 18.452236 13.985479 2.946567" },
             { "name": "grid.out.day.timeofday", "value": "13.317777 10.721167 15.230591 10.863962" }
           ]
          },
          { "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/periods/day/20190210/1?site=999",
            "links": [
             { "rel": "self", "name": "day", "prompt": "Sun Feb 10th", "title": "10/02/19",
               "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/periods/day/20190210/1?site=999", "render": "link"
             },
             { "rel": "collection", "name": "day.timeofday", "prompt": "Feb 10 Night - Feb 10 Evening", "title": "10/02/19 00:00 - 10/02/19 23:59",
               "href": "http://api.endpoints.sundaya.cloud.goog/energy/hse/periods/timeofday/20190210T0000/4?site=999"
             }
           ],          
            "data": [
             { "name": "harvest.day", "value": "31.231499" },
             { "name": "store.in.day", "value": "46.881011" },
             { "name": "store.out.day", "value": "66.939857" },
             { "name": "enjoy.day", "value": "24.705035" },
             { "name": "grid.in.day", "value": "55.216595" },
             { "name": "grid.out.day", "value": "54.768807" },
             { "name": "harvest.day.timeofday", "value": "19.002456 5.073383 11.479933 14.086283" },
             { "name": "store.in.day.timeofday", "value": "4.632091 4.679907 8.214744 18.165258" },
             { "name": "store.out.day.timeofday", "value": "16.033444 16.986144 17.859252 8.370705" },
             { "name": "enjoy.day.timeofday", "value": "4.889902 16.643386 20.3145 6.904358" },
             { "name": "grid.in.day.timeofday", "value": "18.204944 14.541631 6.105331 7.351056" },
             { "name": "grid.out.day.timeofday", "value": "3.139811 4.778908 3.729571 18.143747" }
           ]
          }
       ] 
      }
    }
   ]
```
