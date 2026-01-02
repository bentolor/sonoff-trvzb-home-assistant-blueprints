# Sonoff Home Automation Blueprints

A collection of Home Assistant blueprints for Sonoff devices, designed to enhance your smart home automation.

## Current Blueprints

### Sonoff TRVZB - External Temperature Synchronization
This script was taken from the czech home assistant community: [Post from User Pete30](https://www.homeassistant-cz.cz/viewtopic.php?p=23736)

I translated, modified and tested it to make it more usable for non czech-speakers.

It synchronizes temperature from an external sensor to a Sonoff TRVZB thermostatic valve with configurable update thresholds.

**Features**
- Monitors your external temperature sensor so that your TRV knows the temperature in the room
- Updates temperature only when changes exceed your threshold (saves battery)
- Therefore we have a configurable update threshold (default: 0.1°C)
- Ensures Sonoff TRV is in "external" mode - these TRVs switch to different modes (internal, external_2 etc.) from time to time

**Requirements**
- External temperature sensor (e.g., Sonoff, Aqara, Shelly, Ecowitt)
- Sonoff TRVZB with external temperature input capability (Firmware 1.3+)

### Sonoff TRVZB - Window/Thermostat Synchronization

A Home Assistant blueprint specifically designed for Sonoff thermostats that monitors window sensors and ensures the "Window Open" feature remains active when windows are open.

**Features**

- Monitors window sensors and automatically activates Sonoff's "Window Open" mode when windows are opened
- Prevents the thermostat from turning off the window mode while windows remain open
- Sends notifications to your mobile devices when the thermostat attempts to resume heating with an open window
- Supports multiple windows and thermostats simultaneously (parallel mode)

**Requirements**

- Sonoff thermostat devices with "Window Open" functionality
- Binary sensor entities for your windows/doors
- Mobile app integration for notifications (optional)

## Installation

1. Copy the YAML file to your `<hass-config-dir>/blueprints/automation/<username>/` directory
2. Import the blueprint in Home Assistant (if not already present)
3. Create an automation using the blueprint

## Contributing

These blueprints were created with the assistance of AI.
Feel free to modify and adapt them to your needs.