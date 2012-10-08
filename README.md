# Radio Thermostat Munin plugin

## Description

This is a [Munin](http://munin-monitoring.org/) plugin for monitoring
the temperature reported by a [Radio
Termostat](http://radiothermostat.com/). More plugins are planned.

## Use

   $ ./temperature config
   graph_category thermostat
   graph_title Temperature (degrees F)
   graph_vlabel temperature
   temperature.label temperature
   $ ./temperature
   temperature.value 75.0
