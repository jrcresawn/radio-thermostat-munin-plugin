# Radio Thermostat Munin plugin

## Description

This is a [Munin](http://munin-monitoring.org/) plugin for monitoring
thermostats made by [Radio
Termostat](http://radiothermostat.com/). Plugins included:

* hvac_usage - reports cool and heat usage
* temperature - reports indoor and outdoor degrees Fahrenheit

## Use

    $ ./temperature config
    graph_scale yes
    graph_category thermostat
    graph_title Temperature
    graph_vlabel degrees (F)
    indoor.label indoor
    outdoor.label ZIP Code: 85719

    $ ./temperature
    indoor.value 76.0
    outdoor.value 88