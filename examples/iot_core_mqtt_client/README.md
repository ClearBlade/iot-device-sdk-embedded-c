# MQTT client example

This example uses the ClearBlade Cloud IoT Device SDK for Embedded C to connect a native Linux application to the [ClearBlade Cloud IoT Core MQTT bridge](https://cloud.google.com/iot/docs/how-tos/mqtt-bridge#iot-core-mqtt-auth-run-cpp).

## Getting started

Before you begin, generate a [public/private key pair](https://cloud.google.com/iot/docs/how-tos/credentials/keys), store the private key in the `examples/iot_core_mqtt_client/bin` directory, and name the key `ec_private.pem`.

1. Run `make` in the repository's root directory.

2. Generate the native example application from the root directory.

```
cd examples/iot_core_mqtt_client \
make
```

3. Run the following commands, substituting your device and project information:

<pre>
make \
cd bin \
./iot_core_mqtt_client -p <i><b>PROJECT_ID</b></i> -d projects/<i><b>PROJECT_ID</b></i>/locations/<i><b>REGION</b></i>/registries/<i><b>REGISTRY_ID</b></i>/devices/<i><b>DEVICE_ID</b></i> -t /devices/<i><b>DEVICE_ID</b></i>/state
</pre>

You may optionally send messages, MQTT URLs, and ports with flags -u and -n, respectively. Example: -m something -u us-central1-mqtt.clearblade.com -n 8883
