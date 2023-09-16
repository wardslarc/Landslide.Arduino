# Fuzzy Inference System for Landslide Detection using Arduino Uno

## Overview
This code represents a Fuzzy Inference System (FIS) implemented in C/C++ for landslide detection using an Arduino Uno. Fuzzy Logic is a mathematical approach used to deal with uncertainty and imprecision in decision-making processes. In this particular FIS, it is designed to evaluate input values from various sensors and provide a landslide hazard rating as an output.

## Code Structure
The code consists of several sections, each serving a specific purpose:

1. **Constants and Definitions**: This section defines various constants, such as data types (`FIS_TYPE`), resolution, and input/output ranges. It also defines function pointer types for the membership functions and array operations used in the FIS.

2. **Sensor Inputs**: Declarations and initialization for various sensors, including a soil moisture sensor, an accelerometer, and a raindrop sensor.

3. **FIS Input and Output**: Declaration of arrays to store FIS input and output values.

4. **Setup Routine**: The `setup` function initializes the serial communication, sets pin modes for sensors, and checks for the presence of an ADXL345 accelerometer sensor.

5. **Loop Routine**: The `loop` function continuously reads sensor values, processes them, and evaluates the FIS to provide a landslide hazard rating as output. It also prints sensor readings and the output rating to the serial monitor.

6. **Support Functions for Fuzzy Inference System**: This section includes functions for membership functions (e.g., triangular), array operations (e.g., min and max), and other utility functions required for fuzzy inference.

7. **Data for Fuzzy Inference System**: Definitions of membership functions, rule weights, rule types, rule inputs, and rule outputs used in the FIS.

8. **Data-dependent Support Functions**: Functions that depend on the data defined in the previous section, such as calculating the centroid of the fuzzy output.

9. **Fuzzy Inference System**: The `fis_evaluate` function represents the core of the FIS. It transforms input data into fuzzy input, applies fuzzy logic rules, and calculates the fuzzy output. The fuzzy logic rules and their associated weights are defined earlier in the code.

## How to Use
To use this code for landslide detection with an Arduino Uno, follow these steps:

1. Connect the required sensors to the designated pins (e.g., soil moisture sensor to `A0`, accelerometer sensor).

2. Upload the code to your Arduino Uno using the Arduino IDE.

3. Open the serial monitor in the Arduino IDE to view the sensor readings and the calculated landslide hazard rating.

4. Adjust the fuzzy logic rules, membership functions, and sensor input processing as needed for your specific application or sensor setup.
