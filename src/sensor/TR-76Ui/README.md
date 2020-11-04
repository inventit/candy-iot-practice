# TR-76Ui Sensor Flow

A sensor flow to read readings from CO2, temperature and humidity data logger - TandR [TR-76Ui](https://shop.tandd.co.jp/products/TR-7_series/tr76ui.php). 

**CAUTION**

* Only USB connection is supported as of now.

## Usage

1. Import [candy-rad_tr-76ui.json](./candy-rad_2jcie-bu01.json) and deploy it.
1. It might be required to modify the serial port setting in the serial in/out node, if the device file assigned to 2JCIE-BU01 is not `/dev/ttyUSB0`.
1. Call web api `http://localhost:8100/api/tr76ui` with GET method to get latest readings.

## Specitication

* Read a value from TR-76Ui every 10 sec.
* `http://localhost:8100/api/tr76ui` returns mean, max and min value during last 10 min as below.

```
{
  "temperature": {
    "mean": 23.6,
    "max": 23.6,
    "min": 23.6
  },
  "humidity": {
    "mean": 39,
    "max": 39,
    "min": 39
  },
  "co2": {
    "mean": 1130,
    "max": 1130,
    "min": 1130
  },
  "timestamp": "Wed Nov 04 2020 10:46:56 GMT+0000 (Coordinated Universal Time)",
  "sensorCode": "TR-76Ui"
}
```

* Supported senseor fucntions
  * temperature (℃)
  * humidity (%)
  * co2 (ppm)
