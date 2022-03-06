# myDashBoard

My main motivation to start this personal project was to create a personalized dashboard for my own, using 3 Neopixel 8x8 matrixes controlled by a my-RIO board. As consequence of this main motivation, I created 2 APIs, the [myRIO-Neopixel](https://github.com/memosfet/myRIO-Neopixel) (for Neopixel manipulation) and the [OpenWeatherLabVIEW](https://github.com/memosfet/OpenWeatherLabVIEW) (for current weather queries). So this project is meant to test those APIs from a developer point of view.

## Features
* [ ] Display in Neopixel LED Matrix:
    * [x] Date & Time (In Progress)
    * [x] Audio Analyzer
    * [ ] Timer (In Progress)
    * [ ] Weather (In Progress)
* [ ] Publish local website:
    * [ ] Allow user to select the display mode

## Architecture

This project uses an ascyncronous architecture with the following processes:
* Central Message Handler - Central entity in charge to distribute commands between all processes.
* Audio Analyzer - Continously analyzes the audio input and publishes the FFT output.
* Draw Frame - Continously sends the raw data from the Neopixel API to the FPGA.
* Display Manager - Manages all the Neopixel display objects.
* Error Handling - Logs errors and is in charge of stopping all the processes in case of failure.
* Sequencer - Highest level process that defines the mode on which the whole application operates.

## LabVIEW Requirements

LabVIEW 2019 or older

LabVIEW RT

LabVIEW FPGA

[myRIO-Neopixel](https://github.com/memosfet/myRIO-Neopixel)

[OpenWeatherLabVIEW](https://github.com/memosfet/OpenWeatherLabVIEW)

[JKI HTTP REST API Client for LabVIEW](https://resources.jki.net/http-rest-api-client-for-labview)

## Hardware Requirements

NI my-RIO.

3 Neopixel Matrixes 8x8 Ws2812 5050.

Power Supply 12V 5A.

Buck converter LM2596HVS

Microphone

## Connections

(Work in progress)


## License

The myDashBoard is licensed under an MIT-style license (see LICENSE).