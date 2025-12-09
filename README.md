# GyroBridgeReceiver

GyroBridgeReceiver lets you send **controller and gyro data from iOS** to a **Windows PC** over UDP.  
It uses the [ViGEmBus driver](https://github.com/nefarius/ViGEmBus/releases) to emulate a virtual Xbox 360 controller, so your iOS device can act as a gamepad in Windows games. The iOS device runs the companion app GyroBridge to send gyro and phone-controller data (like Backbone One).

## Download
- Get the latest release from the [Releases](https://github.com/knackepizza/GyroBridgeReceiver/releases) page.
- Download the `GyroBridgeReceiver.exe` file and place it anywhere on your Windows PC.

## Requirements
- **Windows 10/11** (x64 recommended).
- **ViGEmBus driver** installed (required for virtual controller emulation).
- **GyroBridge** the iOS client app that sends the data (will be released on App Store soon)

## Installation
1. Install the **ViGEmBus driver**:
   - Download from the official [ViGEmBus GitHub](https://github.com/nefarius/ViGEmBus/releases).
   - Run the installer and reboot if prompted.
2. Download the GyroBridgeReceiver `.exe` from Releases.
3. Run the `.exe` — no extra setup required.

## Usage
1. Launch `GyroBridgeReceiver.exe`.
2. On your iOS device, open GyroBridge, connect to the Local IP of your Windows PC on the same WiFi.
3. Once connected, a **virtual Xbox 360 controller** will appear in Windows.
4. Start your game — it should recognize the controller automatically.

## Troubleshooting
- **Program closes immediately with error:**
  ```cmd
  VIGEM_ERROR_BUS_NOT_FOUND
  Failed to execute script 'GyroBridgeReceiver' due to unhandled exception!
  ```
  This means the **ViGEmBus driver is missing**. Install it from the [ViGEmBus GitHub](https://github.com/nefarius/ViGEmBus/releases).

- **No controller appears in Windows:** \
Ensure ViGEmBus driver is installed and active. \
Check firewall settings (UDP packets must reach the PC). \
Verify the iOS client is sending data to the correct IP/port.

- **Still failing after retries:** \
Run the program as Administrator.
Reinstall the ViGEmBus driver.

## Credits
- [ViGEmBus](https://github.com/nefarius/ViGEmBus) for virtual gamepad emulation.
- Community libraries and tools that made this project possible.

