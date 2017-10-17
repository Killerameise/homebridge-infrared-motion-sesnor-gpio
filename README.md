# homebridge-contact-sensor
This Homebridge plugin enables you to control a infrared motion sensor switch.

## Setup

1) Wire a infrared motion senor to your Raspberry Pi.
<img src="docs/circuit.png" width="300">

2) Install this plugin

```bash
npm i -g homebridge-gpio-motion-sensor
```

3) Rename the sample-config.json to config.json and integrate your sensor in the accessories array. The pins
of the Raspberry Pi require root rights to control them. Therefore you have to save your config file not
in your users directory. Put it under `/root/.homebridge/config.json`.
If you are already running homekit with other apps integrate the accessories into your config.json
and move your config file to the path above.

Accessory JSON config looks like:

```bash
{
    "accessory": "MotionSensor",
    "name": "MotionSensor1",
    "pin": 2
}
```
