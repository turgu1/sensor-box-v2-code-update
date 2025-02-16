# My Sensor Box V2 Software Updates

Some updates to the SensorBox DIY project configuration file.

See [here](https://www.printables.com/model/1079858-3d-printer-emission-sensor-array-sensorbox-v2) for more info.

(2025-02-15)

- Code cleanup
- Added Pressure from bmp280
- Double-Click page selection
- Added two template sensors (temperature, humidity)
  - Selection code for the sensor to use is now in those sensors.
- Added two pages:
  - Graphics for the last hour (temperature, humidity, pressure, CO2, VOC)
  - Graphics for the last 24 hours
- Added `secrets.yaml` support. Please use the `secrets.yaml.example`, rename it and update it with your values.

ToDo:
- [x] Add button double-click 
- [x] Add a graphics page
- [ ] MQTT support
- [x] Add secrets.yaml support