# 🤖 Artemis _Season_ Code

This project is based on the WPILib command-based architecture, a software design pattern widely used in FIRST Robotics Competition robotics projects.  
The idea behind the command-based model is to organize the robot code using `Object-Oriented Programming (OOP)`, separating robot actions, hardware abstractions, and utilities into independent and reusable modules.

<br>

---

# 👨‍💻 Project Organization

> The robot source code is mainly located inside:
> 
> src/main/java/frc/robot


Below is the current structure of the project:

```txt
📦 teste_swervedrive
├── 📂 src/main/java/frc/robot
│
├── 📂 adl
│   └── # Custom ADL-related systems/utilities
│
├── 📂 commands
│   ├── 📂 driveAuto
│   │   └── # Autonomous driving commands
│   │
│   ├── 📂 teleopDrive
│   │   └── # Teleoperated driving commands
│   │
│   ├── 📂 vision
│   │   └── # Vision-related commands
│   │
│   └── 📂 Poses
│       └── # Robot positioning and pose utilities
│
├── 📂 Dashboards
│   ├── 📂 ADLDashboard
│   ├── 📂 Drive
│   └── 📂 RobotStress
│       └── # The dashboard communication to the robot
│
├── 📂 subsystems
│   │
│   ├── 📂 Swervedrive
│   │   └── # Swerve drivetrain subsystem
│   │
│   ├── 📂 Sensors
│   │   └── # Sensor abstractions and integrations
│   │
│   └── 📂 Score
│       ├── 📂 Angular
│       ├── 📂 Climb
│       ├── 📂 PreShooter
│       ├── 📂 Rollers
│       ├── 📂 Shooter
│       └── 📂 Spindexer
│           └── # Scoring-related mechanisms, separated in hardware and manager
│
├── 📂 TagsID
│   └── # AprilTag / vision tag utilities
│
├── 📄 Robot.java # Main robot lifecycle class
│
├── 📄 RobotContainer.java # Command bindings and subsystem setup
│
└── 📄 Main.java # Robot entry point
```

<br>

---

# ⚙️ Additional Project Components

Besides the robot code itself, the repository also contains additional tools and utilities:

```txt
📦 Dashboard
├── 📂 dashboard-bridge/py
│   ├── 📂 bridge
│   │   └── # Dashboard communication bridge
│   │
│   ├── 📂 cameras
│   │   └── # Camera integrations and streaming systems
│   │
│   └── 📂 limelight
│       └── # Limelight integration utilities
│
└── 📂 dashboard-web
    ├── 📂 css
    │   ├── 📂 adl
    │   ├── 📂 cameras
    │   └── 📂 stress
    │   └── 📄 global.css 
    │
    ├── 📂 js
    │   ├── 📂 adl
    │   ├── 📂 cameras
    │   └── 📂 stress
    │   └── 📄 ws.js
    │
    ├── 📄 cameras.html
    └── 📄 index.html 
```

<br>

---

# 🧠 Code Logic

The robot logic follows the standard WPILib command-based lifecycle:

- **Subsystems** handle hardware abstraction
- **Commands** define robot actions and behaviors
- **RobotContainer** connects controls, commands, and subsystems
- **PathPlanner** manages autonomous trajectories
- **Dashboards** provide telemetry and debugging interfaces

The drivetrain is based on a **swerve drive architecture**, allowing:
- Independent wheel steering
- Holonomic movement
- Field-oriented driving
- Advanced autonomous path following

The repository also integrates:
- Vision systems
- Dashboard communication bridges
- Stress/debug monitoring
- Stream Deck operator controls

<br>

---

# 🚗 Autonomous & Path Planning

Autonomous routines are stored inside:

```txt
src/main/deploy/pathplanner
```

This includes:
- Pre-generated autonomous paths
- Auto routines
- Generated JSON trajectory files

The project uses PathPlanner for autonomous trajectory generation and execution.

<br>

---

# ❓ Where can I find the code?

Main robot code:

```txt
src/main/java/frc/robot
```

Autonomous and deploy files:

```txt
src/main/deploy
```

Dashboard systems:

```txt
dashboard-web
dashboard-bridge
```

External operator integrations:

```txt
streamdeck-control
```
