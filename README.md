# ESP-IDF Wi-Fi Provisioning AP Example

This example demonstrates the usage of `wifi_provisioning` manager component for building a provisioning application. This takes the `wifi_prov_mgr` example from ESP-IDF and triggger the provisioning using a button. Also, the QR for provisionig has been deleted.

In the provisioning process the device is configured as a Wi-Fi station with specified credentials. Once configured, the device will retain the Wi-Fi configuration, until a flash erase is performed.

`wifi_prov_mgr` uses the following components :
* `wifi_provisioning` : provides manager, data structures and protocomm endpoint handlers for Wi-Fi configuration
* `protocomm` : for protocol based communication and secure session establishment
* `protobuf` : Google's protocol buffer library for serialization of protocomm data structures

This example can be used, as it is, for adding a provisioning service to any application intended for IoT.

## How to use example

### Hardware Required

Example should be able to run on any commonly available ESP32/ESP32-S2 development board.

### Application Required

Provisioning applications are available for various platforms. See below

#### Platform : Android

For Android, a provisioning application along with source code is available on GitHub : [esp-idf-provisioning-android](https://github.com/espressif/esp-idf-provisioning-android)

#### Platform : iOS

For iOS, a provisioning application along with source code is available on GitHub : [esp-idf-provisioning-ios](https://github.com/espressif/esp-idf-provisioning-ios)

#### Platform : Linux / Windows / macOS

To install the dependency packages needed, please refer to the top level [README file](../../README.md#running-test-python-script-ttfw).

`esp_prov` supports BLE and SoftAP transport for Linux, MacOS and Windows platforms. For BLE, however, if dependencies are not met, the script falls back to console mode and requires another application through which the communication can take place. The `esp_prov` console will guide you through the provisioning process of locating the correct BLE GATT services and characteristics, the values to write, and input read values.

### Configure the project

```
idf.py menuconfig
```

### Build and Flash

Build the project and flash it to the board, then run monitor tool to view serial output:

```
idf.py -p PORT flash monitor
```

(To exit the serial monitor, type ``Ctrl-]``.)

See the Getting Started Guide for full steps to configure and use ESP-IDF to build projects.


## Log

* Last compile: 07 December 2023.
* Last test: 07 December 2023.
* Last compile espidf version: `v 5.1.1`.
* VSCode ESP-IDF Visual Studio Code Extension `v 1.6.5`.


## License

Apache License, Version 2.0, January 2004.

## Version

`v 0.1.0`

