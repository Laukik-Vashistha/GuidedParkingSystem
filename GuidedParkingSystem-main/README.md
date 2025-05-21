# GuidedParkingSystem
This repository contains the code developed for a research paper on developing a smart guided parking system. The system comprises two main components: a physical sensor network for detecting spot occupancy and a Python-based user web application.

## Research Paper
The research paper corresponding to this code is published in the Future Science Leaders [e-STEAMED journal](https://futurescienceleaders.com/blog/2024/06/developing-a-smart-guided-parking-system/).

### Abstract
Parking congestion in urban areas is a persistent issue that contributes to environmental, physical, and mental problems. This study built a two-part guided parking system to optimize the spot-finding process. The first part was a sensor network for detecting spot occupancy. The second part was a Python user interface that produced and launched the visuals of the parking lot statuses and an optimal parking path on an interactive webtool. The two components were bridged by Arduino IoT Things that acted as real time databases, receiving status information from sensors and syncing it to the user end. The system was functional and accurate in all scenarios, though the updating speed appeared to increase as more spot statuses were changed. Establishing a batch update approach, enhancing the path finding algorithm, creating a spot assignment feature, and exploring the use of more weather-resilient sensors were areas for future studies. 

## Repository Structure 
- ArduinoCloudSketch: Contains Arduino code for the MKR1000 WiFi board. This code is responsible for establishing connections to five ultrasonic sensors, reading occupancy data, and updating a cloud-based Arduino Thing database.
  - SpotStatus.ino: Arduino sketch code for communicating with sensors and updating cloud variables.
  - arduino_secrets.h: File containing WiFi SSID and password.
  - sketch.json: Information file.
  - thingProperties.h: Header file for Arduino cloud connection.

- TestingFiles: Includes bits of code used for testing individual parts of the system.
  - sensorNetwork: Arduino code for testing sensor network readings; useful for checking sensor functionality and circuit connections.
  - CloudConnection.py: Python code to connect to Arduino Cloud.
  - DrawLot.py: Python code for generating visuals of the parking lot.

- UserEnd.py: Python code for the user interface. It is responsible for connecting to Arduino Cloud, visualizing the parking lot statuses and an optimal path, and launching the visuals on an interactive web tool.

## Dependencies
To install the required dependencies, run the following command:
```
pip install arduino-iot-cloud
pip install swig
pip install nest_asyncio
pip install dash
pip install dash-html-components
pip install dash-core-components
pip install plotly
pip install matplotlib
pip install numpy
```
## License
This project is licensed under the MIT License. 
