# PCB_DESIGN_ROADQUALITYINDEXER
## 🔍 Interactive PCB Viewer
[Click here to view the Interactive BOM](https:https://htmlpreview.github.io/?https://github.com/prasannakumar160/PCB_DESIGN_ROADQUALITYINDEXER/blob/main/ibom.html)


Problem Statement

For my honors, NodeMCU was used along with the NEO-6M GPS module and the BNO085 IMU sensor to analyze and index road quality for two-wheelers.
During development, the need arose to integrate additional sensors into the system.
A major limitation was identified — the NodeMCU has only one I²C bus, which was already used by the IMU sensor.
The NodeMCU also uses a micro USB-B interface, which is outdated compared to modern USB-C standards.
These issues made the system less scalable, less efficient, and unsuitable for modern hardware expansion.

Solution
A custom novel PCB was designed to integrate both the IMU and GPS modules into a single compact board.
An I²C bus multiplexer was added to overcome the limitation of a single I²C bus.
The micro USB-B connector was replaced with a USB-C port for improved connectivity and durability.
The redesign allows for multiple sensor connections without communication conflicts.
Overall, the PCB became more efficient, scalable, compact, and future-ready.

Components Used in the Circuit
NodeMCU: Acts as the main controller, handling sensor data processing and wireless communication.
GPS Module (NEO-8M): Provides accurate real-time location data for mapping road quality.
IMU Sensor (BNO055): Measures acceleration and orientation to detect road surface irregularities.
I²C Bus Multiplexer: Expands the single I²C bus, allowing multiple sensors to connect simultaneously.
USB-C Port: Replaces the outdated micro USB-B, offering faster, more durable, and reversible connectivity.
Voltage Regulator: Converts the 5V output from the USB-C port to 3V required by the components.

Purpose of the PCB:
To create an integrated and compact hardware solution for indexing and analyzing road quality in two-wheelers.
To combine the NodeMCU, GPS (NEO-8M), and IMU (BNO055) sensors on a single PCB.
To include an I²C bus multiplexer for supporting multiple additional sensors.
To incorporate a USB-C port for modern, durable, and reversible connectivity.
To include a voltage regulator for stable power management across all components.
To eliminate wiring complexity, enhance reliability, and reduce overall system size.
To enable efficient data acquisition for real-time road condition monitoring.

SCHEMATICS:
The image shows the schematic I designed for the PCB (PVB).
This PCB was custom-designed by me since it is not available in the market.
Connections are established from the USB-C port to a voltage regulator, as the NodeMCU, GPS, and IMU require 3.3V, while the USB-C provides 5V output.
The TX and RX pins of the NodeMCU are connected to the GPS module.
The I2C pins of the NodeMCU are connected to the I2C bus.
From the I2C bus, one set of SCL (SC1) and SDA (SD1) lines are connected to the IMU.
The remaining pins of the I2C bus are extended to connectors for external/additional sensors along with GPIO Pins from NODEMCU
