# 2JCIE-BU01 Sensor Flow

A sensor flow to read readings from environmental sensor - OMRON [2JCIE-BU01](https://www.omron.co.jp/ecb/product-detail?partNumber=2JCIE-BU). 

**CAUTION**

* Only USB connection is supported as of now. BLE has not been supported yet.

## Usage

1. Import [candy-rad_2jcie-bu01.json](./candy-rad_2jcie-bu01.json) and deploy it.
1. It might be required to modify the serial port setting in the serial in/out node, if the device file assigned to 2JCIE-BU01 is not `/dev/ttyUSB0`.
1. Call web api `http://localhost:8100/api/2jciebu` with GET method to get latest readings.

## Specitication

* Read a value from 2JCIE-BU01 every 10 sec.
* `http://localhost:8100/api/2jciebu` returns mean, max and min value during last 10 min as below.

```
{
  "temperature": {
    "mean": 23.21,
    "max": 23.41,
    "min": 23.02
  },
  "humidity": {
    "mean": 63.45,
    "max": 64.18,
    "min": 62.66
  },
  "barometricPressure": {
    "mean": 1014.97,
    "max": 1015.106,
    "min": 1014.802
  },
  "illuminance": {
    "mean": 97,
    "max": 97,
    "min": 97
  },
  "soundNoise": {
    "mean": 44,
    "max": 75.73,
    "min": 33.19
  },
  "etvoc": {
    "mean": 46.2,
    "max": 54,
    "min": 38
  },
  "eco2": {
    "mean": 705.98,
    "max": 757,
    "min": 652
  },
  "discomfortIndex": {
    "mean": 70.61,
    "max": 70.82,
    "min": 70.39
  },
  "heatStroke": {
    "mean": 21.4,
    "max": 21.52,
    "min": 21.3
  },
  "spectralIntensity": {
    "mean": 0,
    "max": 0,
    "min": 0
  },
  "seismicIntensity": {
    "mean": 0,
    "max": 0,
    "min": 0
  },
  "sensorCode": "2JCIE-BU01"
}
```

* Supported senseor fucntions
  * temperature (℃)
  * humidity (%)
  * barometric pressure (hPa)
  * illuminance (lux)
  * sound noise (dB)
  * etvoc (ppb)
  * eco2 (ppm)
  * discomfort index (DI)
  * heat stroke (℃)
  * spectral intensity
  * seismic intensity
