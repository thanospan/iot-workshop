# [FIWARE](https://www.fiware.org/)

## Usage
```
cd iot-workshop/fiware
docker compose up -d
```

- Orion-LD Context Broker: http://localhost:1026/ngsi-ld/v1/

  Note: When referencing from another Docker container running on a different Docker network (e.g., Node-RED), the host machine's IP address should be used instead of `localhost`.

- Interact with the Context Broker by sending HTTP requests according to the [NGSI-LD API](https://swagger.lab.fiware.org/?url=https://raw.githubusercontent.com/FIWARE/specifications/master/OpenAPI/ngsi-ld/full_api.json).

  A Postman collection is provided [here](https://github.com/thanospan/iot-workshop/blob/main/fiware/iot-workshop.postman_collection.json).

## Resources
Additional resources about the FIWARE ecosystem can be found [here](https://github.com/thanospan/iot-workshop/blob/main/fiware/resources.txt).
