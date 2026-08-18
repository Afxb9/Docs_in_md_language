# Robotics & Autonomous Systems

# Skills Development Master Curriculum

**Version 1.2 — Detailed Reference Edition**

A practical, project-driven, competency-gated development plan for an experienced mechanical engineer expanding into embedded systems, electronics, software, robotics, AI, computer vision and UAV autonomy.

Target window: 18 months if progress is strong; 18–24 months is the sustainable completion window. The calendar guides progress, but competency gates decide when a stage is complete.

**Scope frozen after v1.1: new interesting topics go to the Future Development Backlog unless they are required for the active stage.**

# 1. Purpose of This Document

This document is the single source of truth for the Self Development project. It defines the technical direction, stage sequence, learning philosophy, workload, competency standards, project progression, resource-selection rules, and chat-organization system.

It is intentionally broader than any one course. Courses, books, tutorials and certificates are resources that serve this curriculum; they do not define the curriculum.

* Use this document to decide what belongs in the active learning plan.
* Use separate stage chats for detailed teaching, exercises, projects and assessment.
* A single stage may use multiple chats. Continuity is maintained through a Stage Progress Record described later in this document.
* Update this master document only when the overall roadmap, scope, competency requirements or sequencing changes.

# 2. Learner Profile and Design Constraints

The curriculum assumes an existing mechanical-engineering foundation and meaningful hands-on exposure to Arduino, ESP32, Raspberry Pi, programming, CAD/3D printing, robotics and AI/computer-vision projects. The purpose is therefore not to restart from zero, but to close conceptual gaps and develop professional code/system literacy.

| **Constraint / Strength**                 | **Curriculum Response**                                                                                                  |
| ----------------------------------------- | ------------------------------------------------------------------------------------------------------------------------ |
| Full-time work: approximately 8 hours/day | Work hours are excluded from study time. Workday study sessions must remain short and optional enough to be sustainable. |
| Two days off per week                     | One longer hands-on block is preferred; the second day off should not automatically become a full study day.             |
| Family and daily responsibilities         | Normal target is 4–5 study hours/week; 6–7 hours is an excellent week, not an obligation.                                |
| Existing project experience               | Use diagnostic baselines and skip material already demonstrated at competency level.                                     |
| Easy distraction / strong curiosity       | Use a frozen active curriculum, Parking Lot Rule and Future Development Backlog.                                         |
| Interest in future PhD                    | Build strong technical foundations now; formal research/math track remains deferred.                                     |

# 3. End Goal

The long-term technical identity is a mechanically grounded Robotics and Autonomous Systems Engineer who can integrate hardware, software, perception, communication and control rather than merely assemble tutorials.

```text
Mechanical Engineering / CAD / Manufacturing
                ↓
        Electronics + Embedded Systems
                ↓
           C/C++ + Python
                ↓
     Linux / Raspberry Pi / Networking
                ↓
           ROS 2 / Robotics
                ↓
    Computer Vision + ML / Edge AI
                ↓
        UAV Systems + Autonomy
```

# 4. Learning Philosophy

Learn → experiment → build → break → debug → understand → document → improve.

* Understanding why is more important than reproducing a tutorial.
* Hands-on work should normally exceed passive learning.
* A concept is not 'learned' because a video or certificate is complete.
* Professional documentation, datasheets and source code should become normal learning tools.
* Old projects should be revisited and refactored as skills improve.
* Theory is learned in service of engineering capability, while still filling important fundamentals systematically.

# 5. The 60/40 Guideline

| **Activity**      | **Typical Share** | **Examples**                                                                                             |
| ----------------- | ----------------- | -------------------------------------------------------------------------------------------------------- |
| Hands-on / active | ≈60%              | Coding, circuits, measurements, debugging, experiments, integration, code reading, project documentation |
| Structured theory | ≈40%              | Courses, focused reading, official documentation, concept exercises                                      |

This is a guideline, not a weekly accounting requirement. Some theory-heavy weeks or integration-heavy weeks will naturally differ.

# 6. C/C++ Learning Strategy

**C and C++ will be treated as an integrated programming foundation rather than as two completely separate beginner courses.**

C++ will be the primary language for structured programming experiments and modern software development, while the curriculum will deliberately develop the C literacy required for embedded systems, robotics, systems programming, Linux, and hardware-oriented engineering.

C and C++ share a substantial foundation, including variables, fundamental data types, operators, expressions, control flow, functions, arrays, structures, pointers, memory concepts, compilation, and linking. However, C++ introduces additional abstractions and programming mechanisms, while C exposes several low-level programming concepts and idioms that remain important in embedded and systems-oriented work.

The curriculum will therefore develop the common programming and memory concepts shared by both languages while deliberately exposing the learner to important C-specific concepts and code where they are relevant.

C literacy will include, at an appropriate practical level:

* procedural programming and function-based design
* C-style arrays and character arrays
* pointers, addresses, dereferencing, and pointer/array relationships
* structures and enumerations
* C-style strings and relevant standard-library functions
* formatted C I/O such as `printf()` and basic format specifiers
* manual dynamic-memory concepts such as `malloc()`, `calloc()`, `realloc()`, and `free()`
* compilation, linking, object files, headers, source files, and executable generation
* the ability to read and understand existing C code

The curriculum will then progressively introduce modern C++ mechanisms and explain why they are useful, including:

* references
* classes and objects
* constructors and destructors
* RAII
* namespaces
* `std::string`
* standard containers and algorithms
* smart pointers
* templates and other relevant modern C++ features

**The curriculum does not require completion of a separate full introductory C course by default.** C material will be studied selectively according to the competency being developed and the engineering context. A dedicated C study block or course may be introduced later if a competency assessment identifies a genuine gap.

The objective is **C/C++ engineering literacy**, not completion of two independent programming courses.

The learner should ultimately be able to write structured C++ code, understand important C concepts, read basic-to-moderate C code, understand memory behavior, and move comfortably between C and C++ codebases encountered in embedded systems, robotics, Linux, libraries, and hardware-oriented projects.

# 7. Competency Framework

| **Level**              | **Meaning**                            | **Evidence**                                                                 |
| ---------------------- | -------------------------------------- | ---------------------------------------------------------------------------- |
| L1 — Recognize         | Know the term and purpose              | Can identify TCP, a MOSFET, a pointer, a ROS topic, etc.                     |
| L2 — Explain           | Explain accurately in own words        | Can compare TCP/UDP or BJT/MOSFET and explain tradeoffs.                     |
| L3 — Implement         | Use independently                      | Can build a socket application, sensor driver, ROS node or CV pipeline.      |
| L4 — Diagnose / Design | Troubleshoot and make design decisions | Can trace failures, inspect source/packets/signals and justify architecture. |

A topic is normally not considered learned until approximately L3. Core topics should progressively approach L4.

# 8. Timeline Policy: 18–24 Months

The curriculum has a target of approximately 18 months because a visible destination helps maintain momentum. However, 18 months is not a deadline. The sustainable completion window is 18–24 months, and stage completion is competency-gated.

| **Week Type**          | **Expected Study Time** | **Interpretation**                                       |
| ---------------------- | ----------------------- | -------------------------------------------------------- |
| Very busy week         | 0–2 h                   | Life happened. Resume; no catch-up debt.                 |
| Busy but progressing   | 2–3 h                   | Acceptable progress.                                     |
| Normal successful week | 4–5 h                   | The curriculum is designed around this range.            |
| Strong week            | 6–7 h                   | Excellent; use extra time for projects or consolidation. |
| >7 h                   | Optional only           | Never required to keep the plan on track.                |

Seven hours/week is a ceiling to use when available, not a quota. The plan should still function at 4–5 hours/week.

# 9. Three-Level Planning System

```text
LEVEL 1 — MASTER CURRICULUM
 Where am I going?  (18–24 month view)
                ↓
 LEVEL 2 — CURRENT STAGE PLAN
 What competencies am I building?  (typically several weeks)
                ↓
 LEVEL 3 — CURRENT WEEK
 What exactly should I do now?
```

The learner should spend most attention on Level 3. Future stages remain visible in this document but should not compete for attention with the current stage.

# 10. Core Roadmap

| **Stage** | **Target Window*** | **Core Focus**                                                        | **Primary Output**                                      |
| --------- | ------------------ | --------------------------------------------------------------------- | ------------------------------------------------------- |
| 0         | ~2 weeks           | Engineering environment, Git, compiler/build concepts and baseline    | Organized engineering workspace and baseline assessment |
| 1         | ~10–12 weeks       | C/C++ foundations + electronics + light Python foundations            | Custom sensor/actuator module and own sensor driver     |
| 2         | ~7–9 weeks         | Embedded systems, ESP32 architecture, interrupts, timers and FreeRTOS | Structured embedded platform                            |
| 3         | ~6–8 weeks         | Raspberry Pi + Linux + engineering Python scripting                   | Headless Pi edge computer                               |
| 4         | ~7–9 weeks         | Networking + IoT fundamentals                                         | Network-connected robot and packet-level understanding  |
| 5         | ~10–12 weeks       | ROS 2 + mobile robotics                                               | ROS-enabled rover                                       |
| 6         | ~6–8 weeks         | Computer vision / OpenCV                                              | Vision-guided robot                                     |
| 7         | ~8–10 weeks        | ML foundations + PyTorch + edge AI                                    | AI-enabled autonomous robot                             |
| 8         | ~10–14+ weeks      | UAV systems, ArduPilot/PX4, Mission Planner, MAVLink and autonomy     | Autonomous UAV foundation / capstone                    |

*Target windows are planning estimates only. Prior knowledge may shorten a stage; competency gaps may extend it.

# 11. Active Curriculum — Scope Freeze

The active curriculum is intentionally limited to the following sequence:

```text
C/C++ + Electronics + light Python
             ↓
 Embedded Systems / ESP32
             ↓
 Raspberry Pi / Linux
             ↓
 Networking / IoT
             ↓
 ROS 2 / Robotics
             ↓
 Computer Vision
             ↓
 Machine Learning / PyTorch / Edge AI
             ↓
 UAV Systems / Autonomy
```

Web/app development and the wider supporting-skill backlog are not active study tracks during the core journey unless a minimum amount is needed to complete a core project.
# 12. Longitudinal Track A — Python Engineering & Data Skills

Python is not studied as a second full beginner curriculum in parallel with C/C++. C/C++ is the deeper early programming track; Python is strengthened progressively through engineering use.

| **Stage** | **Python Emphasis**                                                                     |
| --------- | --------------------------------------------------------------------------------------- |
| Stage 1   | Data structures, strings, functions, modules, classes/OOP, exceptions and code reading. |
| Stage 2   | Light use only; C/C++ remains dominant for embedded work.                               |
| Stage 3   | Linux scripting, files, processes, serial communication, environments and packages.     |
| Stage 4   | Sockets, TCP/UDP clients/servers, HTTP, MQTT, JSON and API use.                         |
| Stage 5   | ROS 2 Python nodes and structured robotics software.                                    |
| Stage 6   | NumPy, image arrays and OpenCV.                                                         |
| Stage 7   | Jupyter, Pandas, Matplotlib, datasets, ML workflows and PyTorch/tensors.                |
| Stage 8   | MAVLink/ROS tooling, telemetry analysis and high-level autonomy where appropriate.      |

## Python Engineering Data Skills

* NumPy arrays and vectorized operations.
* Pandas DataFrames and engineering-log analysis.
* Matplotlib for engineering visualization.
* Jupyter notebooks for experiments and analysis.
* CSV and JSON.
* Basic SQL/SQLite only when useful for telemetry/data storage.
* Basic statistics required for interpreting experiments and later ML.

```text
Python list → NumPy array → image array → tensor → ML / computer vision
```

This progression is deliberately designed to make later ML code less mysterious by building the underlying data and software concepts first.

# 13. Longitudinal Track B — Code Literacy

Reading professional code is a distinct skill and a major objective of the curriculum. Every programming stage should contain both code-writing and code-reading tasks.

| **Level** | **Code Literacy Target**                                                                  |
| --------- | ----------------------------------------------------------------------------------------- |
| CL1       | Read and explain own code.                                                                |
| CL2       | Read tutorial/example code without running it first.                                      |
| CL3       | Trace unfamiliar structured code across functions and files.                              |
| CL4       | Navigate a library: public API → header/module → implementation.                          |
| CL5       | Navigate a professional open-source project and trace a feature through multiple modules. |

* Identify where a function/class originates.
* Trace arguments and return values.
* Follow object creation and method calls.
* Use IDE navigation: go to definition, references, call hierarchy and search.
* Read documentation beside source code.
* Trace one Arduino library call from API to implementation.
* Later trace a ROS package, OpenCV call, PyTorch training pipeline, and selected ArduPilot/PX4 modules.

# 14. Stage 0 — Engineering Environment, Git and Baseline

## Objectives

* Create a professional development workspace.
* Use Git/GitHub for version control.
* Understand source → preprocess → compile → link → executable.
* Understand the purpose of headers/source files at a basic level.
* Establish documentation habits.
* Run a short baseline to identify what can be accelerated in Stage 1.

## Topics

* Repository, clone, add, commit, push, pull, branch, merge and .gitignore.
* VS Code/project structure.
* Compiler, linker, build errors and runtime errors.
* README structure and engineering notes.
* Basic command-line navigation sufficient for development.

## Exit Evidence

* Create and push a small C/C++ project repository.
* Make a branch, change code, merge it and explain the history.
* Compile a simple program outside Arduino IDE.
* Explain what .h/.cpp files do at a basic level.
* Create the master repository structure.

# 15. Stage 1 — C/C++ + Electronics + Light Python

This is the foundation stage and should not be rushed merely to reach robotics sooner.

## 15.1 C/C++ Core

* Variables, constants, data types, casts and operators.
* Scope and lifetime.
* Conditions, loops and functions.
* Arrays and strings, including C strings versus C++ strings.
* Structs and enums.
* References.
* Memory addresses, pointers, dereferencing and nullptr.
* Stack versus heap and dynamic memory concepts.
* Classes, objects, constructors/destructors and encapsulation.
* Composition, inheritance and polymorphism at an appropriate foundation level.
* Headers/source files, namespaces and basic STL containers.
* State machines, event-driven thinking and non-blocking logic.
* Debugging and assertions.
* C/C++ Integration and C Literacy:

Stage 1 uses **C++ as the primary programming language**, while deliberately developing the C literacy required for embedded systems, robotics, Linux, systems programming, and hardware-oriented engineering.

The learner is not expected to complete two independent introductory language courses. Instead, C concepts will be introduced and reinforced when they provide important understanding of programming, memory, compilation, embedded development, or existing codebases.

Stage 1 should expose the learner to both C and C++ code and progressively develop the ability to:

1. Understand variables, data types, expressions, operators, control flow, functions, scope, and lifetime.
2. Understand arrays and contiguous memory.
3. Understand pointers, addresses, dereferencing, pointer arithmetic, and pointer/array relationships.
4. Understand structures and enumerations.
5. Read and work with C-style strings and character arrays.
6. Understand basic C I/O such as printf() and format specifiers.
7. Understand the purpose and risks of manual dynamic memory management using malloc(), calloc(), realloc(), and free().
8. Understand headers, source files, compilation, linking, object files, and executable generation.
9. Read and explain basic existing C code, including code containing arrays, structs, pointers, and C strings.
10. Understand how modern C++ approaches concepts that may otherwise be handled manually in C, including references, std::string, containers, RAII, and smart pointers.

The objective is not to memorize the C standard library. The objective is to develop enough C literacy to understand, debug, modify, and reason about C code encountered in embedded systems, robotics, Linux, libraries, and mixed C/C++ projects.

C and C++ should therefore be learned as connected engineering tools, with C++ providing the primary modern development environment and C providing essential low-level literacy.

## 15.2 Electronics Core

* Voltage, current, resistance and power.
* Ohm's law; series/parallel circuits; Kirchhoff intuition.
* Resistors, potentiometers, LEDs and diodes.
* Capacitor fundamentals: charge/discharge, decoupling, bulk capacitance and filtering.
* BJT and MOSFET fundamentals and switching use.
* Relays and flyback protection.
* Voltage-regulation basics.
* Pull-up/pull-down resistors and switch debouncing.
* ADC, PWM, logic levels, current limits, grounding and noise.

## 15.3 Light Python Foundation

* Lists, tuples, dictionaries and sets with real understanding.
* Strings and slicing.
* Functions and arguments.
* Comprehensions.
* Modules/imports/packages.
* Classes/OOP sufficient to read structured Python.
* Exceptions and file handling.
* Short code-reading exercises rather than another full beginner Python course.

## 15.4 Stage 1 Project

Build an ESP32 sensor/actuator module containing an IMU or other digital sensor, at least one additional sensor/input, controlled load or motor, LEDs/buttons and appropriate power/interface circuitry.

* At least one sensor must be accessed from its datasheet without relying on its normal high-level Arduino library.
* Implement I²C or SPI communication and create a small reusable C++ driver/library.
* Document circuit reasoning: resistor/capacitor/transistor choices and expected behavior.
* Include one Python-side utility or analysis task only if it supports the project.

## 15.5 Exit Gate

* Explain and use pointers/references at foundation level.
* Read a moderately simple Arduino library and trace a method call.
* Explain pull-up, decoupling, ADC, PWM and transistor/MOSFET switching.
* Compare UART, I²C and SPI.
* Write structured multi-file C++ code.
* Read a structured Python class/module without being blocked by syntax.
* Read and explain basic C code involving arrays, structs, pointers, C strings, and manual memory-management concepts.
* Explain the conceptual differences between common C approaches and modern C++ approaches, including C strings vs. std::string, raw/manual memory management vs. RAII/smart pointers, and pointer-based vs. reference-based parameter passing.

# 16. Stage 2 — Embedded Systems / ESP32

* CPU, Flash, RAM and register concepts.
* GPIO, ADC, PWM, timers and interrupts.
* UART/I²C/SPI at deeper implementation level.
* Watchdog timers.
* Polling versus interrupt-driven designs.
* FreeRTOS: tasks, scheduler, priorities, queues, semaphores and mutexes.
* Shared-state/concurrency problems.
* Timing and non-blocking architecture.

## Project / Exit Gate

Refactor Stage 1 into a structured embedded application with separate acquisition, control, communication and logging responsibilities. Use FreeRTOS where it adds value, pass data safely, and demonstrate diagnosis of timing/blocking problems.

# 17. Stage 3 — Raspberry Pi and Linux

* Linux versus Bash versus terminal.
* Filesystem, users, groups and permissions.
* Processes, signals, services and logs.
* Package management and environment variables.
* Device files and serial devices.
* SSH/SCP and key-based authentication.
* Pipes, redirection and Bash scripting.
* systemd services.
* Python virtual environments and package management in practical use.
* Headless operation and troubleshooting.

## Project / Exit Gate

Operate a Raspberry Pi headlessly. Automatically start a Python/C++ engineering application with systemd, communicate with the ESP32, log data, and diagnose service/permission/device failures using Linux tools.

# 18. Stage 4 — Networking and IoT

* MAC, frames, packets and payloads.
* IPv4, private/public addressing, subnet masks and gateways.
* DHCP, DNS, NAT and routing intuition.
* Ports and sockets.
* Client/server architecture.
* TCP versus UDP.
* HTTP/REST.
* MQTT.
* JSON; WebSockets only if useful.
* Wireshark and packet inspection.

## Required Labs

1. Laptop ↔ Raspberry Pi over UDP.
2. Repeat over TCP and compare behavior.
3. ESP32 → Raspberry Pi over UDP.
4. ESP32 → Raspberry Pi over TCP.
5. Create a simple HTTP/REST interface.
6. Publish/subscribe sensor data using MQTT.
7. Capture traffic and identify IPs, ports, protocol and payload in Wireshark.

## Project / Exit Gate

Create a network-connected robot in which a laptop communicates through Wi-Fi with a Raspberry Pi, which communicates with an ESP32 controlling sensors/actuators. Be able to explain and diagnose each communication layer.

# 19. Stage 5 — ROS 2 and Robotics

Focus on ROS 2. ROS 1 is awareness/history, not a parallel curriculum.

* Workspace, package and build concepts.
* Nodes, topics, publishers/subscribers and messages.
* Parameters.
* Services and actions.
* Launch files.
* rosbag and rqt.
* RViz.
* TF coordinate frames.
* URDF.
* Simulation concepts.
* Encoders and odometry.
* Localization, mapping and navigation concepts.
* Nav2 fundamentals.

## Just-in-Time Math

* Trigonometry for odometry.
* Vectors and coordinate frames.
* Matrices/transforms only when TF and robot geometry require them.

## Project / Exit Gate

Convert the rover into a ROS 2 system. The Pi hosts ROS nodes; the ESP32 retains low-level embedded responsibilities. Build packages independently, visualize/record data, model the robot and demonstrate basic mobile-robot behavior.
# 20. Stage 6 — Computer Vision

* Pixels, resolution, channels and image arrays.
* RGB/BGR/HSV.
* Thresholds and masks.
* Kernels/convolution intuition.
* Blur, edge detection and morphology.
* Contours.
* Camera calibration.
* Intrinsic/extrinsic parameters.
* Perspective.
* ArUco markers.
* Feature detection and tracking.

## Project / Exit Gate

Add a camera to the rover. Detect/track an object or marker, estimate useful position/pose information, publish it through ROS 2 and make robot behavior depend on perception.

# 21. Stage 7 — Machine Learning, PyTorch and Edge AI

This stage formalizes ML after programming, data handling and computer vision foundations exist. Data Science is not a prerequisite; only the relevant engineering-data skills are required.

* Dataset, feature and label.
* Training, validation, test and inference.
* Regression, classification and clustering foundations.
* Loss, optimization and regularization concepts.
* Accuracy, precision, recall and appropriate metrics.
* Overfitting/underfitting.
* Neural-network foundations.
* Activation functions and gradient-descent intuition.
* CNN foundations.
* PyTorch: tensors, datasets/dataloaders, nn.Module, forward pass, loss, optimizer and training loop.
* Object detection / segmentation concepts as relevant.
* Model export/optimization and edge inference.

## PyTorch in One Sentence

PyTorch is a Python-based machine-learning/deep-learning framework used to represent data as tensors, define neural networks, train them using automatic differentiation/optimizers, evaluate them and deploy/export models.

## Project / Exit Gate

Build an AI perception node whose output changes robot behavior. Trace one training script end-to-end: dataset → DataLoader → model → loss → backward pass → optimizer → evaluation → export/inference.

# 22. Stage 8 — UAV Systems and Autonomy

## 22.1 Hardware and Flight Architecture

* Frame, propellers, motors, ESCs and battery/power system.
* Flight controller.
* IMU, GPS, compass and barometer.
* Telemetry and RC system.
* Roll, pitch, yaw and throttle.
* Attitude, altitude and position.
* Flight modes, waypoint missions, return-to-launch and failsafes.

## 22.2 Autopilot / GCS

* ArduPilot as the first deep ecosystem.
* Mission Planner setup, calibration, parameters, modes, waypoints, geofence, failsafes and logs.
* MAVLink fundamentals.
* PX4 studied after the first ecosystem is comfortable, primarily for comparison and ROS 2/autonomy integration.
* Simulation/SITL is used before risky hardware tests whenever possible.

## 22.3 Companion Computer and Autonomy

* Raspberry Pi or similar companion computer.
* Flight-controller communication.
* ROS 2/high-level software as appropriate.
* Vision and AI inference.
* Mission-level decisions and offboard/high-level autonomy.

## Capstone Direction

Autonomous vision-guided UAV: take off, execute a mission, detect a target/landing marker, estimate its position, approach and perform an autonomous precision task such as landing.

# 23. Mathematics Policy

Formal mathematics is deferred, but mathematics is not avoided. Required concepts are learned just-in-time so that theory immediately connects to engineering.

| **Engineering Context**    | **Math Introduced**                               |
| -------------------------- | ------------------------------------------------- |
| ADC/digital representation | Binary representation, scaling and resolution     |
| RC circuits                | Exponential behavior intuition                    |
| Mechanisms/motors          | Algebra, ratios, torque/speed/power relationships |
| Odometry                   | Trigonometry                                      |
| ROS TF / robot geometry    | Vectors, matrices and coordinate transforms       |
| Camera pose                | Geometry and transformations                      |
| Robot arms later           | Forward/inverse kinematics                        |
| UAV orientation            | Euler angles and quaternions                      |
| Control                    | Derivative/integral intuition and feedback        |
| Sensor fusion later        | Probability and estimation concepts               |

# 24. Resource and Course Policy

The curriculum controls the courses. Courses do not control the curriculum.

* Use one primary formal course at a time.
* Skip or accelerate material already demonstrated at competency level.
* A certificate is not, by itself, a reason to complete a learning path.
* Use official documentation as a normal engineering reference.
* Use LinkedIn Learning and short tutorials to close specific gaps rather than create parallel curricula.

# 25. Existing Course / Learning-Path Classification

| **Resource / Track**                                        | **Classification**         | **Placement / Decision**                                                                                                  |
| ----------------------------------------------------------- | -------------------------- | ------------------------------------------------------------------------------------------------------------------------- |
| LinkedIn Learning — C Programming Basics                    | Core / selective           | Stage 1. Use modules that repair real C foundations; skip demonstrated basics.                                            |
| LinkedIn Learning — Advanced C Programming                  | Core / selective           | Stage 1, after foundations. Focus on memory, pointers, data handling and professional patterns relevant to embedded work. |
| LinkedIn Learning — C Programming for Embedded Applications | Core                       | Stage 1→2 bridge. Apply directly to ESP32/embedded projects.                                                              |
| Coursera — Python 3 Programming path                        | Supporting / selective     | Use only modules that strengthen data structures, OOP, modules, code reading or other demonstrated gaps.                  |
| Coursera — Python for Everybody                             | Reference / skip full path | Do not pursue the full certificate unless a later baseline shows major Python fundamentals are missing.                   |
| Coursera — Stanford Machine Learning path                   | Core later                 | Stage 7. Formal ML foundation.                                                                                            |
| PyTorch learning material                                   | Core later                 | Stage 7, after ML and Python/data foundations.                                                                            |
| Coursera — IBM Data Science path                            | Optional / deferred        | Do not complete for the certificate alone. Extract useful data-handling modules if needed.                                |
| Web development                                             | Future Supporting          | Post-core backlog, or minimum just-in-time work for an engineering dashboard/API.                                         |
| App development                                             | Future Supporting          | Post-core backlog, or minimum just-in-time work for robot/IoT/UAV interface needs.                                        |

# 26. Resource Roles

| **Source**             | **Role**                                                                                |
| ---------------------- | --------------------------------------------------------------------------------------- |
| Coursera               | Primary structured learning where a suitable course maps directly to a core competency. |
| LinkedIn Learning      | Focused, practical gap filling and selected programming/embedded material.              |
| Microsoft Learn        | Later Microsoft/cloud/IoT tooling and targeted modules where useful.                    |
| Official documentation | Authoritative engineering reference and source for professional tool/API behavior.      |
| Books                  | Deep explanation when a stage benefits from a durable reference.                        |
| YouTube / tutorials    | Clarification and alternative explanation; avoid playlist accumulation.                 |

# 27. Anti-Distraction System

## 27.1 Parking Lot Rule

Interesting ≠ study now.

Any newly discovered technology, course, framework or topic that is not required for the current stage is recorded in the Future Development Backlog. It does not enter the active weekly plan.

## 27.2 Scope-Change Test

A new topic may enter the active stage only if at least one is true:

* It is a prerequisite for a current competency.
* It is required to complete the current project safely or correctly.
* It resolves a demonstrated gap that is blocking progress.
* It replaces an existing resource more efficiently without expanding scope.

## 27.3 No Catch-Up Debt

Missed study time is not carried as debt. Resume from the current checkpoint. The goal is sustained development over many months, not perfect weekly compliance.

# 28. Future Development Backlog — Not Active Now

These are valuable skills that fit the long-term profile, but they are deliberately parked until the core curriculum is completed or a core project requires a small just-in-time subset.

| **Future Skill**                      | **Why It Matters**                                                                                            | **Current Status**                                                       |
| ------------------------------------- | ------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------ |
| Software engineering practices        | Testing, logging, configuration, dependencies, documentation, architecture and CI/CD improve maintainability. | Backlog; basic good practice may appear naturally.                       |
| CAN / Modbus / RS-485                 | Important engineering/industrial/robotics communication protocols.                                            | Backlog.                                                                 |
| Electronics diagnostic tools          | Oscilloscope and logic-analyzer depth enables signal-level debugging.                                         | Backlog; multimeter use is already part of core electronics.             |
| PCB design / KiCad                    | Moves prototypes from breadboard to engineered hardware.                                                      | Backlog.                                                                 |
| Docker                                | Reproducible Linux/ROS/AI environments and deployment.                                                        | Backlog.                                                                 |
| Databases beyond basic need           | Telemetry and application data storage.                                                                       | Backlog; minimal SQLite/SQL may appear in Python Data Skills.            |
| API engineering depth                 | REST/WebSockets and service architecture.                                                                     | Backlog; minimum REST/JSON appears in networking.                        |
| Cybersecurity fundamentals            | Secure connected/IoT systems.                                                                                 | Backlog; minimum safe practices may be introduced when needed.           |
| Advanced simulation                   | Deeper Gazebo/SITL workflows.                                                                                 | Backlog; basic simulation appears in ROS/UAV core.                       |
| Advanced control systems              | Feedback, stability and controller design.                                                                    | Backlog after core; basic control is introduced just-in-time.            |
| Advanced sensor fusion                | Kalman/EKF and multi-sensor estimation.                                                                       | Backlog after core; concepts appear when UAV work requires them.         |
| Mechanical robotics integration depth | Mechanisms, bearings, gearboxes, tolerances, vibration and design optimization.                               | Backlog/ongoing strength; use existing mechanical expertise in projects. |
| Web development                       | Full web-development skill stack.                                                                             | Backlog; engineering dashboard only if needed.                           |
| App development                       | Native/cross-platform app-development depth.                                                                  | Backlog; engineering interface only if needed.                           |

# 29. Master Project Progression

1. Basic C/C++ and electronics experiments
   ↓
2. ESP32 sensor/actuator module
   ↓
3. Structured FreeRTOS embedded controller
   ↓
4. ESP32 ↔ Raspberry Pi edge system
   ↓
5. Network-connected rover
   ↓
6. ROS 2 rover
   ↓
7. Vision-guided rover
   ↓
8. AI-enabled autonomous rover
   ↓
9. UAV simulation / autopilot ecosystem
   ↓
10. Companion-computer autonomous UAV
# 30. Engineering Documentation Standard

Every meaningful project/experiment should record:

* Objective and expected behavior.
* Relevant theory.
* Hardware/software architecture.
* Circuit diagram and/or mechanical design where relevant.
* Source code and version.
* Datasheets/references.
* Measurements/test procedure.
* Observed results.
* Failures and symptoms.
* Debugging process.
* Root cause and correction.
* What was learned.
* Next improvement.

# 31. Multi-Chat Organization System

A stage is not tied to one chat. Large stages may span multiple chats to keep conversations responsive, searchable and focused. The stage remains one continuous learning unit even when the conversation is split.

## 31.1 Recommended Project Chat Structure

| **Chat Type**           | **Example Name**                                        | **Purpose**                                                                        |
| ----------------------- | ------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| Master reference        | 00 — Master Roadmap                                     | Only overall roadmap decisions, major scope changes and master-document revisions. |
| Stage chat — part 1     | 01A — Stage 1 C/C++ & Electronics — Foundations         | Begin the stage, baseline, first lessons and early exercises.                      |
| Stage chat — part 2     | 01B — Stage 1 C/C++ & Electronics — Memory & Components | Continue the same stage when the first chat becomes long.                          |
| Stage chat — project    | 01P — Stage 1 Capstone                                  | Optional dedicated build/debugging chat if the project becomes extensive.          |
| Stage chat — assessment | 01X — Stage 1 Checkpoint                                | Optional focused competency assessment and gap remediation.                        |

## 31.2 Naming Convention

```text
00 — Master Roadmap
01A — Stage 1 — Part A
01B — Stage 1 — Part B
01P — Stage 1 — Project
02A — Stage 2 — Part A
...
08P — Stage 8 — UAV Capstone
```

The letters are optional. The important requirement is that the stage number and purpose are obvious.

## 31.3 Stage Progress Record

To allow one stage to span multiple chats, each stage should maintain a short living progress record. At the end of a substantial chat or before moving to a new chat, update this record.

| **Field**                      | **What to Record**                                    |
| ------------------------------ | ----------------------------------------------------- |
| Stage / version                | Example: Stage 1, Progress Record v3                  |
| Completed competencies         | Specific items demonstrated, not just lessons watched |
| Current competency level       | L1/L2/L3/L4 where useful                              |
| Projects/experiments completed | What was built and tested                             |
| Current project state          | Hardware/software status and unresolved issues        |
| Courses/resources used         | Course/module names and completed relevant sections   |
| Code literacy work             | Libraries/codebases traced and what was understood    |
| Known gaps                     | Concepts that still need work                         |
| Decisions made                 | Architecture, tools, skipped modules, substitutions   |
| Next exact step                | The first task for the next chat/session              |

## 31.4 Starting a New Chat Within the Same Stage

Use a compact handoff prompt such as:

> This chat continues Stage 1 of the Master Curriculum.
> Use the Master Curriculum project resource as the governing reference.
> Continue from the latest Stage 1 Progress Record.
> Do not restart completed material unless the progress record identifies a gap.
> Keep the work competency-based and within the active stage scope.

If the project environment allows the Master Curriculum and latest Stage Progress Record to remain available as project resources, use those resources rather than copying the entire previous chat.

## 31.5 When to Split a Stage Into Another Chat

* The current chat has become very long or difficult to navigate.
* The stage moves from theory/labs into a large capstone project.
* A debugging thread is becoming extensive and deserves isolation.
* A formal checkpoint/remediation session would be clearer separately.
* The subject remains the same stage; splitting the chat does not imply stage completion.

## 31.6 What Must Not Happen When Starting a New Chat

* Do not restart the stage from lesson one by default.
* Do not silently change the curriculum or add new topics.
* Do not assume a certificate/module equals competency.
* Do not lose unresolved project/debugging context; put it in the Stage Progress Record first.
* Do not move to the next stage until the agreed exit gate is met or an explicit decision is made to defer a gap.

# 32. Weekly Operating Model

A normal week should be small enough to survive real life.

| **Session Type**               | **Typical Duration** | **Typical Use**                       |
| ------------------------------ | -------------------: | ------------------------------------- |
| Short workday session 1        |            30–45 min | Theory / course                       |
| Short workday session 2        |            30–45 min | Exercise / code reading               |
| Optional third workday session |            30–45 min | Review, documentation or debugging    |
| Day-off focused block          |            1.5–2.5 h | Hardware/project integration          |
| Optional second day-off block  |            45–90 min | Project continuation or consolidation |

Not every slot must be used every week. A 4–5 hour week is successful. If 6–7 hours are available, use the extra time mainly for hands-on consolidation rather than adding a new subject.

# 33. Example Stage 1 Week

| **Session**        | **Task**                                                                            |
| ------------------ | ----------------------------------------------------------------------------------- |
| 30–45 min          | C/C++ concept: data types, operators or functions.                                  |
| 30–45 min          | Read a short unfamiliar C/C++ code sample and trace it.                             |
| 30–45 min          | Electronics theory: voltage/current/resistance and one calculation.                 |
| 1.5–2 h            | Breadboard experiment: LED/resistor, measurements and comparison with calculations. |
| 30–45 min optional | Python code-reading/data-structure exercise or project documentation.               |

This example illustrates the intended scale: focused, connected and finishable.

# 34. Initial Four-Week Direction

| **Week** | **C/C++**                              | **Electronics**                  | **Python / Code Literacy**                       | **Hands-On**                        |
| -------- | -------------------------------------- | -------------------------------- | ------------------------------------------------ | ----------------------------------- |
| 1        | Variables, types, operators, functions | V/I/R/P; Ohm's law               | Read simple functions and data structures        | LED/resistor measurements           |
| 2        | Arrays, strings, structs               | Series/parallel; voltage divider | Lists/dicts/strings; compare data representation | Divider + sensor-data program       |
| 3        | Addresses, pointers, references        | Capacitors and RC behavior       | Trace object/reference behavior conceptually     | Capacitor charge/filter experiments |
| 4        | Classes, headers, .cpp                 | Diode/BJT/MOSFET intro           | Read a simple Python class/module                | Microcontroller-controlled load     |

At the end of the first four weeks, perform a practical checkpoint rather than a conventional exam.

# 35. Assessment Method

Checkpoints should mix four forms of evidence:

1. Explain: answer conceptual questions in own words.

2. Read: inspect unfamiliar code/circuit/architecture and explain it.

3. Build: implement a small task without copying a complete solution.

4. Diagnose: troubleshoot an intentionally broken or realistically failing system.

5. A weak checkpoint does not mean failure. It identifies exactly which competencies need another cycle before moving on.

# 36. Deferred Academic / Research Track

Formal PhD preparation is intentionally deferred while technical foundations are strengthened. When activated later, it can include formal mathematics, research methodology, literature review, academic writing, research-gap identification, experimental design and paper reproduction.

* Formal linear algebra.
* Calculus and differential equations.
* Probability/statistics at research depth.
* Optimization.
* Research methods and experimental design.
* Literature search/review.
* Academic writing.
* Reproducing and extending published work.

# 37. Success Criteria for the Core Journey

* Read and structure non-trivial C/C++ and Python code with much less dependence on tutorials.
* Understand common electronic components and reason about their role in real circuits.
* Design and debug embedded interfaces rather than only connect modules.
* Use Raspberry Pi/Linux confidently as an engineering computer.
* Understand TCP/IP and IoT communication rather than treating Wi-Fi as a black box.
* Build ROS 2 software with clear nodes/interfaces and understand core mobile-robot concepts.
* Build classical computer-vision pipelines and integrate them with robot behavior.
* Understand ML workflows and read/write foundational PyTorch training/inference code.
* Deploy intelligent perception to edge/robot systems.
* Understand UAV hardware/software architecture and operate an autopilot/GCS ecosystem.
* Integrate a companion computer and progress toward autonomous UAV behavior.
* Use documentation, source code, datasheets, measurements and diagnostic tools as normal engineering practice.

# 38. Final Operating Rules

1. Stay on the current stage.
2. Use the Parking Lot for interesting but non-required topics.
3. One primary formal course at a time.
4. Certificates are secondary to competency.
5. Normal weekly target is 4–5 hours; never create catch-up debt.
6. Use 6–7 hour weeks for consolidation, not scope expansion.
7. Every stage can span multiple chats.
8. Maintain a Stage Progress Record before changing chats.
9. Do not advance merely because the target window ended; use the exit gate.
10. Do not demand perfection before moving on: unresolved non-critical gaps may be documented and revisited deliberately.
11. Keep the master project evolving so skills connect rather than remain isolated.
12. Do not modify the master scope for every new technology encountered.

# 39. Recommended First Action

Add this Master Curriculum v1.2 as a project resource. Keep the current master-roadmap chat as a reference. Then open a dedicated Stage 0 chat and begin with the Stage 0 baseline/environment setup. When Stage 0 becomes long, continue it in a second Stage 0 chat using the Stage Progress Record rather than restarting.

Suggested opening message:

> This chat is for **Stage 0 — Engineering Environment, Git and Baseline**.
> Use **Master Curriculum v1.2** as the governing project resource.
> Guide me one step at a time, keep the workload compatible with the weekly limits in the curriculum, and maintain a **Stage Progress Record** so this stage can continue across multiple chats if needed.
> Follow the **Engineering Documentation & Portfolio** requirements in the Master Curriculum throughout the stage. Help me document my work as I go rather than leaving documentation until the end, and tell me when something should be committed to GitHub, captured as evidence, or added to the portfolio record.

39. Longitudinal Track C — Engineering Documentation & Portfolio

Before starting or recommending tools, software versions, courses, frameworks, or technical resources for this stage, verify that they are still current and appropriate. Preserve the stage competencies and objectives even if the specific tools or resources have changed.

## Purpose

Documentation is treated as part of engineering work, not as an optional activity performed after a project is finished. The goal is to ensure that every meaningful stage leaves durable evidence of capability, decisions, debugging and results, while keeping the workload light enough to remain sustainable.

## Core workflow

**Capture → Document → Commit → Demonstrate → Share selectively**

* Capture during the work: photos, screenshots, measurements, circuit/CAD views, important errors and short notes.
* Document the engineering story: objective, architecture, implementation, tests, failures, debugging, results and lessons learned.
* Commit technical evidence to Git/GitHub in an organized repository.
* Demonstrate significant projects with a short video, GIF, screenshots or test evidence where appropriate.
* Share selectively on LinkedIn when a project, experiment or learning milestone has a useful engineering story. Certificates alone should not dominate the profile.

## Portfolio layers

* **GitHub** — technical evidence and engineering archive. Repositories should contain readable code, a useful README, diagrams/results where relevant, and enough context for another engineer to understand the work.
* **LinkedIn** — visibility and professional storytelling. Use it to explain what was built, why it mattered, a challenge encountered, what was learned and where the technical evidence can be found.
* **Curated portfolio website** — deferred until after the core curriculum unless there is a concrete need. Eventually it should showcase only the strongest projects rather than duplicate every repository.

## Minimum documentation standard for meaningful projects

* Project title and one-paragraph purpose/problem statement.
* System architecture or block diagram when useful.
* Hardware/software list and key design decisions.
* Source code with meaningful commits.
* At least a few useful photos/screenshots/plots or other evidence.
* Test method and result.
* One or more challenges/failures and how they were diagnosed.
* What was learned and what would be improved next.
* Short demonstration media for major stage projects when practical.

## Stage-by-stage portfolio expectations

* **Stage 0:** Create/clean GitHub profile, establish repository/README template, learn commits, and create a portfolio index repository or equivalent project index.
* **Stage 1:** Document core electronics/programming experiments and publish the first properly structured capstone repository.
* **Stage 2:** Show embedded architecture, timing/task design, test evidence and debugging notes.
* **Stage 3:** Document Linux deployment, service configuration, logs and Pi↔ESP32 integration.
* **Stage 4:** Include network architecture, protocol choices, packet/Wireshark evidence and communication tests.
* **Stage 5:** Document ROS graph/architecture, packages, robot model, visualization and demonstrations.
* **Stage 6:** Include vision pipeline, calibration/processing evidence and measured behavior.
* **Stage 7:** Document dataset/model workflow, evaluation metrics, inference pipeline and limitations.
* **Stage 8:** Produce a polished UAV/autonomy capstone record suitable for employers, collaborators or future academic discussion.

## Documentation time policy

Documentation does not create a new weekly study track. It is included inside project time. As a rule of thumb, reserve roughly the final 15–30 minutes of a meaningful build/test session for commits, notes, photos and README updates. Major projects may require a separate short polishing session at completion.

Do not postpone all documentation until the end of a stage; important evidence and debugging details are easiest to capture while they are fresh.

## Recovering previous projects

Do not interrupt the core curriculum to reconstruct every old project. Create an Old Projects Recovery List and classify remembered projects as:

* **A — Portfolio worthy:** strong project with enough surviving code/photos/files to reconstruct properly.
* **B — Mention worthy:** preserve a short description and available evidence without a major reconstruction effort.
* **C — Historical only:** record the name/idea and move on.

Recover only a small number of the strongest old projects gradually. Future work takes priority over perfect reconstruction of the past.

## Portfolio quality gate

For major stage projects, completion evidence should include both technical competency and adequate documentation. A project does not need marketing polish, but it should be understandable, reproducible enough for its purpose, and supported by evidence of results.

# 40. v1.2 Change Summary and Scope Freeze

Version 1.2 adds Engineering Documentation & Portfolio as a third longitudinal track. It does not add a new technical subject or increase the planned weekly workload. GitHub is the primary technical record, LinkedIn is the selective visibility/storytelling layer, and a dedicated portfolio website remains deferred.

After v1.2, the Master Curriculum is considered scope-frozen. New technical interests should normally enter the Future Development Backlog rather than trigger another master-plan revision.

**END OF MASTER CURRICULUM v1.2**
