### 启动 ROS

roscore

### 创建工作环境

mkdir -p ~/catkin_ws/src

 cd ~/catkin_ws/src

 catkin_init_workspace

catkin_create_pkg test std_msgs rospy roscpp

(创建包text，包名+消息类型 python依赖项，c++依赖项)

### 编译

cd ~/catkin_ws

catkin_make

### 添加全局路径

echo "source catkin_ws/devel/setup.bash" >> ~/.bashrc

source ~/.bashrc

### ros命令

rosrun 包名 节点名

roslaunch 包名+，launch文件

rosrun rqt_graph rqt_graph（节点关系图）

### ros信息命令

 rostopic  ros+topic 确认ROS话题信息

 rosservice ros+service 确认ROS服务信息

 rosnode ros+node 确认ROS节点信息 

rosparam  ros+param(parameter) 确认和修改ROS参数信息 

rosbag  ros+bag 记录和回放ROS消息 

rosmsg  ros+msg 显示ROS消息类型

rossrv ros+srv 显示ROS服务类型 

rosversion  ros+version 显示ROS功能包的版本信息 

roswtf  ros+wtf 检查ROS系统

### ros catkin 命令

catkin_create_pkg  自动生成功能包 

catkin_make  基于catkin构建系统的构建

catkin_eclipse 对于用catkin构建系统生成的功能包进行修改，使其能在 Eclipse环境中使用 catkin_prepare_release  发布时用到的日志整理和版本标记 

catkin_generate_changelog  在发布时生成或更新CHANGELOG.rst文件 

catkin_init_workspace  初始化catkin构建系统的工作目录 

catkin_find  搜索catkin

### ros功能包

rospack ros+pack查看ros功能包信息

rosinstall 安装附加功能包

rosdep 安装该功能包的依赖性文件

roslocate ros功能包相关命令

### ros节点操作命令

rosnode list 查询活动节点

rosnode ping +节点名 与指定的节点进行连接测试

rosnode info+节点名 查看指定节点信息

rosnode kill+节点名 停止节点运行

### rostopic话题

rostopic list 显示话题目录

rostopic echo +话题名称  实时显示话题消息内容

rostopic find +消息类型   小时使用指定类型消息的话题

rostopic info+话题名称 显示话题信息

### ros消息信息

rosmsg list  显示所有消息

rosmsg show +消息名称 显式指定消息

rosmsg package+功能包名  显示功能包的消息

rosmsg packages  显示所有消息包类型

