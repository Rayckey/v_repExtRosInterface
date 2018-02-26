# ROS Interface plugin for V-REP

### Compiling

1. Download
```
$ git clone --recursive https://github.com/Rayckey/v_repExtRosInterface.git
```
2. Edit `meta/messages.txt` and `meta/services.txt` if you need to include more ROS messages/services. You need to specify the full message/service type, i.e. geometry_msgs/Twist rather than Twist.
3. Edit `set(ENV{VREP_ROOT} ~/V-REP_PRO_EDU_V3_5_0_Linux)` in `CMakeLists.txt` to the path of V-REP installation, and comment `link_directories("/opt/ros/lunar/lib")` if using older versions 
4. Return to work space and build using catkin build (catkin make may cause issues)
```
$ catkin build
```
5. IMPORTANT! After compiling, copy `libv_repExtRosInterface.so` from `WORKSPACE/devel/lib/` to V-REP root folder, do so whenever the `meta/messages.txt` or `meta/services.txt` files have changed
# v_repExtRosInterface
