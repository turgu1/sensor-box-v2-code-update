# My Sensor Box V2 Software Updates

Some updates to the SensorBox DIY project configuration file.

See [here](https://www.printables.com/model/1079858-3d-printer-emission-sensor-array-sensorbox-v2) for more info.

(2025-02-15)

### Code cleanup

The lambda code has been reformatted to be in line with C / C++ usage

### Button clics management and Pages selection

A new click has been added to permit page selection. There is now 3 clicks durations:

- Short click: Between 10 and 350ms: page selection
- Medium click: Between 750ms and 3 sec.: Screen dimming selection
- Long click: Between 5 sec. and 15 sec.: Wifi AP Mode

There is 3 pages available to access in sequence through a short click:

- The Sensors page (as per the original software)
- Graphics for the last hour (temperature, humidity, pressure, CO2, VOC)
- Graphics for the last 24 hours

### Added Pressure of bmp280

The bmp280 pressure sensor has been added on the top line of the first page. See pictures below.

### Graphics support

To permit proper access to the temperature and humidity sensors by the graph add-on, two template sensors have been added. The lambda producing those sensors' state are now responsible of selecting the first sensor that returns a valid value. The firs page is now using those sensors to diaplay the current temperature and level of relative humidity.

### secrets.yaml

Added `secrets.yaml` support. Please use the `secrets.yaml.example`, copy it to secrets.yaml and update it with your values.

### Pictures

Here are some pictures showing the current 3 pages displayed by the SensorBox:

</br></br>
<img src="./pictures/Page1.jpg" width="150" title="Page 1"/>&nbsp;<img src="./pictures/Page2.jpg" width="150" title="Page 2"/>&nbsp;<img src="./pictures/Page3.jpg" width="150" title="Page 3"/>
</br></br>

### ToDo:

- [x] Add button double-click 
- [x] Add a graphics page
- [ ] MQTT support
- [x] Add secrets.yaml support