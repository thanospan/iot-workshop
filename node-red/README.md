# [Node-RED](https://nodered.org/)

## Usage
- Run the containers:
```
cd /path/to/iot-workshop/node-red
docker compose up -d
```

- Node-RED is running at http://localhost:1880/

  Note: When referencing Node-RED from another Docker container running on a different Docker network, the host machine's IP address should be used instead of `localhost`.

- [Import](https://nodered.org/docs/user-guide/editor/workspace/import-export) the [provided flows](https://github.com/thanospan/iot-workshop/blob/main/node-red/flows.json).
