---
title: Astronaut AR Visualization Tool
project: ctsgc-ar-visualization
published: true
year: 2019
---

## About
This is a wearable system for quick visualization and diagnosis of issues in space using mixed reality technology. This project was completed as a part of a Faculty-Student Summer Research grant through the [Connecticut Space Grant Consortium](http://ctspacegrant.org/) and Central Connecticut State University. The Principle Investigator was Dr. Haoyu Wang. 

This research will contribute to NASA’s Human Exploration and Development of Space strategic enterprise. The goal of the research is to develop a wearable system based on mixed reality (augmented reality (AR) and virtual reality (VR)) to help human quickly visualize and diagnose issues in space vehicles or habitats. Two undergraduate students will design and prototype the system which integrates Microsoft Hololens (AR), HTC VIVE and MANUS VR (VR), and a computer through software development using their application programming interface (API).

### Honors
This project was presented at the 2019 Connectcut Space Grant Consortium Grants Expo.

### Design
Over the summer, we developed a proof-of-concept Augmented Reality system to aid in simple visualization and issue diagnosis for satellite repair.

I did preliminary research on the user interface to help us develop our goals and scope for this proof of concept. We were inspired by other developing AR tools that help their users access more information about what they see in front of them, such as [this construction tool](https://www.youtube.com/watch?v=tAmImhdWYjA) used in a construction site. We wanted to be able to visualize useful and relevant sensor information that could help with EVA repairs. In order to do this, we needed to create an application using the Microsoft Hololens and a test platform with sensors to use as our mock satellite.

I was primarily in charge of model satellite used for demo. I came up with a list of potential sensors that could stand in for actual sensors used on satellite systems, including battery voltage monitors and temperature sensors, voltage monitors for solar panel arrays, and an air tank with an internal pressure and temperature sensor. We also included three simple connectors that could represent something being unplugged. I drew a schematic in Autodesk EAGLE to finalize the sensor interface, along with a Bluetooth module used to transmit the data to the Hololens. 

Using Autodesk Inventor, I drew CAD models of the components of the miniature satellite for 3D printing. This included the main body, a box for 3 9V batteries, the solar panel wings, the slot for the air tank, and a panel to allow us to access the internal electronics. During this design I needed to think about where wiring would go and how we would interact with the satellite during build and final use. It took a few tries to get everything to fit but was ultimately successful. 

The main controller for this system was an Arduino Uno. I wrote the code that interfaced with each of the sensors: I2C for the temperature and pressure sensor, analong inputs for solar panel and battery voltage levels, Dallas one-wire interface for the battery temperature sensors, and digital inputs for the connections. All of this information was gathered in packets of data, and sent via UART to the HC-06 bluetooth module in CSV format. 

These packets were received with the Hololens Bluetooth module. I assisted Austin in the development and debugging of the Universal Windows Application. We experimented with Vuforia to use as a way to contextualize the information. By using visual cues like QR codes, the HoloLens software could identify what it's looking at and display the sensor information that matters. This is important for real world systems, that may have an overwhelming amount of data, which would be impractical to display all at once. In addition to this, we were able to have the app recognize the satellite and overlay the CAD model, another potentially useful feature. 


## Resources
- [CT Space Grant Award Announcement](http://ctspacegrant.org/6261/spring-2019-award-recipients)


## Media
{% include image-gallery.html folder="/assets/img/ctsgc-ar-visualization" %}

<div class="videos">
<iframe src="https://drive.google.com/file/d/0B_S9H2AY2UyESjJCbzB2MlJyUFFCcGZfSUhjeVh0Ql9XRUhN/preview" width="640" height="480"></iframe>
<iframe src="https://drive.google.com/file/d/1hsG-7OFaZ7a6wAcbC8UoxqRq8nXH-CYS/preview" width="640" height="480"></iframe>
<iframe src="https://drive.google.com/file/d/1gi7ZVDLinleVf_q4mEAnGIsIgdeeq1PR/preview" width="640" height="480"></iframe>
</div>