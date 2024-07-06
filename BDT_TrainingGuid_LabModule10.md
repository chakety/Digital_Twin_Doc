# Lab Module 10 - Final Project - Training Guide


## Final Project Description

### What is this? 
The Digital Twin Application (DTA) developed using Unity creates a virtual replica of a real-world system that manages and monitors the performance of five distinct assets collecting data from an Edge Device App (EDA). These assets gather real-time data on temperature, humidity, and wind power generation storage. The application enables visualization and analysis of this data to support decision-making processes in maintenance and operations.

The primary use case of this application is to predict maintenance needs based on the data processed within the DTA. It employs predictive analytics to forecast when components might fail or require replacement due to performance degradation. This is visually represented in the app as a warning notification, alerting operators to upcoming maintenance needs within a specified timeframe, enhancing proactive maintenance strategies.


### Why - Who Cares? 

I am passionate about this problem because single data points presented as mere numbers often fail to convey the urgency or significance behind them. By transforming this data into color-coded visual cues within the digital twin environment, we tap into a more intuitive understanding. Colors engage more than just the sense of sight; they evoke emotions and associations that numbers alone may not. For instance, red can be associated with heat or warnings, prompting immediate attention and action, while blue might be linked to water or cooler conditions.


For many, especially those in operational or monitoring roles, rapid and clear communication of information is critical. Color coding enhances data readability and urgency, making it far more likely for users to notice and react appropriately to changes or anomalies. This method of data representation can lead to quicker decision-making and more effective problem-solving in environments where time and accuracy are of the essence, such as in industrial settings. By integrating sensory engagement into data analysis, the application ensures that critical information is not just presented, but also perceived and acted upon effectively.



### How - About your Design and Implementation

#### Summary

The system architecture comprises three interconnected components, each critical to the overall functionality and flow of data:

1. Edge Device Side: This component features various sensors that collect essential data types. The sensors are strategically positioned to monitor specific environmental and operational parameters.
2. MQTT Broker: As the central communication hub, the MQTT broker is crucial for the seamless transmission of data between the edge devices and the digital twin application. It ensures that data collected from the physical environment is accurately and efficiently relayed to the digital twin, facilitating real-time updates and interactions.
3. Digital Twin Application: This is where the visualization and interaction with the collected data occur. The application houses the digital representations of the assets—two thermostats for temperature data, two wind turbines for monitoring wind power storage, and one humidity sensor. Once data is received from the edge devices via the MQTT broker, it is processed by the Digital Twin Application, which then updates the virtual assets accordingly. Each asset is visually represented in a way that changes color based on the data it receives; for example, temperature extremes might change the color of the thermostat assets, and variations in power storage levels detected by the wind turbines could be visualized with different hues. This visual coding helps users immediately grasp the status and needs of each asset without delving into complex datasets.


This configuration not only ensures a reliable and continuous data flow but also utilizes visual cues to simplify the interpretation of data, enhancing user engagement and decision-making efficiency within the virtual environment.


#### System Diagram
![alt text](<DTA system-1.png>)


#### How is Data Generated?

All the data is generated from simulation data, it is positive float value and did not exceeed float size. 



#### How are Commands Processed?

Commands are processed seamlessly between the assets and their corresponding edge devices, which share the same device ID for straightforward communication. The format for commands is "deviceID/actuatorCommand", making it clear which device is being controlled and what action is required.



EOF.
