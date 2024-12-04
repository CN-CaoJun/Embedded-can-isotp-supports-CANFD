# Embedded-CAN-ISOTP

## Introduction

Embedded-CAN-ISOTP is an embedded implementation of the Transport protocol and network layer services. It is primarily designed for use with RTOS (Real-Time Operating Systems) and provides a portable layer for easy integration. The ISO-TP (ISO Transport Protocol) implemented in this project adheres to the ISO15765-2 standard, ensuring compatibility and standardization. Additionally, the project supports both CAN TP (Controller Area Network Transport Protocol) and CAN FD TP (Controller Area Network with Flexible Data-Rate Transport Protocol), catering to different communication requirements within automotive and embedded systems.

## Framework
### Project desin
The framework for implementing CAN TP (Controller Area Network Transport Protocol) in the Embedded-CAN-ISOTP project is structured as follows:
<div style="text-align: center;">
  <img src="./docs/cantp_framework.jpg">
</div>

- Application Layer: This layer is where the application interacts with the transport protocol. It is responsible for initiating and managing the communication sessions.
- Transport Layer: The ISO-TP (ISO Transport Protocol) is implemented at this layer. It adheres to the ISO15765-2 standard and provides the necessary transport services for CAN and CAN FD networks. Specific introduction please refer to [Introduction of CAN TP](./CAN_ISO15765.md)
- Portable Layer: This layer provides a set of APIs (Application Programming Interfaces) for the transport protocol. It includes functions for opening, reading, writing, and controlling the CAN hardware. This layer is designed to be portable across different RTOS (Real-Time Operating Systems) and MCU (Microcontroller Unit) platforms.
- CAN Hardware: This layer represents the physical CAN hardware, which is responsible for transmitting and receiving data over the CAN bus.
- Platform: This layer includes the RTOS (Real-Time Operating Systems) and MCU (Microcontroller Unit) platforms. The project supports various RTOS platforms such as FreeRTOS, ThreadX, and Zephyr.

### ISO design
<div style="text-align: center;">
  <img src="./docs/image.png">
</div>

## Reference opensource projects
This project is inspired by below projects.

1. **[openxc/isotp-c](https://github.com/openxc/isotp-c)** /**[lishen/isotp-c](https://github.com/lishen2/isotp-c)**
2. **[lishen/can-isotp](https://github.com/hartkopp/can-isotp)**
## Highlight Features
  - **ISO-TP (ISO Transport Protocol) Implementation**: This project implements the ISO15765-2 standard, ensuring compatibility and standardization.
  - **Support CAN and CAN FD**: The project not only supports traditional CAN TP, but also CAN FD TP to meet different communication needs.
  - **Portable layer**: Provides a set of APIs for easy porting and integration on different RTOS and MCU platforms.