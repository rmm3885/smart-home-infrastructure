# Smart Home Infrastructure System

This project documents a distributed home automation system integrating IoT devices across Zigbee, Matter, and Wi-Fi using Home Assistant.

## Overview
- YAML-based automation logic
- Real-time monitoring and system debugging
- Incident analysis and system reliability improvements

## Structure

### Automations
- `stairs_light.yaml` — Presence-based lighting automation

### Incidents
- `petlibro-feeder-connectivity.md` — Device connectivity debugging
- `aqara-p2-presence.md` — Presence sensor reliability issue

## Key Skills Demonstrated
- Distributed systems integration
- Debugging cross-protocol communication issues
- YAML-based configuration and automation
- Network troubleshooting and system reliability

## Example Automation

```yaml
trigger:
  - platform: state
    entity_id: binary_sensor.stairs_presence
    to: "on"
action:
  - service: light.turn_on
    target:
      entity_id: light.stairs
