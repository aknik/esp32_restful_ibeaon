[![Build Status](https://travis-ci.org/ryanm101/esp32_restful_ibeaon.svg?branch=master)](https://travis-ci.org/ryanm101/esp32_restful_ibeaon)

ESP32 BLE ibeacon broadcaster & tracker
=======================================


Work in progress to implement an BLE sniffer sending packets through REST

Installation
------------

* Install ESP32 toolchain as described [here](https://esp-idf.readthedocs.io/en/v3.0-rc1/get-started/linux-setup.html). I currently use [1.22.0-75](https://dl.espressif.com/dl/xtensa-esp32-elf-linux64-1.22.0-75-gbaf03c2-5.2.0.tar.gz)
* Clone esp-idf and set its `IDF_PATH` environment variable. I use v3.0-rc1
* Run `make menuconfig`
  * `Network configuration` to configure WiFi, iBeaon & REST Server
  * `Component config`
    * `Bluetooth`->`Bluedroid Enable` to activate `GATT client module(GATTC)`


Objectives
----------

* (Partially Implemtented) Scan for BLE iBeacon (Search for ~500ms)
* (TODO) Report iBeacons Detected to HTTP Server via REST POST
          {[{'name': 'ibeaconA', 'uuid': '00000000-0000-0000-0000-000000000000', 'major': 0, 'minor': 0}]}
* (TODO) Broadcast iBeacon every ~500ms
* (TODO) ID if Broadcast & Search be done synchronously?
* (TODO) update OTA
* (TODO) SetConfig via txt / REST
