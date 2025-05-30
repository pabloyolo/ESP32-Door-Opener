# ESP32 Building Door Opener

Control your apartment or building entry door with an ESP32 and relay wired to the portphone's open switch. Integrates with Home Assistant or MQTT for easy control from anywhere.

## 🛠️ Features

- Open building door remotely via ESP32 relay

## 📷 Hardware

- ESP32 (e.g., DevKit v1)
- 5V relay module
- Wires and connectors
- Rj45 connectors/ cable

![Wiring Diagram](hardware/wiring-diagram.png)

More in [hardware/parts-list.md](hardware/parts-list.md)

## 🔌 Firmware

You can use either:
- Arduino (.ino) sketch (see `firmware/esp32-door-relay.ino`)
- ESPHome YAML config (coming soon)

## 🏠 Home Assistant Integration

Switch and automation examples in [home-assistant/](home-assistant/)

Example switch:
```yaml
switch:
  - platform: mqtt
    name: "Building Door"
    command_topic: "esp32/door/relay"
    payload_on: "ON"
    payload_off: "OFF"
