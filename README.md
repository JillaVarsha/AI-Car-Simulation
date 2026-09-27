# 🚗 AI Car Simulation

### Autonomous Car Simulation using NEAT and Pygame

This project is an artificial intelligence-based autonomous driving simulation where virtual cars learn to navigate a track without direct human control.

The project uses a **Neural Network** combined with the **NEAT (NeuroEvolution of Augmenting Topologies)** algorithm to evolve driving behavior across multiple generations. Each car uses radar-like sensors to detect obstacles and makes driving decisions based on the information received.

The simulation is built using **Python and Pygame**.

---

## ✨ Features

* 🧠 Neural-network-based autonomous driving
* 🧬 NEAT evolutionary learning algorithm
* 🚗 Multiple AI-controlled cars
* 📡 Radar sensors for obstacle detection
* 💥 Collision detection
* 🛣️ Track/map-based driving environment
* 📊 Generation tracking
* 👥 Displays the number of cars still alive
* ⏸️ Pause/Play functionality using the **Spacebar**
* 📈 Fitness calculation based on the distance travelled
* 🔄 Evolution across multiple generations

---

## 🧠 How It Works

Each car is controlled by a neural network generated using NEAT.

The car receives information from multiple radar sensors positioned around it. These sensors measure the distance between the car and the track boundaries.

The sensor values are provided as inputs to the neural network.

The network then chooses one of several possible actions:

* Turn left
* Turn right
* Reduce speed
* Increase speed

The cars that successfully travel farther receive higher fitness values. NEAT uses these fitness values to evolve the population over successive generations.

### Basic Flow

```text
Track Map
    ↓
Radar Sensors
    ↓
Distance Measurements
    ↓
Neural Network
    ↓
Driving Decision
    ↓
Move / Turn / Brake / Accelerate
    ↓
Collision Detection
    ↓
Fitness Calculation
    ↓
Evolution through NEAT
    ↓
Next Generation
```

---

## 🛠️ Technologies Used

| Technology  | Purpose                          |
| ----------- | -------------------------------- |
| Python      | Core programming language        |
| Pygame      | Simulation and graphics          |
| NEAT-Python | Neural network evolution         |
| Math        | Movement and sensor calculations |
| Random      | Randomized operations            |
| Sys         | Program and event handling       |

---

## 📁 Project Structure

```text
AI-Car-Simulation/
│
├── newcar.py
├── config.txt
├── car.png
├── map.png
```

### File Description

**`newcar.py`**
Contains the main simulation, car class, radar sensors, collision detection, neural-network interaction, fitness calculation, and generation loop.

**`config.txt`**
Contains the NEAT configuration used to create and evolve the neural networks.

**`car.png`**
Image used as the car sprite in the simulation.

**`map.png`**
Track/map used as the driving environment.

---

## ⚙️ Installation

### 1. Clone the repository

```bash
git clone https://github.com/your-username/AI-Car-Simulation.git
cd AI-Car-Simulation
```

### 2. Install the required libraries

```bash
pip install pygame neat-python
```

### 3. Make sure the required files are present

```text
newcar.py
config.txt
car.png
map.png
```

### 4. Run the simulation

```bash
python newcar.py
```

---

## 🎮 Controls

| Key          | Action                    |
| ------------ | ------------------------- |
| `SPACE`      | Pause / Resume simulation |
| Close Window | Exit simulation           |

The simulation displays the current generation and the number of cars that remain alive.

---

## 📡 Radar Sensor System

Each car uses multiple radar sensors to detect the surrounding track boundaries.

The sensors operate at different angles around the vehicle and measure distances up to a defined range.

These measurements are converted into values and supplied to the neural network as input data.

---

## 🧬 NEAT Evolution

The project uses **NEAT — NeuroEvolution of Augmenting Topologies**.

At the beginning of a generation, multiple neural networks control different cars.

Each car receives a fitness value based on how far it travels.

Cars that achieve better fitness contribute to the evolutionary process, allowing later generations to develop improved driving behavior.

---

## 🚗 Car Decision System

The neural network receives radar data:

```text
Radar 1
Radar 2
Radar 3
Radar 4
Radar 5
       ↓
 Neural Network
       ↓
   Best Action
```

The selected output determines the car's movement, such as changing its angle or adjusting its speed.

---

## 📊 Fitness

The primary fitness measurement is the distance travelled by the car.

This encourages the evolutionary algorithm to develop cars that can survive longer and navigate farther along the track.

---

## ⏸️ Pause / Resume

The simulation can be paused and resumed using the **Spacebar**.

When paused, the simulation displays a pause overlay while maintaining the current simulation state.

---

## 🔮 Future Improvements

Possible improvements include:

* 🧠 More advanced neural-network architectures
* 🛣️ Multiple tracks and environments
* 🚦 Traffic and obstacle simulation
* 🏁 Lap and checkpoint systems
* 📈 Fitness and generation graphs
* 💾 Saving and loading trained models
* 🎥 Replay of the best-performing car
* 🚗 Different vehicle types
* 🌐 Web-based visualization
* 🎯 More sophisticated reward functions

---

## 🎯 Project Objective

The objective of this project is to demonstrate how **evolutionary neural networks can be used to develop autonomous driving behavior** through simulation.

Instead of manually programming every driving decision, the system allows neural networks to evolve through repeated interaction with the environment.

---

## 📌 Project Status

**Status:** 🚧 Developing / Experimental

The current implementation supports autonomous car simulation, radar-based sensing, collision detection, evolutionary generations, fitness calculation, and pause/resume functionality.
