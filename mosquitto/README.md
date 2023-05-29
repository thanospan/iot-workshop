# [Mosquitto](https://mosquitto.org/)

## Usage
- Run the containers:
```
cd /path/to/iot-workshop/mosquitto
docker compose up -d
```

- The Mosquitto MQTT broker is running at `localhost:1883`

  Note: When referencing the MQTT broker from another Docker container running on a different Docker network (e.g., Node-RED), the host machine's IP address should be used instead of `localhost`.

- Test using Docker:
  - Open a terminal and run an MQTT subscriber:
  ```
  docker run -it --rm --network="mosquitto" eclipse-mosquitto:2.0.15 mosquitto_sub -h mosquitto -p 1883 -t "#"
  ```
  - Open another terminal and run an MQTT publisher:
  ```
  docker run -it --rm --network="mosquitto" eclipse-mosquitto:2.0.15 mosquitto_pub -h mosquitto -p 1883 -t hello -m "Hello, World!"
  ```

- Test using Node-RED:
  - Open [Node-RED](http://localhost:1880) and [import](https://nodered.org/docs/user-guide/editor/workspace/import-export) the [provided MQTT example flow](https://github.com/thanospan/iot-workshop/blob/main/node-red/flows.json).
  
    Note: If the MQTT nodes do not connect to the MQTT broker, change the MQTT broker's address from `host.docker.internal` to the host machine's IP.

- Test using Python:
  - Requirements: [Python](https://www.python.org/), [Paho MQTT Python](https://github.com/eclipse/paho.mqtt.python)
  - An MQTT subscriber script is provided [here](https://github.com/thanospan/iot-workshop/blob/main/mosquitto/subscribe.py).
  - An MQTT publisher script is provided [here](https://github.com/thanospan/iot-workshop/blob/main/mosquitto/publish.py).
  - More examples can be found [here](https://github.com/eclipse/paho.mqtt.python/tree/master/examples).

## Resources
MQTT client libraries for various programming languages can be found [here](https://mqtt.org/software/).
