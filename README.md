# Radio Thermostat Munin plugin

## Description

This is a [Munin](http://munin-monitoring.org/) plugin for monitoring
thermostats made by [Radio
Termostat](http://radiothermostat.com/). Plugins included:

* cool_runtime - cooling system runtime in minutes
* temperature - degrees Fahrenheit measured by thermostat

More plugins are planned.

## Use

    $ ./temperature config
    graph_category thermostat
    graph_title Temperature
    graph_vlabel degrees (F)
    temperature.label degrees (F)

    $ ./temperature
    temperature.value 75.0
