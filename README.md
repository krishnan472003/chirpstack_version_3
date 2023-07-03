# CONNECTING LORAWAN DEVICES USING CHIRPSTACK VERSION 3
## requirements
* Kerlink gateway
* redis
* postgres
* mosquitto

## Architecture:

* Kerlink packet forwarder: sends data to chirpstack via UDP
* Chirpstack gateway bridge: sends data to network server via mqtt
* Chirpstack network server: receives data from network server and posts it to to application server
* Chirpstack application server: Published data to application server.

### kerlink packet forwarder
* https://www.youtube.com/watch?v=BGj3s8s2sF8&t=508s follow this video to setup the device gateway
* link for installation:  https://www.chirpstack.io/project/ for rest of the steps

### Things to consider:
* opening udp port 1700 for server to gateway in the server
* opening rest to the ports as tcp
* This is version three not version four
* configure the gateway to send data to the required server
