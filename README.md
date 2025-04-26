
# WiFi Honeypot with ESP8266 (Fake AP + Captive Portal)

## Objective
Create a fake WiFi access point that lures nearby devices to connect, and optionally serve a captive portal to simulate login behavior. This is an educational project for studying wireless security, phishing techniques, and awareness of rogue access points.

## Hardware
- ESP8266 NodeMCU Devboard (FlipperZero-compatible)
- Micro-USB or USB-C cable
- No FlipperZero required

## Tools & Firmware
- Arduino IDE or ESPHome Flasher
- Web browser for management interface
- Firmware used: [Deauther by Spacehuhn](https://github.com/SpacehuhnTech/esp8266_deauther)

## Features Used
- Fake Access Point broadcasting custom SSID
- Captive portal with a warning banner (educational simulation)
- Logs client MAC addresses and probe requests
- Isolated lab testing environment

## Lab Setup
| Component        | Role                |
|------------------|---------------------|
| ESP8266 Devboard | Fake AP + Portal    |
| Test Device      | Connects to fake AP |
| Host Machine     | Monitors via Web UI |

## Steps Performed
1. **Flashed Firmware to ESP8266**
2. **Connected to ESP8266 WiFi**
3. **Enabled FakeAP Mode**
4. **Tested with Phone**
5. **Modified Captive Portal Page**

## Observations
- Most modern phones auto-connect if previously joined open networks
- Some clients fall back to cellular data instead of opening captive portal
- Captive portal does not function on HTTPS-only devices (expected)
- MAC addresses can be logged unless client uses MAC randomization

## Ethics & Safety
- **Only used in isolated lab network**
- **No credential harvesting or malicious intent**

## Next Steps
- Customize captive portal with custom branding or banners
- Capture probe requests passively in a log
- Add logging endpoint for form submission (non-malicious use only)

## Notes
This project deepens understanding of **rogue APs, client behavior, and wireless phishing simulations**, tying in with Security+ topics like social engineering, network security, and secure wireless design.
