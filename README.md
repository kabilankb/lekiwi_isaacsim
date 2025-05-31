
---

# 🦾 Lekiwi URDF for Isaac Sim

This repository provides the **Unified Robot Description Format (URDF)** models for the **Lekiwi robot**, optimized for use within **NVIDIA Isaac Sim**. Our goal is to enable realistic, high-fidelity simulations of the Lekiwi robot for robotics research, development, and testing.

![Image](https://github.com/user-attachments/assets/d5f6e9d0-4639-4994-b41d-35f78ffdd3ef)
---

## 📚 Table of Contents

* [About Lekiwi](#about-lekiwi)
* [Features](#features)
* [Getting Started](#getting-started)

  * [Prerequisites](#prerequisites)
  * [Installation](#installation)
  * [Usage in Isaac Sim](#usage-in-isaac-sim)
  * [Viewing the URDF with ROS 2](#viewing-the-urdf-with-ros-2)
* [Current URDF Models](#current-urdf-models)
* [Upcoming Work](#upcoming-work)
* [Contributing](#contributing)
* [License](#license)
* [Contact](#contact)

---

## 🤖 About Lekiwi

**Lekiwi** is a compact mobile manipulator designed for **indoor navigation** and **precise object manipulation**. This repository provides accurate URDF representations of Lekiwi for seamless integration into simulation environments like **Isaac Sim**.

---

## ✨ Features

* ✅ **Isaac Sim Compatible**: Designed and tested with NVIDIA Isaac Sim.
* 🧩 **Modular Design**: Easily modify or extend components.
* 🔧 **Accurate Kinematics & Dynamics**: Faithful representation of Lekiwi's real-world properties.
* 🎨 **Visual Meshes Included**: Realistic visuals using `.stl` or `.obj` meshes.

---

## 🚀 Getting Started

Follow these instructions to set up the URDF model locally for development and simulation.

### 🔧 Prerequisites

* **NVIDIA Isaac Sim** (See [Isaac Sim Docs](https://docs.omniverse.nvidia.com/app_isaacsim/app_isaacsim/overview.html))
* **Python 3.x**
* **ROS 2** (`Humble`, `Iron`, or `Rolling` recommended)
* **urdf\_tutorial** package:

  ```bash
  sudo apt install ros-<ros2-distro>-urdf-tutorial
  ```

---

### 📦 Installation

1. **Clone the Repository:**

   ```bash
   git clone git@github.com:kabilankb/lekiwi_isaacsim.git
   cd lekiwi-urdf-isaacsim
   ```

2. **Place URDF in Isaac Sim Assets:**

   **Recommended (Symbolic Link for Development):**

   ```bash
   cd ~/.local/share/ov/pkg/isaac_sim-202X.X.X/exts/omni.isaac.examples/omni/isaac/examples/usd_assets/
   ln -s /absolute/path/to/lekiwi-urdf-isaacsim lekiwi_robot
   ```

   **Alternative (Direct Copy):**

   ```bash
   cp -r urdf meshes /path/to/isaac_sim_assets/lekiwi_robot/
   ```

---

### 🛠️ Usage in Isaac Sim

1. Launch Isaac Sim.
2. Go to `File -> New Stage`.
3. Import the URDF:

   * `File -> Import -> URDF`
   * Navigate to:
     `omniverse://localhost/NVIDIA/Assets/lekiwi_robot/urdf/lekiwi.urdf`
   * Select `lekiwi.urdf`
   * Enable **merge fixed joints** for better performance (optional).
4. Simulate and interact with the robot in the scene.

---

### 👁️ Viewing the URDF with ROS 2

1. **Source ROS 2:**

   ```bash
   source /opt/ros/<ros2-distro>/setup.bash
   ```

2. **Launch URDF in RViz:**

   ```bash
   ros2 launch urdf_tutorial display.launch.py model:=/absolute/path/to/lekiwi-urdf-isaacsim/urdf/lekiwi.urdf
   ```
![Image](https://github.com/user-attachments/assets/ed895c3b-36ca-43e3-965a-78523df1fa8b)
---

## 📁 Current URDF Models

* `urdf/lekiwi.urdf` – Main URDF file for Lekiwi
* `meshes/` – Visual and collision meshes (`.stl`, `.obj`, etc.)

---

## 🧪 Upcoming Work

* ⚙️ Refined collision meshes
* 📷 Sensor integration (LiDAR, cameras, IMU)
* 🔩 Actuator control enhancements (velocity/torque/friction)
* 🤖 ROS 2 control integration (`ros2_control`)
* 🌐 Task-specific Isaac Sim environments
* 📘 Expanded documentation and tutorials
* 🚀 Simulation performance optimization

---

## 🤝 Contributing

We welcome contributions from the community!

1. Fork the repo
2. Create a new branch:

   ```bash
   git checkout -b feature/your-feature-name
   ```
3. Commit your changes:

   ```bash
   git commit -m "Add: Description of your feature"
   ```
4. Push and open a Pull Request.

Please follow coding standards and include relevant documentation. For major features, open an issue for discussion first.

---

## 📄 License

This project is licensed under the **[MIT License](LICENSE)**. You may modify and use it freely under the terms specified.

---

