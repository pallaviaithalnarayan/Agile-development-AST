# Agile-development-AST

## Project Overview

This project demonstrates an agile development approach for autonomous robotic systems using Isaac Sim as the primary simulation environment. The framework enables the development and testing of mobile robots with capabilities for navigation, perception, manipulation, and human-robot interaction in simulated environments before deployment to physical systems.

## Core Components

### IsaacSim (Main Project)
The primary simulation environment where the robot's behavior and interactions are tested and validated:
- **Simulation Environment**: `robile_simulation.usd` provides a realistic testing environment
- **URDF Models**: Robot configuration files for accurate physical simulation
- **Workspace**: Complete ROS2 workspace for simulation and development

### Supporting Components
The project consists of several smaller tasks and components:

1. **ROS1 SMACH**
   - Implementation of state machines using the ROS1 framework
   - Provides basic robot behavior control 

2. **ROS2 AST**
   - ROS2-based packages for core robot functionality:
     - `pkg_move`: Navigation module
     - `pkg_perceive_plane`: Environmental perception 
     - `pkg_pick`: Object pickup module
     - `pkg_place`: Object placement module

3. **ROS2 SMACH**
   - Modern state machine implementation using ROS2
   - Manages robot behavior across different scenarios
   - Includes testing framework

4. **Source Control & Issue Management**
   - Development workflow management
   - Selected packages for version control testing

5. **UML Observer**
   - System design and modeling
   - UML diagrams for component relationships

## Project Structure

```
Agile-development-AST/
├── IsaacSim/                          # Main project
│   ├── robile_simulation.usd          # Simulation environment
│   ├── simulators.ipynb               # Jupyter notebook for simulation control
│   ├── URDF/                          # Robot models
│   │   ├── 4_wheel_config.urdf        # Four-wheel robot configuration
│   │   ├── model-2.urdf               # Alternate robot model
│   │   └── ...
│   └── simulation_ws/                 # ROS2 workspace for simulation
│       ├── build/                     # Build directory
│       ├── install/                   # Install directory
│       ├── log/                       # Log files
│       └── src/                       # Source code
├── ros1_smach/                        # ROS1 state machine implementation
├── ros2_ast/                          # Core ROS2 packages
│   └── src/
│       ├── pkg_move/                  # Navigation module
│       ├── pkg_perceive_plane/        # Environment perception
│       ├── pkg_pick/                  # Object pickup module
│       └── pkg_place/                 # Object placement module
├── ros2_smach/                        # ROS2 state machine implementation
│   ├── src/
│   │   └── state_machine/
│   └── test/
│       └── test_state_machine.py
├── source_control_issue_management/   # Development workflow
├── uml_observer/                      # System design documentation
├── user_stories/                      # Project requirements as user stories
├── software_requirements.md           # Detailed software requirements
└── robot_software_architecture.jpg    # Architecture diagram
```

## User Stories

The project implements several key user stories for autonomous robot operation:

1. Human-Robot Communication for Task Assignment
2. Task Status Tracking via Human-Robot Communication
3. Object Delivery to Location
4. User Feedback Collection
5. Object Detection and Manipulation
6. Location Specification via Voice Command
7. Navigate to Destination
8. Obstacle Avoidance
9. User Notification on Arrival
10. Task Completion Confirmation

## Getting Started

### Prerequisites

- Isaac Sim (2022.1.0 or newer)
- ROS2 (Foxy or newer)
- ROS1 Noetic (for ROS1 SMACH components)
- Python 3.8+

### Installation

1. Clone the repository:
   ```
   git clone https://your-repository-url/Agile-development-AST.git
   ```

2. Set up Isaac Sim environment:
   ```
   # Install Isaac Sim according to NVIDIA documentation
   # Configure the Python path for Isaac Sim
   ```

3. Build the ROS2 workspace:
   ```
   cd Agile-development-AST/IsaacSim/simulation_ws
   colcon build
   ```

4. Source the workspace:
   ```
   source install/setup.bash  # For bash
   source install/setup.ps1   # For PowerShell
   ```

### Running the Simulation

1. Start Isaac Sim and load the simulation environment:
   ```
   # Launch Isaac Sim
   # Open robile_simulation.usd
   ```

2. Launch the robot state machine:
   ```
   ros2 launch state_machine robot_task.launch.py
   ```

## Development Methodology

This project follows agile development methodologies with:
- User story-driven development
- Component-based architecture
- Continuous integration with simulation-based testing
- Iterative implementation cycles

