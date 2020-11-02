# candy-iot-practice

Snippets to connect a sensor to a cloud platform using CANDY LINE products.

Almost snippets are written in the Node-RED flow editor, and these are called 'flow'. Flows fall into two categories. One is a sensor flow which collects readings from a sensor. Another is a cloud flow which uploads values to a cloud platform.

## System Requirements

Belows are required as a edge gateway.

* Raspberry Pi
* CANDY Pi Lite or Lite+
* AC adapter (5V4A)
* microSD (16GB or larger is recommended)
* nanoSIM

It is recommended to use CANDY Pi Lite and CANDY RED provided by [CANDY LINE Inc.](https://www.candy-line.io/).

CANDY Pi Lite is a communication board for Raspberry Pi and ASUS Thinker Board. It enables you to connect to the Internet via carrier line like LTE, LTE-M, and so on. CANDY RED is a Node-RED based development environment and runtime environment which works on a single board computer. Some nodes for connecting to sensors and useful utility nodes are preinstalled so that users can develop IoT edge applications easily.

Please visit a product's web site (http://candy-line.com) for more details.

If you would like to use snippets in this repository without CANDY Pi Lite and CANDY RED, it is possible, but you may need to customize your OS images and install some nodes to your Node-RED environment.

For supported sensors and cloud platforms, please refer to the individual pages.

## Sensors

| Type | Vendor | Production Code | Notes |
| :--- | :----- | :--- | :-- |
| Environment | OMRON | [2JCIE-BU01](./src/sensor/2jcie-bu01) | |

## Cloud Platforms and Sensors

| Platform | Vendor | Sensor | Notes |
| :--- | :----- | :--- | :-- |
| MindSphere | Siemens | [2JCIE-BU01](./src/cloud/mindsphere/2jcie-bu01) | |

## Revision History

| Rev. | Date | Description |
| :--- | :----- | :--- |
| 0.0.1 | November 2, 2020 | DRAFT release |


