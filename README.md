# BME280 MQTT transmitter

The hardware consists of a BME280 sensor attached to a WEMOS D1 mini Pro.

The software is intended to collect environment data from the BME280 at a set period and pass it back to a central server via MQTT.

To-do:

Add WifiManager functionality so wifi credentials can be added over the air.
Add JSON functionality so MQTT payloads can be more concise.
Add ability to set/change MQTT topic over the air