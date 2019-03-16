#BLAM With Grid Map

***BLAM!*** is an open-source software package for LiDAR-based real-time 3D localization and mapping. ***BLAM!*** is developed by Erik Nelson from the Berkeley AI Research Laboratory ([BAIR](http://bair.berkeley.edu)). See https://youtu.be/08GTGfNneCI for a video example.


##介绍
这是由BLAM修改而成的可以试试转点云为栅格地图的BLAM PRO。便于路径规划和导航

##编译
使用下面的命令编译安装
```bash
catkin_make -DCMAKE_BUILD_TYPE=Release
```

##运行
##正常的BLAM

在线模式，使用另一个终端播放bag或者链接激光雷达
```bash
roslaunch blam_example test_online.launch
```

离线模式
```bash
roslaunch blam_example test_offline.launch
```


##转栅格地图
使用滤波器滤除地面后在建立点云地图在转栅格地图
```bash
roslaunch blam_example cloud2map_filter_octomap.launch
```

使用直通滤波器去除点云后在转栅格地图
```bash
roslaunch blam_example cloud2map_passthrough_octomap.launch
```



