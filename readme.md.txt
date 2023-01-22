1. Copy the entire 'botcar2' folder to the catkin_ws/src location and run caktin_make

2. Before running, the controllers need to be installed else you will get 'controllers not found' error. Please use the following command:

	sudo  apt-get  install  ros-noetic*control*

3. Run the following for Gazebo Environment and simulation:

	roslaunch botcar2 newlaunch.launch

4. Then for using the Teleop, run in a separate terminal in the /scripts location:

	chmod +x teleop_template.py
	rosrun botcar2 teleop_template.py

5. Then for LaserScan vizualization, follow these steps:

	(a) Run 'rviz' command in a new terminal and select the Fixed Frame

	(b) Add a new 'RobotModel' vizualization, this will make the robot spawn

	(c) Add 'LaserScan' vizualization and choose the topic as 'my_robot/scan/' with the size set as 0.1 

6. Then for using the publisher and subscriber, run in separate terminals in /scripts location:
	
	chmod +x subscriber.py
	chmod +x publisher.py
	rosrun botcar2 subscriber.py
	rosrun botcar2 publisher.py