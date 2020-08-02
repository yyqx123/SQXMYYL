# 摇摇乐
2020年新工科联盟-Xilinx暑期学校（Summer School）项目

# 项目介绍

本项目是基于FPGA搭建具有实时性的云端传感器数据检测系统的摇摇乐项目，通过板载陀螺仪上IMU采集其转动的数据，通过I2C接口发送给FPGA中收到数据后由QSPI	接口发送至ESP32中，再由ESP32发送数据上传给AWS IOT控制台，进行数据的实时监测。本项目的核心目的是通过板载FPGA+ESP32的设计搭建与AWS IOT的数据处理及数据通信的平台，实现将传感器的数据接入到AWS IOT 云端的功能

# 实现功能

能够正确采集板载陀螺仪上IMU收集的数据，记录摇摇乐转动的次数，并且通过ESP32发送给AWS云服务器节点，进行传感器数据云端显示。

# 软件清单

Vivado2018.03（用于FPGA开发）  Arduino-IDE（用于ESP32开发及案例调试和连接AWS）

# 硬件清单

SEA-Board开发板，板载FPGA型号为XC7S15FTGB196-1  TF卡 读卡器

# 项目开发步骤
解压DEMO文件夹；
在VIVADO上对工程文件综合，生成BIT文件，利用TF烧录到FPGA;
通过QSPI接口将数据传输给ESP32;
ESP32连接AWS IOT ,发送数据，进行监测。




