# IoT-Projects-Ecosystem
Description of the architecture, components, microservices, reverse proxy and IoT devices that integrate the IoT ecosystem.

## IoT Devive

Raspberry Pi Pico 2W connected to the local Wi-Fi that sends MQTT messages using SSL to a private broker running in the VPS. Publishes measured temperature and humidity.

## MQTT Broker

Mosquitto installed using user, password and SSL. Running in docker container.

## Python client in Docker

App running coroutines. Subscribes to two topics and publishes counter. Used for practicing logging, coroutines and aiomqtt.

## Grafana dashboard

Used for viewing temperature and humidity measured and sent by the Raspberry Pi Pico.

## FastAPI API

WIP. Will be used for getting measurements.

## Telegram Bot

Used for controlling Raspberry Pi Pico thermostat. WIP: get measurements.

## Flask App

Used for sending blink and setpoint MQTT messages to broker, for controlling the Rpi Pico thermostat.

## Node-RED

WIP. Used for controlling the Rpi Pico's LED, checking it's state (ON or OFF) and seeing latest measured temperature and humidity.
