# c+ Studio - TR-76Ui cloud flow

A cloud flow to upload readings read from TR-76Ui.

## Usage

1. Create a data adapter at c+ Studio.
1. Import [candy-red_cplus_tr-76ui.json](./candy-red_cplus_tr-76ui.json) to CANDY RED and deploy it.
1. Import [candy-red_cplus_config.json](../common/candy-red_cplus_config.json) to CANDY RED and deploy it.
1. Access to CANDY RED dashboard and configure settings.
1. Readings will be uploaded soon. Happy to enjoy creating dashboards.

## Specification

* Retrieve sensor values from the TR-76Ui sensor flow every 10 minutes, which contains a mean of the last 10 minutes.
* Upload mean, max, and min values to c+ Studio.
  * value01: mean
  * value02: max
  * value03: min
