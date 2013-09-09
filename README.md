# Radio Thermostat Munin plugin

## Description

This is a [Munin](http://munin-monitoring.org/) plugin for monitoring
thermostats made by [Radio
Thermostat](http://radiothermostat.com/). Plugins included:

* hvac_runtime - reports cool and heat runtime in hours per day
* hvac_usage - reports cool and heat usage in percentage per day
* temperature - reports indoor and outdoor temperatures and set points in degrees Fahrenheit

## Prerequisites

0. Radio Thermostat connected to a WiFi router (mine is a [3M Filtrete 3M-50](http://www.radiothermostat.com/filtrete/products/3M-50/))
0. web server with Munin and Python installed that is able to connect to thermostat

## Installation

0. Install Python.
0. Install Munin.
0. Copy radio-thermostat-munin-plugin files to `/usr/share/munin/plugins`.
0. Make symbolic links for each file from `/usr/share/munin/plugins` to `/etc/munin/plugins`.
0. `service munin-node restart`

## Use

    $ ./temperature config
    graph_scale yes
    graph_category thermostat
    graph_title Temperature
    graph_vlabel degrees (F)
    outdoor.label outdoor at ZIP 85719
    outdoor.colour ffa500
    outdoor.draw AREA
    indoor.label indoor
    indoor.colour 00ff00
    coolsetpoint.label cool set point
    coolsetpoint.colour 0000ff
    heatsetpoint.label heat set point
    heatsetpoint.colour ff0000

    $ ./temperature
    outdoor.value 68
    indoor.value 77.0
    coolsetpoint.value 76.0
    heatsetpoint.value 60.0
