# Vendor Tree for Realme N53 (RMX3761)

## Vendor Blobs Overview

This repository contains proprietary vendor files for the Realme N53 (RMX3761) required to build a custom ROM.

### Binary Organization

```bash
vendor/realme/RMX3761/
├── proprietary/
│   ├── bin/
│   ├── etc/
│   ├── firmware/
│   ├── lib/
│   └── lib64/
├── Android.bp
├── Android.mk
├── BoardConfigVendor.mk
└── device-vendor.mk
```

## Proprietary Blobs

### Key Components
- Camera Blobs (692 files)
- Audio HAL Implementation
- Graphics/GPU Drivers
- Sensor HAL
- Fingerprint HAL
- Wi-Fi/Bluetooth Firmware
- Thermal Engine Components

### Firmware Versions
- Baseband Version: RMX3761_11.A.31
- Vendor SPL: July 2023

## Extraction Information

### Source
- Stock ROM Version: RMX3761_11.A.31
- Android Version: 13
- Extraction Method: Non-root method using payload dumper

### Verified Compatibility
- Android 13 (Stock)
- Android 14 (Custom ROM)

## Implementation Details

### Hardware Support
- Full Camera Features
- Audio Processing
- GPU Acceleration
- Sensor Calibration
- Fingerprint Recognition
- Radio Interface Layer

### Known Issues
- None reported

## Usage Instructions

1. Clone this repository to `vendor/realme/RMX3761`
2. Include this vendor in device tree:
```makefile
$(call inherit-product, vendor/realme/RMX3761/device-vendor.mk)
```

## Vendor Specific Features

### Camera
- 50MP Main Sensor Support
- 2MP Depth Sensor
- 8MP Front Camera
- Portrait Mode Processing
- Night Mode Algorithm

### Display
- 90Hz Refresh Rate Support
- Dynamic Refresh Rate Switching
- Hardware Composer Implementation

### Audio
- Multiple Audio Scenarios
- Voice Processing
- Dirac Sound Enhancement

### Security
- Fingerprint Hardware Support
- TEE Implementation
- Keymaster Support

## Updating Vendor Files

To update vendor files:
1. Extract new blobs from updated firmware
2. Update proprietary-files.txt
3. Re-run setup-makefiles.sh

## Dependencies

- Device Tree: [device/realme/RMX3761](../../../device/realme/RMX3761)
- Kernel Source: [kernel/realme/RMX3761](../../../kernel/realme/RMX3761)

## Notes

- All blobs are compatible with Android 14
- Maintains original firmware signatures
- SELinux policies included

## License

```
Copyright (C) 2023 The LineageOS Project

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
```
