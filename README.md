# FILE2BYTE_SEND_RECV_MQTT

A minimal Python utility for sending and receiving arbitrary files (images, binaries, etc.) over MQTT by encoding them as byte arrays. Designed for use with Python and MicroPython on devices such as ESP32 and ESP32-CAM.

## Features

- Send any file by opening it in bytes mode and publishing as a `bytearray` via MQTT
- Receive files by subscribing to an MQTT topic and writing received bytes to a file
- Compatible with MicroPython for ESP32/ESP32-CAM deployments
- Minimal dependencies — uses `paho-mqtt` only

## Tech Stack

- Python 3 / MicroPython
- paho-mqtt

## Project Structure

| File | Description |
|---|---|
| `send.py` | Opens a file in binary mode and publishes it as a bytearray to an MQTT topic |
| `receive.py` | Subscribes to an MQTT topic and saves incoming bytes to a file |

## Requirements

```
paho-mqtt
```

Install with:

```bash
pip install paho-mqtt
```

## Usage

Edit `MQTT_SERVER` and `MQTT_PATH` in both scripts to match your broker.

**Send a file:**

```bash
python send.py
```

**Receive a file:**

```bash
python receive.py
```

For MicroPython (ESP32), adapt the scripts using the `umqtt` library instead of `paho-mqtt`.

## License

MIT
