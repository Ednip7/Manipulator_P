## Manipulator P running in docker.
This projects use code provided by Robotis to control and simulate Open Manipulator P.

# Usage

The recommended reference development environment is provided as a docker container. To create the container, go to the `docker/` folder and run `build.bash`.

> cd docker/
> ./build.bash

The container creates a ROS Melodic + Gazebo 9 environment that can be used to launch the simulation and build the software.

To launch the container use the `run.bash` script in the `docker/` folder.

> ./run.bash

After that, to open a second, third, etc. terminals, use the `join.bash` script instead.

> ./join.bash

This will set you up to work, with a starting working directory set in the root fo the ROS workspace.

To build the repository you only need to do:

> catkin_make
> source devel/setup.bash

And to launch simulations:

Load OpenManipulator-PRO on Gazebo simulator and click on Play ▶ button.
> roslaunch open_manipulator_p_gazebo open_manipulator_p_gazebo.launch

Controller for Gazebo:

Launch the open_manipulator_p_controller for gazebo simulation.

>roslaunch open_manipulator_p_controller open_manipulator_p_controller.launch use_platform:=false