{
    "collection": {
        "version": "0.2",
        "href": "http:/api.sundaya.com/energy/hse/week/20190204/1?site=9999",
        "links": [
            {
                "rel": "self", "name": "week", "prompt": "Week", "title": "04/02/2019 - 10/02/2019",
                "href": "http:/api.sundaya.com/energy/hse/week/20190204/1?site=9999"
            },
            {
                "rel": "collection", "name": "week.day", "prompt": "Days", "title": "Monday Tuesday Wednesday Thursday Friday Saturday Sunday",                
                "href": "http:/api.sundaya.com/energy/hse/day/20190204/7?site=9999"
            },
            {
                "rel": "up", "name": "week.month", "prompt": "Month", "title": "February", 
                "href": "http:/api.sundaya.com/energy/hse/month/201902/1?site=9999", "render": "link"                
            },
            {
                "rel": "next", "name": "week.next", "prompt": "Next", "title": "11/02/2019 - 17/02/2019",
                "href": "http:/api.sundaya.com/energy/hse/week/20190211/1?site=9999", "render": "link"
            },
            {
                "rel": "prev", "name": "week.previous", "prompt": "Previous", "title": "28/01/2019 - 03/02/2019",
                "href": "http:/api.sundaya.com/energy/hse/week/20190128/1?site=9999", "render": "link"
            }
        ],
        "items": [
            {
                "href": "http:/api.sundaya.com/energy/hse/day/20190204/1?site=9999",
                "links": [
                    { 
                        "rel": "self", "name": "day", "prompt": "Day", "title": "Monday",
                        "href": "http:/api.sundaya.com/energy/hse/day/20190204/1?site=9999", "render": "link"
                    },
                    {
                        "rel": "item", "name": "day.hours", "prompt": "Hours", "title": "06 07 08 09 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 01 02 03 04 05",                
                        "href": "http:/api.sundaya.com/energy/hse/hour/20190204T0600/24?site=9999"
                    }
                ],          
                "data": [
                    { "name": "harvest.day", "value": "15396" },
                    { "name": "store.day.in", "value": "15396" },
                    { "name": "store.day.out", "value": "15396" },
                    { "name": "enjoy.day", "value": "15396" },
                    { "name": "grid.day.in", "value": "0" },
                    { "name": "grid.day.out", "value": "15396" },
                    { "name": "harvest.day.hours", "value": "54 3640 33 23 55 44 54 3640 33 23 55 44 54 3640 33 23 55 44 54 3640 33 23 55 44" },
                    { "name": "store.day.hours.in", "value": "54 3640 33 23 55 44 54 3640 33 23 55 44 54 3640 33 23 55 44 54 3640 33 23 55 44" },
                    { "name": "store.day.hours.out", "value": "54 3640 33 23 55 44 54 3640 33 23 55 44 54 3640 33 23 55 44 54 3640 33 23 55 44" },
                    { "name": "enjoy.day.hours", "value": "54 3640 33 23 55 44 54 3640 33 23 55 44 54 3640 33 23 55 44 54 3640 33 23 55 44" },
                    { "name": "grid.day.hours.in", "value": "0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0" },
                    { "name": "grid.day.hours.out", "value": "54 3640 33 23 55 44 54 3640 33 23 55 44 54 3640 33 23 55 44 54 3640 33 23 55 44" }
                ]
            },
            {
                "href": "http:/api.sundaya.com/energy/hse/day/20190205/1?site=9999",
                "links": [
                    { 
                        "rel": "self", "name": "day", "prompt": "Day", "title": "Tuesday",
                        "href": "http:/api.sundaya.com/energy/hse/day/20190205/1?site=9999", "render": "link"
                    },
                    {
                        "rel": "item", "name": "day.hours", "prompt": "Hours", "title": "06 07 08 09 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 01 02 03 04 05",                
                        "href": "http:/api.sundaya.com/energy/hse/hour/20190204T0600/24?site=9999"
                    }
                ],          
                "data": [
                    { "name": "harvest.day", "value": "34464" },
                    { "name": "store.day.in", "value": "34464" },
                    { "name": "store.day.out", "value": "34464" },
                    { "name": "enjoy.day", "value": "34464" },
                    { "name": "grid.day.in", "value": "34464" },
                    { "name": "grid.day.out", "value": "34464" },
                    { "name": "harvest.day.hours", "value": "3640 3643 33 23 1233 44 3640 3643 33 23 1233 44 3640 3643 33 23 1233 44 3640 3643 33 23 1233 44" },
                    { "name": "store.day.hours.in", "value": "3640 3643 33 23 1233 44 3640 3643 33 23 1233 44 3640 3643 33 23 1233 44 3640 3643 33 23 1233 44" },
                    { "name": "store.day.hours.out", "value": "3640 3643 33 23 1233 44 3640 3643 33 23 1233 44 3640 3643 33 23 1233 44 3640 3643 33 23 1233 44" },
                    { "name": "enjoy.day.hours", "value": "3640 3643 33 23 1233 44 3640 3643 33 23 1233 44 3640 3643 33 23 1233 44 3640 3643 33 23 1233 44" },
                    { "name": "grid.day.hours.in", "value": "3640 3643 33 23 1233 44 3640 3643 33 23 1233 44 3640 3643 33 23 1233 44 3640 3643 33 23 1233 44" },
                    { "name": "grid.day.hours.out", "value": "3640 3643 33 23 1233 44 3640 3643 33 23 1233 44 3640 3643 33 23 1233 44 3640 3643 33 23 1233 44" }
                ]
            },
            {
                "href": "http:/api.sundaya.com/energy/hse/day/20190206/1?site=9999",
                "links": [
                    { 
                        "rel": "self", "name": "day", "prompt": "Day", "title": "Wednesday",
                        "href": "http:/api.sundaya.com/energy/hse/day/20190206/1?site=9999", "render": "link"
                    },
                    {
                        "rel": "item", "name": "day.hours", "prompt": "Hours", "title": "06 07 08 09 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 01 02 03 04 05",                
                        "href": "http:/api.sundaya.com/energy/hse/hour/20190206T0600/24?site=9999"
                    }
                ],          
                "data": [
                    { "name": "harvest.day", "value": "23972" },
                    { "name": "store.day.in", "value": "23972" },
                    { "name": "store.day.out", "value": "23972" },
                    { "name": "enjoy.day", "value": "23972" },
                    { "name": "grid.day.in", "value": "0" },
                    { "name": "grid.day.out", "value": "23972" },
                    { "name": "harvest.day.hours", "value": "54 30 33 23 2333 3520 54 30 33 23 2333 3520 54 30 33 23 2333 3520 54 30 33 23 2333 3520" },
                    { "name": "store.day.hours.in", "value": "54 30 33 23 2333 3520 54 30 33 23 2333 3520 54 30 33 23 2333 3520 54 30 33 23 2333 3520" },
                    { "name": "store.day.hours.out", "value": "54 30 33 23 2333 3520 54 30 33 23 2333 3520 54 30 33 23 2333 3520 54 30 33 23 2333 3520" },
                    { "name": "enjoy.day.hours", "value": "54 30 33 23 2333 3520 54 30 33 23 2333 3520 54 30 33 23 2333 3520 54 30 33 23 2333 3520" },
                    { "name": "grid.day.hours.in", "value": "0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0" },
                    { "name": "grid.day.hours.out", "value": "54 30 33 23 2333 3520 54 30 33 23 2333 3520 54 30 33 23 2333 3520 54 30 33 23 2333 3520" }
                ]
            },
            {
                "href": "http:/api.sundaya.com/energy/hse/day/20190207/1?site=9999",
                "links": [
                    { 
                        "rel": "self", "name": "day", "prompt": "Day", "title": "Thursday",
                        "href": "http:/api.sundaya.com/energy/hse/day/20190207/1?site=9999", "render": "link"
                    },
                    {
                        "rel": "item", "name": "day.hours", "prompt": "Hours", "title": "06 07 08 09 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 01 02 03 04 05",                
                        "href": "http:/api.sundaya.com/energy/hse/hour/20190207T0600/24?site=9999"
                    }
                ],          
                "data": [
                    { "name": "harvest.day", "value": "30548" },
                    { "name": "store.day.in", "value": "30548" },
                    { "name": "store.day.out", "value": "30548" },
                    { "name": "enjoy.day", "value": "30548" },
                    { "name": "grid.day.in", "value": "30548" },
                    { "name": "grid.day.out", "value": "30548" },
                    { "name": "harvest.day.hours", "value": "54 30 33 3520 2000 2000 54 30 33 3520 2000 2000 54 30 33 3520 2000 2000 54 30 33 3520 2000 2000" },
                    { "name": "store.day.hours.in", "value": "54 30 33 3520 2000 2000 54 30 33 3520 2000 2000 54 30 33 3520 2000 2000 54 30 33 3520 2000 2000" },
                    { "name": "store.day.hours.out", "value": "54 30 33 3520 2000 2000 54 30 33 3520 2000 2000 54 30 33 3520 2000 2000 54 30 33 3520 2000 2000" },
                    { "name": "enjoy.day.hours", "value": "54 30 33 3520 2000 2000 54 30 33 3520 2000 2000 54 30 33 3520 2000 2000 54 30 33 3520 2000 2000" },
                    { "name": "grid.day.hours.in", "value": "54 30 33 3520 2000 2000 54 30 33 3520 2000 2000 54 30 33 3520 2000 2000 54 30 33 3520 2000 2000" },
                    { "name": "grid.day.hours.out", "value": "54 30 33 3520 2000 2000 54 30 33 3520 2000 2000 54 30 33 3520 2000 2000 54 30 33 3520 2000 2000" }
                ]
            },
            {
                "href": "http:/api.sundaya.com/energy/hse/day/20190208/1?site=9999",
                "links": [
                    { 
                        "rel": "self", "name": "day", "prompt": "Day", "title": "Friday",
                        "href": "http:/api.sundaya.com/energy/hse/day/20190208/1?site=9999", "render": "link"
                    },
                    {
                        "rel": "item", "name": "day.hours", "prompt": "Hours", "title": "06 07 08 09 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 01 02 03 04 05",                
                        "href": "http:/api.sundaya.com/energy/hse/hour/20190208T0600/24?site=9999"
                    }
                ],          
                "data": [
                    { "name": "harvest.day", "value": "38484" },
                    { "name": "store.day.in", "value": "38484" },
                    { "name": "store.day.out", "value": "38484" },
                    { "name": "enjoy.day", "value": "38484" },
                    { "name": "grid.day.in", "value": "38484" },
                    { "name": "grid.day.out", "value": "38484" },
                    { "name": "harvest.day.hours", "value": "54 30 3520 3640 2333 44 54 30 3520 3640 2333 44 54 30 3520 3640 2333 44 54 30 3520 3640 2333 44" },
                    { "name": "store.day.hours.in", "value": "54 30 3520 3640 2333 44 54 30 3520 3640 2333 44 54 30 3520 3640 2333 44 54 30 3520 3640 2333 44" },
                    { "name": "store.day.hours.out", "value": "54 30 3520 3640 2333 44 54 30 3520 3640 2333 44 54 30 3520 3640 2333 44 54 30 3520 3640 2333 44" },
                    { "name": "enjoy.day.hours", "value": "54 30 3520 3640 2333 44 54 30 3520 3640 2333 44 54 30 3520 3640 2333 44 54 30 3520 3640 2333 44" },
                    { "name": "grid.day.hours.in", "value": "54 30 3520 3640 2333 44 54 30 3520 3640 2333 44 54 30 3520 3640 2333 44 54 30 3520 3640 2333 44" },
                    { "name": "grid.day.hours.out", "value": "54 30 3520 3640 2333 44 54 30 3520 3640 2333 44 54 30 3520 3640 2333 44 54 30 3520 3640 2333 44" }
                ]
            },
            {
                "href": "http:/api.sundaya.com/energy/hse/day/20190209/1?site=9999",
                "links": [
                    { 
                        "rel": "self", "name": "day", "prompt": "Day", "title": "Saturday",
                        "href": "http:/api.sundaya.com/energy/hse/day/20190209/1?site=9999", "render": "link"
                    },
                    {
                        "rel": "item", "name": "day.hours", "prompt": "Hours", "title": "06 07 08 09 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 01 02 03 04 05",                
                        "href": "http:/api.sundaya.com/energy/hse/hour/20190209T0600/24?site=9999"
                    }
                ],          
                "data": [
                    { "name": "harvest.day", "value": "24156" },
                    { "name": "store.day.in", "value": "24156" },
                    { "name": "store.day.out", "value": "24156" },
                    { "name": "enjoy.day", "value": "24156" },
                    { "name": "grid.day.in", "value": "0" },
                    { "name": "grid.day.out", "value": "24156" },
                    { "name": "harvest.day.hours", "value": "54 3520 33 2333 55 44 54 3520 33 2333 55 44 54 3520 33 2333 55 44 54 3520 33 2333 55 44" },
                    { "name": "store.day.hours.in", "value": "54 3520 33 2333 55 44 54 3520 33 2333 55 44 54 3520 33 2333 55 44 54 3520 33 2333 55 44" },
                    { "name": "store.day.hours.out", "value": "54 3520 33 2333 55 44 54 3520 33 2333 55 44 54 3520 33 2333 55 44 54 3520 33 2333 55 44" },
                    { "name": "enjoy.day.hours", "value": "54 3520 33 2333 55 44 54 3520 33 2333 55 44 54 3520 33 2333 55 44 54 3520 33 2333 55 44" },
                    { "name": "grid.day.hours.in", "value": "0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0" },
                    { "name": "grid.day.hours.out", "value": "54 3520 33 2333 55 44 54 3520 33 2333 55 44 54 3520 33 2333 55 44 54 3520 33 2333 55 44" }
                ]
            },
            {
                "href": "http:/api.sundaya.com/energy/hse/day/20190210/1?site=9999",
                "links": [
                    { 
                        "rel": "self", "name": "day", "prompt": "Day", "title": "Sunday",
                        "href": "http:/api.sundaya.com/energy/hse/day/20190210/1?site=9999", "render": "link"
                    },
                    {
                        "rel": "item", "name": "day.hours", "prompt": "Hours", "title": "06 07 08 09 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 01 02 03 04 05",                
                        "href": "http:/api.sundaya.com/energy/hse/hour/20190210T0600/24?site=9999"
                    }
                ],          
                "data": [
                    { "name": "harvest.day", "value": "22684" },
                    { "name": "store.day.in", "value": "22684" },
                    { "name": "store.day.out", "value": "22684" },
                    { "name": "enjoy.day", "value": "22684" },
                    { "name": "grid.day.in", "value": "22684" },
                    { "name": "grid.day.out", "value": "22684" },
                    { "name": "harvest.day.hours", "value": "54 30 3520 23 2000 44 54 30 3520 23 2000 44 54 30 3520 23 2000 44 54 30 3520 23 2000 44" },
                    { "name": "store.day.hours.in", "value": "54 30 3520 23 2000 44 54 30 3520 23 2000 44 54 30 3520 23 2000 44 54 30 3520 23 2000 44" },
                    { "name": "store.day.hours.out", "value": "54 30 3520 23 2000 44 54 30 3520 23 2000 44 54 30 3520 23 2000 44 54 30 3520 23 2000 44" },
                    { "name": "enjoy.day.hours", "value": "54 30 3520 23 2000 44 54 30 3520 23 2000 44 54 30 3520 23 2000 44 54 30 3520 23 2000 44" },
                    { "name": "grid.day.hours.in", "value": "54 30 3520 23 2000 44 54 30 3520 23 2000 44 54 30 3520 23 2000 44 54 30 3520 23 2000 44" },
                    { "name": "grid.day.hours.out", "value": "54 30 3520 23 2000 44 54 30 3520 23 2000 44 54 30 3520 23 2000 44 54 30 3520 23 2000 44" }
                ]
            }
        ]
    }
}