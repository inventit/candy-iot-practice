# c+ Studio - 2JICE-BU01 cloud flow

A cloud flow to upload readings read from 2JCIE-BU01.

## Usage

1. Create a data adapter at c+ Studio.
1. Import [candy-red_cplus_2jcie-bu01.json](./candy-red_cplus_2jcie-bu01.json) to CANDY RED and deploy it.
1. Import [candy-red_cplus_config.json](../common/candy-red_cplus_config.json) to CANDY RED and deploy it.
1. Access to CANDY RED dashboard and configure settings.
1. Readings will be uploaded soon. Happy to enjoy creating dashboards.

## Specification

* Retrieve sensor values from the 2JCIE-BU01 sensor flow every 10 minutes, which contains a mean of the last 10 minutes.
* Upload mean, max, and min values to c+ Studio.
  * value01: mean
  * value02: max
  * value03: min
