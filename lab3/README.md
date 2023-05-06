# Lab 3 — Python
## Objectives:
- Study the GitHub repository [Lesson 3](https://github.com/kevinwlu/iot/tree/master/lesson3) labs
- Install required Python packages such as jdcal, astral, and geopy
```
$ cd ~/iot
$ cd *3
$ python3 julian.py
$ python3 date_example.py
$ python3 datetime_example.py
$ python3 time_example.py
$ python3 sun.py 'New York'
$ python3 moon.py
$ python3 coordinates.py 'SC Williams Library'
$ python3 address.py '40.74480675, -74.02532862031404'
$ python3 cpu.py
$ python3 battery.py
$ python3 documentstats.py document.txt
```

## julian.py
```
$ python3 julian.py
Calendar Date: 2023-05-05
Julian Date: 2460069.5
Modified Julian Date: 60069.0

```

## date_example.py
```
$ python3 date_example.py
Date: 2023-05-05
Date: 05-05-23
Day of Week: Friday
Month: May
Year: 2023
107 days after the first day of classes
-1 days before the last day of classes
```

## datetime_example.py
```
2023-05-05 18:42:08.099838
2023-05-05 18:42:08.099837
2023-05-05 22:42:08.099837
1683326528.0998378
Fri May  5 18:42:08 2023
2023-05-05 18:42:08.099838
2023-05-05 22:42:08.099838
```

## time_example.py
```
$ python3 time_example.py dwadwa
Fri May  5 18:56:05 2023
```

## sun.py 'New York'
```
$ python3 sun.py 'New York'
Information for New York/USA

Timezone: US/Eastern
Latitude: 40.72; Longitude: -74.00
```

## moon.py
```
$ python3 moon.py
2023-05-05 Moon Phase: 13
2023-05-06 Moon Phase: 14
2023-05-07 Moon Phase: 15
2023-05-08 Moon Phase: 16
2023-05-09 Moon Phase: 17
2023-05-10 Moon Phase: 18
2023-05-11 Moon Phase: 19
2023-05-12 Moon Phase: 20
2023-05-13 Moon Phase: 21
2023-05-14 Moon Phase: 22
2023-05-15 Moon Phase: 23
2023-05-16 Moon Phase: 24
2023-05-17 Moon Phase: 25
2023-05-18 Moon Phase: 26
2023-05-19 Moon Phase: 27
2023-05-20 Moon Phase: 0
2023-05-21 Moon Phase: 1
2023-05-22 Moon Phase: 2
2023-05-23 Moon Phase: 3
2023-05-24 Moon Phase: 4
2023-05-25 Moon Phase: 5
2023-05-26 Moon Phase: 6
2023-05-27 Moon Phase: 6
2023-05-28 Moon Phase: 7
2023-05-29 Moon Phase: 8
2023-05-30 Moon Phase: 9
2023-05-31 Moon Phase: 10
2023-06-01 Moon Phase: 11
2023-06-02 Moon Phase: 12
2023-06-03 Moon Phase: 13
```

## coordinates.py 'SC Williams Library'
```
$ python3 coordinates.py 'SC Williams Library'
Library Parking, Williams Lake, Cariboo Regional District, British Columbia, Canada
(52.130143399999994, -122.14187089155848)
```

## address.py '40.74480675, -74.02532862031404'
```
$ python3 address.py '40.74480675, -74.02532862031404'
Samuel C. Williams Library, Field House Road, Hoboken, Hudson County, New Jersey, 07030, United States
(40.74480675, -74.02532861159351)
```

## cpu.py
```
$ python3 cpu.py

The number of physical cores =  6
The number of logical CPUs =  12
The utilization per second as a percentage for each CPU
[1.6, 1.6, 1.6, 0.0, 4.7, 1.6, 1.6, 0.0, 75.4, 1.6, 10.9, 0.0]
[13.6, 3.1, 7.8, 1.6, 3.1, 0.0, 6.2, 0.0, 51.6, 1.6, 21.9, 1.6]
```

## battery.py
```
$ python3 battery.py
sbattery(percent=100, secsleft=<BatteryTime.POWER_TIME_UNLIMITED: -2>, power_plugged=True)
```

## documentstats.py document.txt
```
$ python3 documentstats.py document.txt
Word Count: 1343
Top Ten Words: [('our', 26), ('their', 20), ('has', 20), ('he', 19), ('them', 15), ('these', 13), ('have', 11), ('we', 11), ('us', 11), ('people', 10)]
```
