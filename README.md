# Autonomous Race Car

The platform is based on 1/10th sized rally cars and the Nvidia Jetson TX 2 embedded super-computer. The platform houses the following major components, 1. RealSense ZR-300 RGB-D Camera which could get images up to 1080p @ 30Hz and get depth upto 628 × 628 @ 60fps 2. Hokuyo URG- 04LX-UG01 Laser having a scanning angle of 30◦ and a sampling rate of 10Hz and 3. Razor IMU containing the accelerometer, gyroscope and magnetometer programmed for sample rate of 50Hz and 4. Fully programmable VESC (Vedder Electronic Speed Controller) which controls both the brushless motor (forward/backward) and servo motor (steering).

Over the course of Winter 2018 quarter this remote controlled car was programmed using ROS, Python, PyTorch and OpenCV to handle autonmous driving one step at a time. First, particle filter was implemented to allow the car to localize itself. Second, local control algorithms were implemented using incoming visual data from the car’s RGBD camera. Third Model Predictive path control (MPPI) algorithm was implemented to integrate local control with a global plan. Finally a global planning module is implemented that integrates all the above components with an efficient gloabl search over the map to compute a trajectory (plan) that the car would follow.
