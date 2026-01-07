In this activity, a snake-like modular robot is simulated in CoppeliaSim and controlled using ROS 2. The robot consists of multiple articulated modules whose joints are coordinated to generate sinusoidal locomotion, mimicking real snake movement.

Robot Behavior:

🐍 Sinusoidal Locomotion
The robot generates wave-like motion by synchronizing vertical and horizontal joints across its body, allowing smooth forward propulsion.

🎮 Velocity-Based Control
High-level motion commands are sent using Twist messages, where:

- Linear velocity controls forward speed.
- Angular velocity controls turning behavior.

🧠 Head Orientation Control
A dedicated command topic controls the head joint angle independently, enabling directional stability during movement.

⏱️ Patterned Motion Execution
A command node sends timed movement patterns, causing the robot to move forward for a fixed duration and then stop autonomously.

🔗 ROS 2 – CoppeliaSim Integration
The system uses the CoppeliaSim ZMQ Remote API to directly command joint positions while publishing joint states through ROS for real-time feedback.
