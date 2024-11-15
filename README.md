Before start it, please check the file path in all the files, particularly in .world file.

To start the program please follow this steps:

1. Open a terminal in the "robot"

```
cd robot
catkin_make
source devel/setup.bash
```

if there are any erros, that's must because of dependencies.

You have to download many packages about gazebo and there are some other imformation in the pdf (which is made by a youtuber).

The pdf is about how to use rviz to control arm(pusher). 

2. Start the roslaunch

```
roslaunch moveit_sim full_robot_arm_sim.launch 
```

Then you can change the state of arm by choosing "pusher up" as the end state and clicking "plan and execute".

if you only want to drive the car you can use the command below instead.Because it has a pusher ahead, so the car can't drive up to the platform.

```
roslaunch robot_model_pkg robot_xacro.launch
```

3. Drive the car

```
rosrun teleop_twist_keyboard teleop_twist_keyboard.py
```

You have to download the revelent package before using the command above.

You can follow the imformation given by this command.

i: forward; k: stop; ……

4. At last you can maneuver the car to do the tasks.

I'm sure that the car can drive up the ramps and push the balls into the basket.A photo is given.
