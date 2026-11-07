# 🤖 RobotCar

A Raspberry Pi-powered four-wheel robot car with manual control and autonomous obstacle avoidance.

The car uses two DRV8833 motor drivers, four DC motors, and three ultrasonic sensors to detect obstacles and navigate around them.

## Features

* 🚗 Four-wheel motor control
* 🎮 Keyboard/manual driving
* 📡 Left, center, and right ultrasonic sensors
* 🤖 Autonomous obstacle avoidance
* 🔄 Automatic turning and reversing
* 🕹 Manual override while autonomous mode is running

## Hardware

* Raspberry Pi 4B
* 4 × DC gear motors
* 2 × DRV8833 motor drivers
* 3 × HC-SR04 ultrasonic sensors
* 2 × motor battery packs
* Robot chassis and wheels

See [Parts List](docs/PARTS.md) for the complete parts list.

## 📸 Project Photo Gallery

Photos documenting the completed RobotCar, its ultrasonic sensors, Raspberry Pi wiring, and early development stages. **Click any image to view the full-resolution photo.**

All photos are stored in [`projimages/`](projimages/).

### 🚗 Complete RobotCar and Chassis Views

<table>
  <tr>
    <td align="center" width="50%"><a href="projimages/robotcar-complete-side-profile-checkered-mat.jpg"><img src="projimages/robotcar-complete-side-profile-checkered-mat.jpg" alt="Complete robot, side view" width="360"></a><br><sub>Complete robot, side view</sub></td>
    <td align="center" width="50%"><a href="projimages/robotcar-complete-overhead-checkered-mat.jpg"><img src="projimages/robotcar-complete-overhead-checkered-mat.jpg" alt="Complete robot, overhead view" width="360"></a><br><sub>Complete robot, overhead view</sub></td>
  </tr>
  <tr>
    <td align="center" width="50%"><a href="projimages/robotcar-carpet-front-left-angle.jpg"><img src="projimages/robotcar-carpet-front-left-angle.jpg" alt="Front-left angle" width="360"></a><br><sub>Front-left angle</sub></td>
    <td align="center" width="50%"><a href="projimages/robotcar-carpet-front-overhead-view.jpg"><img src="projimages/robotcar-carpet-front-overhead-view.jpg" alt="Front overhead view" width="360"></a><br><sub>Front overhead view</sub></td>
  </tr>
  <tr>
    <td align="center" width="50%"><a href="projimages/robotcar-carpet-left-side-profile.jpg"><img src="projimages/robotcar-carpet-left-side-profile.jpg" alt="Left side profile" width="360"></a><br><sub>Left side profile</sub></td>
    <td align="center" width="50%"><a href="projimages/robotcar-carpet-side-profile.jpg"><img src="projimages/robotcar-carpet-side-profile.jpg" alt="Side profile on carpet" width="360"></a><br><sub>Side profile on carpet</sub></td>
  </tr>
  <tr>
    <td align="center" width="50%"><a href="projimages/robotcar-carpet-side-chassis-view.jpg"><img src="projimages/robotcar-carpet-side-chassis-view.jpg" alt="Chassis and electronics side view" width="360"></a><br><sub>Chassis and electronics side view</sub></td>
    <td align="center" width="50%"><a href="projimages/robotcar-carpet-overhead-angle.jpg"><img src="projimages/robotcar-carpet-overhead-angle.jpg" alt="Angled overhead chassis view" width="360"></a><br><sub>Angled overhead chassis view</sub></td>
  </tr>
  <tr>
    <td align="center" width="50%"><a href="projimages/robotcar-carpet-upper-side-view.jpg"><img src="projimages/robotcar-carpet-upper-side-view.jpg" alt="Upper side of assembled car" width="360"></a><br><sub>Upper side of assembled car</sub></td>
    <td align="center" width="50%"><a href="projimages/robotcar-checkered-mat-side-view.jpg"><img src="projimages/robotcar-checkered-mat-side-view.jpg" alt="Side view on checkered mat" width="360"></a><br><sub>Side view on checkered mat</sub></td>
  </tr>
  <tr>
    <td align="center" width="50%"><a href="projimages/robotcar-full-top-view-chassis-and-components.jpg"><img src="projimages/robotcar-full-top-view-chassis-and-components.jpg" alt="Full chassis and components" width="360"></a><br><sub>Full chassis and components</sub></td>
  </tr>
</table>

### 📡 Ultrasonic Sensors and Display

<table>
  <tr>
    <td align="center" width="50%"><a href="projimages/robotcar-front-view-sensor-array-and-display.jpg"><img src="projimages/robotcar-front-view-sensor-array-and-display.jpg" alt="Front sensor array and display" width="360"></a><br><sub>Front sensor array and display</sub></td>
    <td align="center" width="50%"><a href="projimages/robotcar-front-ultrasonic-sensor-array-and-oled.jpg"><img src="projimages/robotcar-front-ultrasonic-sensor-array-and-oled.jpg" alt="Ultrasonic sensor array and OLED" width="360"></a><br><sub>Ultrasonic sensor array and OLED</sub></td>
  </tr>
  <tr>
    <td align="center" width="50%"><a href="projimages/robotcar-front-ultrasonic-sensor-and-servo.jpg"><img src="projimages/robotcar-front-ultrasonic-sensor-and-servo.jpg" alt="Ultrasonic sensor and servo" width="360"></a><br><sub>Ultrasonic sensor and servo</sub></td>
    <td align="center" width="50%"><a href="projimages/robotcar-front-sensor-assembly-overview.jpg"><img src="projimages/robotcar-front-sensor-assembly-overview.jpg" alt="Front sensor assembly" width="360"></a><br><sub>Front sensor assembly</sub></td>
  </tr>
  <tr>
    <td align="center" width="50%"><a href="projimages/robotcar-front-sensor-and-battery-packs.jpg"><img src="projimages/robotcar-front-sensor-and-battery-packs.jpg" alt="Front sensor and battery packs" width="360"></a><br><sub>Front sensor and battery packs</sub></td>
    <td align="center" width="50%"><a href="projimages/robotcar-servo-mounted-sensor-boards.jpg"><img src="projimages/robotcar-servo-mounted-sensor-boards.jpg" alt="Servo-mounted sensor boards" width="360"></a><br><sub>Servo-mounted sensor boards</sub></td>
  </tr>
  <tr>
    <td align="center" width="50%"><a href="projimages/robotcar-checkered-mat-sensors-closeup.jpg"><img src="projimages/robotcar-checkered-mat-sensors-closeup.jpg" alt="Sensors close-up" width="360"></a><br><sub>Sensors close-up</sub></td>
    <td align="center" width="50%"><a href="projimages/robotcar-top-view-sensors-and-display.jpg"><img src="projimages/robotcar-top-view-sensors-and-display.jpg" alt="Sensors and display from above" width="360"></a><br><sub>Sensors and display from above</sub></td>
  </tr>
  <tr>
    <td align="center" width="50%"><a href="projimages/robotcar-angled-top-view-display-and-sensors.jpg"><img src="projimages/robotcar-angled-top-view-display-and-sensors.jpg" alt="Display and sensors at an angle" width="360"></a><br><sub>Display and sensors at an angle</sub></td>
  </tr>
</table>

### 🔌 Raspberry Pi, Wiring, and Power

<table>
  <tr>
    <td align="center" width="50%"><a href="projimages/robotcar-angled-top-view-wiring-and-pi.jpg"><img src="projimages/robotcar-angled-top-view-wiring-and-pi.jpg" alt="Wiring and Raspberry Pi" width="360"></a><br><sub>Wiring and Raspberry Pi</sub></td>
    <td align="center" width="50%"><a href="projimages/robotcar-raspberry-pi-and-breadboard-overhead.jpg"><img src="projimages/robotcar-raspberry-pi-and-breadboard-overhead.jpg" alt="Raspberry Pi and breadboard" width="360"></a><br><sub>Raspberry Pi and breadboard</sub></td>
  </tr>
  <tr>
    <td align="center" width="50%"><a href="projimages/robotcar-raspberry-pi-wiring-closeup.jpg"><img src="projimages/robotcar-raspberry-pi-wiring-closeup.jpg" alt="Raspberry Pi wiring close-up" width="360"></a><br><sub>Raspberry Pi wiring close-up</sub></td>
    <td align="center" width="50%"><a href="projimages/robotcar-raspberry-pi-ribbon-cable-closeup.jpg"><img src="projimages/robotcar-raspberry-pi-ribbon-cable-closeup.jpg" alt="Raspberry Pi ribbon cable" width="360"></a><br><sub>Raspberry Pi ribbon cable</sub></td>
  </tr>
  <tr>
    <td align="center" width="50%"><a href="projimages/robotcar-ribbon-cable-and-wiring-overhead.jpg"><img src="projimages/robotcar-ribbon-cable-and-wiring-overhead.jpg" alt="Ribbon cable and wiring overhead" width="360"></a><br><sub>Ribbon cable and wiring overhead</sub></td>
    <td align="center" width="50%"><a href="projimages/robotcar-side-electronics-and-power-view.jpg"><img src="projimages/robotcar-side-electronics-and-power-view.jpg" alt="Electronics and power from the side" width="360"></a><br><sub>Electronics and power from the side</sub></td>
  </tr>
  <tr>
    <td align="center" width="50%"><a href="projimages/robotcar-top-view-raspberry-pi-and-power-bank.jpg"><img src="projimages/robotcar-top-view-raspberry-pi-and-power-bank.jpg" alt="Raspberry Pi and power bank" width="360"></a><br><sub>Raspberry Pi and power bank</sub></td>
  </tr>
</table>

### 🛠 Early Prototypes and Development

<table>
  <tr>
    <td align="center" width="50%"><a href="projimages/robotcar-early-prototype-motors-and-controller.jpg"><img src="projimages/robotcar-early-prototype-motors-and-controller.jpg" alt="Early motors and controller prototype" width="360"></a><br><sub>Early motors and controller prototype</sub></td>
    <td align="center" width="50%"><a href="projimages/robotcar-early-prototype-motor-driver-and-pi-case.jpg"><img src="projimages/robotcar-early-prototype-motor-driver-and-pi-case.jpg" alt="Early motor driver and Raspberry Pi case" width="360"></a><br><sub>Early motor driver and Raspberry Pi case</sub></td>
  </tr>
  <tr>
    <td align="center" width="50%"><a href="projimages/robotcar-prototype-pi-breadboard-and-power.jpg"><img src="projimages/robotcar-prototype-pi-breadboard-and-power.jpg" alt="Prototype Raspberry Pi, breadboard, and power" width="360"></a><br><sub>Prototype Raspberry Pi, breadboard, and power</sub></td>
    <td align="center" width="50%"><a href="projimages/robotcar-prototype-ultrasonic-sensor-servo-mount.jpg"><img src="projimages/robotcar-prototype-ultrasonic-sensor-servo-mount.jpg" alt="Prototype ultrasonic sensor servo mount" width="360"></a><br><sub>Prototype ultrasonic sensor servo mount</sub></td>
  </tr>
</table>

## Quick Start

Clone the repository:

```bash
git clone https://github.com/overcharged-coder/RobotCar.git
cd RobotCar
```

Install the required Raspberry Pi package:

```bash
sudo apt update
sudo apt install -y python3-gpiozero
```

### Test the Motors

```bash
python3 motor_test.py
```

### Test the Ultrasonic Sensors

```bash
python3 ultrasonic_test.py
```

### Manual Driving

```bash
python3 drive.py
```

Controls:

| Key | Action |
| --- | --- |
| `W` | Forward |
| `S` | Reverse |
| `A` | Left |
| `D` | Right |
| `SPACE` | Stop |
| `Q` | Quit |

### Autonomous Mode

```bash
python3 autonomous.py
```

The car drives forward while monitoring all three ultrasonic sensors.

If an obstacle is detected, it can:

* Stop
* Reverse
* Compare the available space
* Turn toward the clearer direction
* Continue driving

Manual controls can also temporarily override autonomous mode.

## Documentation

* 📦 [Parts List](docs/PARTS.md)
* 🔧 [Build & Wiring Guide](docs/BUILD.md)
* 💻 [Software Setup](docs/SOFTWARE.md)
* 🔌 [Wiring Diagram](docs/drawings/pi-wiring.png)

## Project Updates

Current development work, planned features, and known issues are tracked here:

* 📋 [RobotCar Project Board](https://github.com/users/overcharged-coder/projects/2)
* 🛠 [Open Issues](https://github.com/overcharged-coder/RobotCar/issues)
* ✅ [Closed Issues](https://github.com/overcharged-coder/RobotCar/issues?q=is%3Aissue%20state%3Aclosed)

The Project Board is the main place to see what is currently being worked on, what is planned next, and what has been completed.

## Future Development

The next stage of RobotCar will add camera-based navigation so the car can identify driveable floor and make smarter navigation decisions instead of relying only on ultrasonic sensors.
