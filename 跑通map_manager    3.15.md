## 基于RGB-D相机的无人机导航避碰实时动态障碍物跟踪映射系统

### 摘要

#### 该系统首先利用具有占有率体素图的深度图像生成潜在的动态障碍物区域作为建议。根据障碍物区域建议，应用卡尔曼滤波器和我们的连续性滤波器跟踪每个动态障碍物。最后，利用跟踪的动态障碍物的状态，提出了基于马尔可夫链的环境感知轨迹预测方法。





# 编译octomap的包报错：Could not find the required component ‘octomap_ros‘.

#### 

### 报错

Could not find a package configuration file provided by "octomap_ros" with
any of the following names:

octomap_rosConfig.cmake
octomap_ros-config.cmake

### 解决方法

#### 补齐缺失的包

sudo apt-get install ros-melodic-octomap ros-melodic-octomap-mapping ros-melodic-octomap-msgs ros-melodic-octomap-ros ros-melodic-octomap-rviz-plugins ros-melodic-octomap-server

#### 无法定位软件包

#### 这种情况得确定ubantu版本

sudo apt-get install ros-noetic-octomaps



# fast_gicp下载编译失败解决办法

#### 问题：无法从github下载

#### 解决：码云下载源码

git clone https://gitee.com/qianlihaoyue/fast_gicp.git --recursive

放在工作目录下

#### 问题：编译失败不通过

[关于fast_gicp下载编译失败解决办法_fastgicp-CSDN博客](https://blog.csdn.net/dss0606/article/details/132963284)

将网页cmakelist文件替换fast-gicp的cmakelist文件



# hdl_graph_slam 调试遇到的问题解决

#### 安装依赖项

sudo apt install libomp-dev

sudo apt-get install ros-noetic-geodesy ros-noetic-pcl-ros ros-noetic-nmea-msgs ros-noetic-libg2o

#### 问题：“ ”is not a member of “ ”

#### 解决：

在hdl_global_localization的cmakelist文件添加

add_compile_options(-std=c++14)  add_compile_options(-std=gnu++14)



# Ubuntu编译报错 error: #error PCL requires C++14 or above

#### 问题：编译ndt_omp功能包的时候,出现报错 `error: #error PCL requires C++14 or above` ,并且后面一堆报错乱码

#### 解决方法：

#### 1.注释c++11的特性数值

#### 2.不能解决，找到工程中所有依赖pcl的功能包，修改对应的cmakelist文件。

#### 在add_compile_options(-std=c++11)下一行加入

#### set(CMAKE_CXX_STANDARD 14)

#### 指定c++版本



# ROS：Could NOT find move_base_msgs

### 解决方法：

#### 安装move_base_msgs,注意安装对应ros版本

sudo apt-get install ros-noetic-move-base-msgs



# 乐视RGB-D深度相机/Orbbec Astra Pro显示图像和点云

#### 安装依赖项后：E:无法定位软件包：ros-noetic-libuvc

#### 无法sudo 安装，指定版本后也无效

#### 解决方法：libuvc下有三个包，ros-noetic-libuvc-camera

#### ros-noetic-libuvc-camera-dbgsym   ros-noetic-libuvc-ros

#### 分别sudo apt-get install



####  

#### 创建 astra udev 环境

roscd astra_camera
sudo sh ./scripts/create_udev_rules



#### 使用lsusb查看相机接口！（未找到rgb模块）

启动roslaunchastra-camera  astrapro.launch

rviz

#### add-by topic添加image

![微信图片_20250316212802](C:\Users\arche\Desktop\微信图片_20250316212802.png)
