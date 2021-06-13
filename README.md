
# gazebo_demo_workshop

A simple demo of Gazebo basics. A simple building or a workshop with two simple robot can be found. The robot has two wheels and a castor wheel. Also there is a plugin to display welcome message  with in this gazebo world.  

### Directory Structure
```
gazebo_demo_workshop 	# main project folder
├── CMakeLists.txt      # cmake file for compiling the welcome message script
├── LICENSE
├── README.md
├── model		# Model files for simple robot and a simple house
│   ├── Building
│   │   ├── model.config
│   │   └── model.sdf
│   └── two_wheel_robot
│       ├── model.config
│       └── model.sdf
├── script
│   └── welcome_message.cpp  # Gazebo World plugin C++ script
└── world
    └── workshop       #Gazebo world containing simple house and robot
```

### Steps to launch the simulation

#### Step 1 Update and upgrade the Workspace image
```sh
$ sudo apt-get update
$ sudo apt-get upgrade -y
```

#### Step 2 Clone the lab folder in /home/workspace/
```sh
$ cd /home/workspace/
$ git clone https://github.com/mautonomous/gazebo_demo_workshop gazebo_demo_workshop
```

#### Step 3 Compile the code
```sh
$ cd /home/workspace/gazebo_demo_workshop
$ mkdir build
$ cd build/
$ cmake ../
$ make
```

#### Step 4 Add the library path to the Gazebo plugin path  
```sh
$ export GAZEBO_PLUGIN_PATH=${GAZEBO_PLUGIN_PATH}:/home/workspace/gazebo_demo_workshop/build
```


###Reference
https://github.com/udacity/RoboND-myrobot 
