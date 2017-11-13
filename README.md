# Extended-Kalman-Filter
In this project, I used C++ to write a program that processes Lidar and Radar data to track / predict object positioning via an Extended Kalman Filter. 

## Project Info
For a quick tutorial on Kalman Filters, I recommend the following [here](http://www.ilectureonline.com/lectures/subject/SPECIAL%20TOPICS/26/190).

Kalman filters offer a great way to make a prediction about the position and speed of an object based on historic data (one time step backwards). To see the implementation please visit the following three files in the 'src' folder:

1. FusionEFK.cpp
2. kalman_filter.cpp
3. tools.cpp

## Setup instructions
FYI, I ran my code on a Macbook Pro. Please ensure you have downloaded the Udacity SDCND Simulator [here](https://github.com/udacity/self-driving-car-sim/releases/) and have installed cmake (3.5), make (4.1), and gcc/gcc+ (5.4).

1. Open Terminal
2. `git clone https://github.com/tlapinsk/CarND-Extended-Kalman-Filter-Project.git`
3. `cd CarND-Extended-Kalman-Filter-Project`
4. `sh install-mac.sh`
5. `mkdir build && cd build`
6. `cmake`
7. `make`
8. `./ExtendedKF`

## Results
My Extended Kalman Filter produced the below results. 'px' is the x-position, 'py' is the y-position, 'vx' is velocity in the x-direction, and 'vy' is velocity in the y-direction.

| Input |   MSE   |
| ----- | ------- |
|  px   | 0.0973  |
|  py   | 0.0855  |
|  vx   | 0.4513  |
|  vy   | 0.4399  |


![Visualization](https://github.com/tlapinsk/CarND-Extended-Kalman-Filter-Project/blob/master/output/results.png?raw=true "Visualization")

## Resources
Most of my code is pulled from the Udacity introduction to Extended Kalman Filters within the SDCND. Below are further resources and helpful links that I used to complete this project:

- [Normalization in Kalman.cpp](https://discussions.udacity.com/t/ekf-radar-causes-rmse-to-go-through-the-roof/243944/5?u=tim.lapinskas)
- [Radar updates](https://discussions.udacity.com/t/radar-updates-are-messing-up/281342/3)
- [Initialization graphic](https://discussions.udacity.com/t/initializing-the-radar-state-for-ekf/236396/10?u=tim.lapinskas)
- [RMSE values](https://discussions.udacity.com/t/rmse-values-of-ekf-project/243997)