# ROii - Automotive TSN Network Designer 3D

🚗 **Zone-based Time-Sensitive Networking · 3D Visualization**

An interactive 3D web application for designing and visualizing automotive Time-Sensitive Networking (TSN) architectures using Microchip LAN9662/9692 zone controllers.

## 🌟 Features

### 🎨 3D Visualization
- **Interactive 3D Canvas**: Powered by Three.js for real-time rendering
- **Vehicle Model**: Pre-configured automotive sensor layout
- **Drag & Drop**: Intuitive device placement and movement
- **Auto Layout**: Intelligent zone-based positioning

### 🔷 Zone Controllers
- **LAN9662**: 4-port TSN switch (2× RJ45 + 2× SFP)
- **LAN9692**: 12-port TSN switch (7× MateNET T1 + 4× SFP+ 10G + 1× MGMT)

### 📡 Sensors & Devices
- **Cameras**: Front, rear, and side vision sensors
- **LiDAR**: 3D range sensor for autonomous driving
- **Radar**: Object detection and distance measurement
- **ECU**: Electronic Control Units for processing

### 🚗 Vehicle Scenario
Pre-configured automotive zone architecture with:
- Front cameras (left, center, right)
- Rear and side cameras
- Front and rear corner radars
- Side radars
- Roof-mounted LiDAR
- Multiple zone controllers
- ADAS and chassis ECUs

### ⚡ TSN Features
- IEEE 802.1Qbv (Time-Aware Shaper)
- IEEE 802.1Qav (Credit-Based Shaper)
- IEEE 802.1Qbu (Frame Preemption)
- IEEE 1588 PTP (Precision Time Protocol)

### 🎮 Interactive Controls
- **Select Mode**: Click to select, drag to move devices
- **Connect Mode**: Click devices to create network links
- **Auto Rotation**: Automatic camera rotation
- **Export**: Save network configuration as JSON

## 🚀 Live Demo

Visit the live application: **[https://hwkim3330.github.io/roii/](https://hwkim3330.github.io/roii/)**

## 📦 Quick Start

1. Clone the repository:
```bash
git clone https://github.com/hwkim3330/roii.git
cd roii
```

2. Open `index.html` in a modern web browser:
```bash
# Using Python
python3 -m http.server 8000

# Or just open directly
open index.html
```

3. Click **"🚗 Load Vehicle Scenario"** to load the pre-configured automotive layout

## 🎯 Usage

### Loading Vehicle Scenario
1. Click the **"🚗 Load Vehicle Scenario"** button in the header
2. A complete automotive TSN architecture will be loaded with:
   - Zone controllers positioned centrally
   - Sensors positioned around the vehicle
   - All connections pre-configured

### Adding Devices
- Click any device card in the left sidebar to add it to the canvas
- Devices are randomly positioned by default
- Use **Select Mode** to drag and reposition devices

### Creating Connections
1. Click **"Connect Mode"** in the tools section or use the 🔗 button
2. Click on the source device
3. Click on the target device to create a link
4. Exit connect mode by clicking **"Select Mode"**

### Device Properties
- Click any device in **Select Mode** to view its properties
- Configure port settings, VLAN, priority, and bandwidth
- Properties panel appears on the right side

### Auto Layout
- Click **"⚡ Auto Layout"** to automatically arrange devices in a zone-based topology
- Zone controllers are positioned centrally
- Sensors are arranged in an arc
- ECUs are positioned below

### Export Configuration
- Click **"📤 Export"** to download the current network configuration as JSON
- Configuration includes device positions, types, and connections

## 🏗️ Architecture

### Zone-based Architecture
The application follows automotive zone controller architecture:
- **Central Zone Controllers**: LAN9662/9692 switches at the core
- **Sensor Zones**: Cameras, radars, and LiDAR positioned around the vehicle
- **Processing Zones**: ECUs for ADAS and chassis control
- **Deterministic Networking**: TSN ensures real-time, low-latency communication

### Technology Stack
- **Three.js**: 3D graphics rendering
- **Vanilla JavaScript**: No frameworks, pure performance
- **WebGL**: Hardware-accelerated graphics
- **Canvas API**: Dynamic textures and labels

## 📊 Network Statistics

Real-time display of:
- **Devices**: Total number of devices in the network
- **Links**: Number of network connections
- **Bandwidth**: Aggregate network throughput

## 🎨 Visual Design

- **Dark Theme**: Modern dark UI with gradient backgrounds
- **Glassmorphism**: Translucent panels with backdrop blur
- **Neon Accents**: Blue gradient highlights for TSN theme
- **3D Shadows**: Realistic lighting and shadow effects

## 🖥️ Browser Compatibility

- Chrome/Edge 90+
- Firefox 88+
- Safari 14+
- Modern browsers with WebGL support

## 📝 Configuration File Format

```json
{
  "timestamp": "2025-10-16T07:40:00.000Z",
  "devices": [
    {
      "id": "device-1",
      "type": "lan9692",
      "label": "Front-ZC",
      "position": { "x": -6, "y": 0, "z": 0 }
    }
  ],
  "connections": [
    {
      "from": "device-1",
      "to": "device-2"
    }
  ]
}
```

## 🤝 Contributing

Contributions are welcome! Feel free to:
- Report bugs
- Suggest new features
- Submit pull requests

## 📄 License

This project is part of KETI's TSN research initiative.

## 🔗 Related Projects

- [Microchip VelocityDRIVE](https://www.microchip.com/)
- [IEEE 802.1 TSN Task Group](https://1.ieee802.org/tsn/)

## 📧 Contact

For questions and support, please open an issue on GitHub.

---

**Developed by KETI (Korea Electronics Technology Institute)**

🔷 Time-Sensitive Networking for Automotive Applications
