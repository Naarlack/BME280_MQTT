# BME280 MQTT transmitter

The hardware consists of a BME280 sensor attached to a WEMOS D1 mini Pro.

The software is intended to collect environment data from the BME280 at a set frequency and pass it back to a central server via MQTT.

To-do:
* Add WifiManager functionality so wifi credentials can be added over the air
* Update MQTT topic structure:
    * root/stem/BME280/data -> for sending data from the BME280
    * root/stem/BME280/cmd  -> for sending and recieving commands
* Add JSON functionality to the 'root/stem/BME280/data' topic so payloads can be more concise:
    * {temperature: X, humidity: Y, pressure: Z}
* Add ability to set/change functionality via the 'root/stem/BME280/data' topic:
    * location  -> change the 'root/stem' location
    * voltage   -> get the voltage (for units being powered by battery)
    * identify  -> flash an LED so unit can be identified
    * frequency -> set the frequency at which data is broadcast
    * ip        -> get the ip address of the unit