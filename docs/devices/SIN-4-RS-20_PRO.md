---
title: "NodOn SIN-4-RS-20_PRO control via MQTT"
description: "Integrate your NodOn SIN-4-RS-20_PRO via Zigbee2MQTT with whatever smart home infrastructure you are using without the vendor's bridge or gateway."
addedAt: 2022-01-31T17:42:44
pageClass: device-page
---

<!-- !!!! -->
<!-- ATTENTION: This file is auto-generated through docgen! -->
<!-- You can only edit the "Notes"-Section between the two comment lines "Notes BEGIN" and "Notes END". -->
<!-- Do not use h1 or h2 heading within "## Notes"-Section. -->
<!-- !!!! -->

# NodOn SIN-4-RS-20_PRO

|     |     |
|-----|-----|
| Model | SIN-4-RS-20_PRO  |
| Vendor  | [NodOn](/supported-devices/#v=NodOn)  |
| Description | Roller shutter relay switch |
| Exposes | cover (state, position, tilt), calibration, calibration_vertical_run_time_up, calibration_vertical_run_time_down, calibration_rotation_run_time_up, calibration_rotation_run_time_down, linkquality |
| Picture | ![NodOn SIN-4-RS-20_PRO](https://www.zigbee2mqtt.io/images/devices/SIN-4-RS-20_PRO.png) |


<!-- Notes BEGIN: You can edit here. Add "## Notes" headline if not already present. -->


<!-- Notes END: Do not edit below this line -->


## OTA updates
This device supports OTA updates, for more information see [OTA updates](../guide/usage/ota_updates.md).


## Options
*[How to use device type specific configuration](../guide/configuration/devices-groups.md#specific-device-options)*

* `invert_cover`: Inverts the cover position, false: open=100,close=0, true: open=0,close=100 (default false). The value must be `true` or `false`

* `cover_position_tilt_disable_report`: Do not publish set cover target position as a normal 'position' value (default false). The value must be `true` or `false`


## Exposes

### Cover 
The current state of this cover is in the published state under the `state` property (value is `OPEN` or `CLOSE`).
To control this cover publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"state": "OPEN"}`, `{"state": "CLOSE"}`, `{"state": "STOP"}`.
It's not possible to read (`/get`) this value.
To change the position publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"position": VALUE}` where `VALUE` is a number between `0` and `100`.
To change the tilt publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"tilt": VALUE}` where `VALUE` is a number between `0` and `100`.

### Calibration (enum)
Automatic calibration of the roller shutter..
Value can be found in the published state on the `calibration` property.
To read (`/get`) the value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/get` with payload `{"calibration": ""}`.
To write (`/set`) a value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"calibration": NEW_VALUE}`.
The possible values are: `stop`, `start`.

### Calibration vertical run time up (numeric)
Manuel calibration: Set vertical run time up of the roller shutter. Do not change it if your roller shutter is already calibrated..
Value can be found in the published state on the `calibration_vertical_run_time_up` property.
To read (`/get`) the value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/get` with payload `{"calibration_vertical_run_time_up": ""}`.
To write (`/set`) a value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"calibration_vertical_run_time_up": NEW_VALUE}`.
The minimal value is `0` and the maximum value is `65535`.
The unit of this value is `10 ms`.

### Calibration vertical run time down (numeric)
Manuel calibration: Set vertical run time down of the roller shutter. Do not change it if your roller shutter is already calibrated..
Value can be found in the published state on the `calibration_vertical_run_time_down` property.
To read (`/get`) the value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/get` with payload `{"calibration_vertical_run_time_down": ""}`.
To write (`/set`) a value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"calibration_vertical_run_time_down": NEW_VALUE}`.
The minimal value is `0` and the maximum value is `65535`.
The unit of this value is `10 ms`.

### Calibration rotation run time up (numeric)
Manuel calibration: Set rotation run time up of the roller shutter. Do not change it if your roller shutter is already calibrated..
Value can be found in the published state on the `calibration_rotation_run_time_up` property.
To read (`/get`) the value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/get` with payload `{"calibration_rotation_run_time_up": ""}`.
To write (`/set`) a value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"calibration_rotation_run_time_up": NEW_VALUE}`.
The minimal value is `0` and the maximum value is `65535`.
The unit of this value is `ms`.

### Calibration rotation run time down (numeric)
Manuel calibration: Set rotation run time down of the roller shutter. Do not change it if your roller shutter is already calibrated..
Value can be found in the published state on the `calibration_rotation_run_time_down` property.
To read (`/get`) the value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/get` with payload `{"calibration_rotation_run_time_down": ""}`.
To write (`/set`) a value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"calibration_rotation_run_time_down": NEW_VALUE}`.
The minimal value is `0` and the maximum value is `65535`.
The unit of this value is `ms`.

### Linkquality (numeric)
Link quality (signal strength).
Value can be found in the published state on the `linkquality` property.
It's not possible to read (`/get`) or write (`/set`) this value.
The minimal value is `0` and the maximum value is `255`.
The unit of this value is `lqi`.

