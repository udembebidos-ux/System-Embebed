# 🤖 Autonomous Robot Car - Embedded Systems

An autonomous robot car project developed for the Embedded Systems course, implemented using Raspberry Pi Pico 2W and MicroPython.

## 📋 Overview

This project involves the design and development of a robot car capable of autonomous navigation, obstacle avoidance, and remote control via WiFi. The system integrates sensors, actuators, and embedded control algorithms on the Raspberry Pi Pico 2W microcontroller.

## ✨ Features

- **Autonomous navigation**: Real-time obstacle detection and avoidance
- **Remote control**: WiFi interface for manual commands
- **Integrated sensors**: Ultrasonic, infrared, and line-following capabilities
- **Intelligent mode**: Potential integration with AI/TinyML for pattern recognition
- **Low power consumption**: Optimized for battery operation
- **Modular architecture**: Easy to extend and customize

## 🛠️ Hardware Requirements

### Core Components
- 1x Raspberry Pi Pico 2W
- 1x Robot car chassis with 2-4 wheels
- 2x DC motors with gearboxes
- 1x Motor driver (L298N or equivalent)
- 1x HC-SR04 ultrasonic sensor module
- 2-3x Infrared sensors (for line following)
- 1x Battery pack (7.4V recommended)
- 1x 5V voltage regulator
- Jumper wires, breadboard, and connectors

### Optional Components
- Servo motor for sensor mounting
- Status indicator LEDs
- Buzzer for audio feedback
- Speed sensors (rotary encoders)
- IMU module (accelerometer/gyroscope)

## 📁 Project Structure
├── 📄 main.py # Main entry point
├── 📂 core/ # Core system code
│ ├── motor_control.py # Motor driver interface
│ ├── sensors.py # Sensor management
│ └── navigation.py # Navigation algorithms
├── 📂 wifi/ # Wireless connectivity
│ ├── server.py # Web server
│ └── api.py # API endpoints
├── 📂 bluetooth/ # Bluetooth connectivity
├── 📂 ai/ # AI components (optional)
│ └── tinyml_model.py # TinyML inference
├── 📂 utils/ # Utility functions
│ ├── config.py # Configuration settings
│ └── helpers.py # Helper functions
├── 📂 docs/ # Additional documentation
│ ├── hardware_setup.md # Hardware assembly guide
│ ├── api_reference.md # API documentation
│ └── troubleshooting.md # Common issues and solutions
├── 📄 requirements.txt # Dependencies
├── 📄 CHANGELOG.md # Updates
└── 📄 README.md # This file


## 🚀 Getting Started

### Installation
1. Clone this repository
2. Upload the project files to your Raspberry Pi Pico 2W
3. Configure WiFi credentials in `config.py`
4. Run `main.py` to start the robot

## 🔧 Configuration

Edit the `utils/config.py` file to customize:
- WiFi SSID and password
- Motor pin assignments
- Sensor thresholds
- Operating modes

## 👥 Project Information

**Course**: Embedded Systems  
**Institution**: Universidad Distrital Francisco José de Caldas  
**Semester**: 2026-1  
**Development Platform**: Raspberry Pi Pico 2W  
**Programming Language**: MicroPython

## 📖 Documentation

For detailed documentation, please refer to the `docs/` directory:
- Hardware assembly and wiring diagrams
- API reference for remote control
- Troubleshooting guide
- Development guidelines

## 🤝 Contributing

This is an educational project. Contributions, suggestions, and improvements are welcome for learning purposes.

## 📝 License

This project is open-source under the MIT License for educational purposes.

---

**Note**: This project is designed as a learning platform for embedded systems concepts including real-time control, sensor integration, wireless communication, and autonomous behavior.
