# LoRa Chat with RSSI-Based Distance Estimation

This Arduino sketch allows two LoRa-enabled devices to exchange messages over long distances. It also estimates the distance between devices using the signal strength (RSSI) of received messages.

## Features

- Two-way communication via LoRa
- Displays received messages on Serial Monitor
- Estimates distance based on RSSI
- Simple Serial input to send messages

## Hardware Requirements

- 2x Arduino boards (e.g., Uno, Nano, Mega)
- 2x LoRa modules (e.g., RFM95)
- Jumper wires
- Power supply (ensure 3.3V for LoRa module)

## Wiring Configuration

| LoRa Pin | Arduino Pin |
|----------|-------------|
| VCC      | 3.3V        |
| GND      | GND         |
| SCK      | 13          |
| MISO     | 12          |
| MOSI     | 11          |
| NSS/CS   | 8           |
| RST      | 4           |
| DIO0     | 7           |

> ⚠️ Note: LoRa modules operate at 3.3V. Supplying 5V may damage the module.

## Frequency Configuration

The frequency is set to:

```cpp
#define RF95_FREQ 951.0
