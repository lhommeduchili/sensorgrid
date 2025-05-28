# sensorgrid
## Real-time temperature monitoring system with an ESP32 microcontroller and a Raspberry Pi computer.

Complete IoT system that reads temperature data from multiple DS18B20 sensors connected to an ESP32 HUZZAH32 Feather, transmits the data over Wi-Fi via MQTT, and visualizes it in real time on a web server hosted by a Raspberry Pi.

It is designed to learn and apply standard hardware/software interfacing practices, including MQTT communication, web development, and embedded systems programming.

--

### 🔧 Features
* 📡 ESP32 reads temperature from up to 5 DS18B20 sensors via OneWire.
* 🌐 Sends readings via MQTT to a local Mosquitto broker on the Raspberry Pi.
* 🧠 Python backend on the Pi subscribes to sensor data and forwards it to a Flask web server.
* 📊 Interactive real-time graphs powered by Plotly.js and Socket.IO.
* 🖥️ Web dashboard accessible locally or remotely (e.g., via ngrok or port forwarding).
* 💾 Easily extendable to include data logging, historical visualization, or remote control features.

--

### 📦 Tech Stack
#### Microcontroller (ESP32 HUZZAH32 Feather)
* C++ (Arduino framework)
* DS18B20 sensors (OneWire)
* PubSubClient (MQTT)

#### Server (Raspberry Pi)
* Python 3
* Mosquitto MQTT broker
* Flask + Flask-SocketIO
* Plotly.js (frontend visualization)
* Socket.IO (real-time updates)

--

### 🚀 Getting Started
1. Flash the ESP32 with the Arduino sketch to read and publish temperatures.
2. Set up the Raspberry Pi with Mosquitto, Flask, and SocketIO.
3. Run the MQTT listener and the Flask server.
4. Visit http://<raspberry-pi-ip>:5000 or your ngrok public URL.
