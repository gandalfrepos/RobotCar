<p align="center">
  <a href="https://omspace.dev"><strong>OM.</strong></a> &nbsp; / &nbsp; PROJECTS &nbsp; / &nbsp; ROBOTICS
</p>

<p align="center">
  <img src="https://img.shields.io/badge/FEATURED%20PROJECT-ROBOTICS-06B6D4?style=for-the-badge&labelColor=0F172A" alt="Featured robotics project">
</p>

<h1 align="center">🤖 Autonomous RobotCar</h1>

<p align="center">
  <strong>A four-wheel robot that senses obstacles, makes decisions, and navigates on its own.</strong>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Raspberry%20Pi%204B-0F172A?style=flat-square&logo=raspberrypi&logoColor=white" alt="Raspberry Pi 4B">
  <img src="https://img.shields.io/badge/Python-2563EB?style=flat-square&logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/Autonomous%20Navigation-7C3AED?style=flat-square" alt="Autonomous navigation">
  <img src="https://img.shields.io/badge/2026%20Build-0F766E?style=flat-square" alt="2026 build">
</p>

<p align="center">
  <a href="https://omspace.dev/pages/project-robot-car.html"><strong>🌐 Project Story</strong></a> &nbsp; | &nbsp;
  <a href="https://www.youtube.com/watch?v=gdj-aWxs_uI"><strong>▶️ Watch Demo</strong></a> &nbsp; | &nbsp;
  <a href="GALLERY.md"><strong>📸 Gallery</strong></a> &nbsp; | &nbsp;
  <a href="docs/BUILD.md"><strong>🛠️ Build Guide</strong></a>
</p>

<table align="center">
  <tr>
    <td align="center">
      <a href="projImages/robocarheroimage.png">
        <img src="projImages/robocarheroimage.png" alt="Om's Raspberry Pi RobotCar on a grey background" width="700">
      </a>
      <br>
      <sub>RobotCar — four-wheel autonomous obstacle-avoidance prototype</sub>
    </td>
  </tr>
</table>

<p align="center"><sub>2026 &nbsp; • &nbsp; DESIGNED, BUILT &amp; PROGRAMMED BY OM CHATTERJEE &nbsp; • &nbsp; ACTIVE DEVELOPMENT</sub></p>

---

<p><img src="https://img.shields.io/badge/01-OVERVIEW-06B6D4?style=for-the-badge&labelColor=0F172A" alt="01 - Overview"></p>

## 🎯 The challenge

> **THE ENGINEERING CHALLENGE**  
> Making a robot move is one task. Making it choose a safe direction on its own is another.

I built RobotCar to explore the connection between **sensing, decision-making, and physical motion**. A Raspberry Pi controls four DC motors through two DRV8833 drivers. Three ultrasonic sensors measure nearby obstacles, and Python logic uses those readings to continue, stop, reverse, or turn toward a clearer route.

Manual keyboard control provides a way to test movement directly and temporarily override autonomous navigation.

<table align="center">
  <tr>
    <td align="center" width="25%"><strong>4</strong><br><sub>DRIVE MOTORS</sub></td>
    <td align="center" width="25%"><strong>3</strong><br><sub>ULTRASONIC SENSORS</sub></td>
    <td align="center" width="25%"><strong>2</strong><br><sub>DRV8833 DRIVERS</sub></td>
    <td align="center" width="25%"><strong>1</strong><br><sub>RASPBERRY PI 4B</sub></td>
  </tr>
</table>

---

<p><img src="https://img.shields.io/badge/02-SYSTEM%20DESIGN-3B82F6?style=for-the-badge&labelColor=0F172A" alt="02 - System Design"></p>

## ⚙️ From code to motion

| Layer | Hardware / software | Purpose |
| :--- | :--- | :--- |
| **Compute** | Raspberry Pi 4B, Python | Runs the control and navigation programs |
| **Movement** | 4 DC gear motors, 2 DRV8833 drivers | Drives and steers the four-wheel chassis |
| **Sensing** | 3 HC-SR04 ultrasonic sensors | Reads distances to the left, center, and right |
| **Power** | 2 motor battery packs | Supplies the drivetrain separately from the controller |
| **Control** | Keyboard input, autonomous logic | Provides direct driving and obstacle avoidance |

### 🔁 How the car decides

The autonomous mode follows a simple, continuous feedback loop:

| 👀 SENSE | 🧠 DECIDE | 🚗 MOVE |
| :---: | :---: | :---: |
| Read three distances | Select a safer path | Drive, reverse, or turn |

**Navigation sequence**

1. **Drive.** Move forward while monitoring the left, center, and right sensors.
2. **Detect.** Stop when an obstacle is too close.
3. **Create space.** Reverse if extra room is needed.
4. **Compare.** Check which direction has more available space.
5. **Turn.** Rotate toward the clearer side.
6. **Continue.** Resume moving and keep checking the sensors.

This is reactive obstacle avoidance. Camera-based interpretation of the floor is a planned extension, not part of the current navigation system.

---

<p><img src="https://img.shields.io/badge/03-DEMONSTRATION-8B5CF6?style=for-the-badge&labelColor=0F172A" alt="03 - Demonstration"></p>

## 🎬 RobotCar in motion

**Watch the real test footage.** The video shows RobotCar driving and navigating a kitchen environment.

<p align="center">
  <a href="https://www.youtube.com/watch?v=gdj-aWxs_uI">
    <img src="https://img.youtube.com/vi/gdj-aWxs_uI/hqdefault.jpg" alt="Watch the RobotCar demonstration on YouTube" width="480">
  </a>
  <br>
  <sub>Click to watch the RobotCar demo on YouTube</sub>
</p>

---

<p><img src="https://img.shields.io/badge/04-CONTROL-06B6D4?style=for-the-badge&labelColor=0F172A" alt="04 - Control"></p>

## 🎮 Manual and autonomous driving

Manual mode helps verify the drivetrain independently from the navigation algorithm.

| Key | Action |
| :---: | :--- |
| `W` | Forward |
| `S` | Reverse |
| `A` | Left |
| `D` | Right |
| `SPACE` | Stop |
| `Q` | Quit |

Autonomous mode monitors all three sensors and changes direction when obstacles are detected. Manual input can temporarily override autonomous control.

---

<p><img src="https://img.shields.io/badge/05-GETTING%20STARTED-3B82F6?style=for-the-badge&labelColor=0F172A" alt="05 - Getting Started"></p>

## 🚀 Run the project

Clone the current repository:

```bash
git clone https://github.com/gandalfrepos/RobotCar.git
cd RobotCar
```

Install the Raspberry Pi GPIO package:

```bash
sudo apt update
sudo apt install -y python3-gpiozero
```

| Task | Command |
| :--- | :--- |
| Test the four motors | `python3 motor_test.py` |
| Test ultrasonic sensors | `python3 ultrasonic_test.py` |
| Drive with the keyboard | `python3 drive.py` |
| Start obstacle avoidance | `python3 autonomous.py` |

> Run these scripts on the Raspberry Pi with the motor drivers, sensors, and power supplies wired according to the project documentation.

---

<p><img src="https://img.shields.io/badge/06-PROJECT%20MEDIA-8B5CF6?style=for-the-badge&labelColor=0F172A" alt="06 - Project Media"></p>

## 📸 Build gallery

A visual record of the build, from early motor prototypes to the assembled robot. **Preview four highlights below**, then explore all **31 photos** in the separate gallery.

<table align="center">
  <tr>
    <td align="center" width="25%">
      <a href="projImages/robotcar-complete-side-profile-checkered-mat.jpg">
        <img src="projImages/robotcar-complete-side-profile-checkered-mat.jpg" alt="Completed RobotCar side view" width="145">
      </a><br><sub>COMPLETE BUILD</sub>
    </td>
    <td align="center" width="25%">
      <a href="projImages/robotcar-front-view-sensor-array-and-display.jpg">
        <img src="projImages/robotcar-front-view-sensor-array-and-display.jpg" alt="Ultrasonic sensor array and display" width="145">
      </a><br><sub>SENSORS &amp; DISPLAY</sub>
    </td>
    <td align="center" width="25%">
      <a href="projImages/robotcar-raspberry-pi-wiring-closeup.jpg">
        <img src="projImages/robotcar-raspberry-pi-wiring-closeup.jpg" alt="Raspberry Pi and wiring detail" width="145">
      </a><br><sub>ELECTRONICS</sub>
    </td>
    <td align="center" width="25%">
      <a href="projImages/robotcar-early-prototype-motors-and-controller.jpg">
        <img src="projImages/robotcar-early-prototype-motors-and-controller.jpg" alt="Early RobotCar motor and controller prototype" width="145">
      </a><br><sub>EARLY PROTOTYPE</sub>
    </td>
  </tr>
</table>

<p align="center">
  <a href="GALLERY.md"><strong>📷 OPEN THE FULL 31-PHOTO GALLERY →</strong></a>
</p>

The original images are stored in [`projImages/`](projImages/).

---

<p><img src="https://img.shields.io/badge/07-DOCUMENTATION-3B82F6?style=for-the-badge&labelColor=0F172A" alt="07 - Documentation"></p>

## 📚 Build and technical references

| Document | Description |
| :--- | :--- |
| [Parts list](docs/PARTS.md) | Components and hardware used |
| [Build & wiring guide](docs/BUILD.md) | Assembly and connections |
| [Software setup](docs/SOFTWARE.md) | Raspberry Pi configuration and dependencies |
| [Wiring diagram](docs/drawings/pi-wiring.png) | Circuit connection reference |
| [Source files](https://github.com/gandalfrepos/RobotCar) | Python programs and repository history |

---

<p><img src="https://img.shields.io/badge/08-DEVELOPMENT-06B6D4?style=for-the-badge&labelColor=0F172A" alt="08 - Development"></p>

## 🔭 Building in layers

The project was developed by testing individual subsystems before combining them:

- **Motor control:** Verify direction and steering before adding autonomous logic.
- **Sensor integration:** Check distance readings from each ultrasonic sensor.
- **Manual driving:** Confirm that hardware responds correctly to keyboard commands.
- **Autonomy:** Combine distance measurements and movement rules into an obstacle-avoidance loop.
- **Hardware iteration:** Move from early L298N driver prototypes to the more efficient DRV8833 motor drivers.

### 📷 Next milestone: computer vision

Ultrasonic distance readings indicate how far away an obstacle is, but not what it is or whether a visible area is driveable. The planned next stage uses a camera to identify floor space and make more informed navigation decisions.

### 🗂️ Development tracking

[Open issues](https://github.com/gandalfrepos/RobotCar/issues) · [Closed issues](https://github.com/gandalfrepos/RobotCar/issues?q=is%3Aissue%20state%3Aclosed) · [Original project board](https://github.com/users/overcharged-coder/projects/2)

---

<p align="center">
  <a href="https://omspace.dev"><strong>OM.</strong></a><br>
  <sub>OM CHATTERJEE &nbsp; • &nbsp; ROBOTICS + SOFTWARE &nbsp; • &nbsp; LEARNING BY BUILDING</sub><br><br>
  <a href="https://omspace.dev/pages/project-robot-car.html">Project portfolio</a> &nbsp; • &nbsp; <a href="GALLERY.md">Photo gallery</a> &nbsp; • &nbsp; <a href="#-autonomous-robotcar">Back to top ↑</a>
</p>
