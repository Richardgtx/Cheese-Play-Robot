###  三子棋机器人
这是一个会下三子棋的机器人。可以实现人机对弈。该项目荣获全国大学生电子设计大赛三等奖（2024E题），由张承璧、潘玮同学与我共同完成，我担任团队队长。

![Representation](https://github.com/user-attachments/assets/272f9cb6-7245-4d2f-9c10-fa8edddd0abf)

#### 功能实现
- 棋子位置识别：棋格&棋子在空间中的位置已预先标定，其坐标信息作为一组数据预先存储于系统中。系统通过识别棋格&棋子在图像中的位置与其预先标定的坐标进行匹配，从而确定棋子的精确位置。
- 决策：使用  $\alpha-\beta$  剪枝算法实现对弈。
- 移动棋子：该机器人采用了步进电机驱动的丝杠机构，丝杠末端连接舵机带动的电磁铁（吸取棋子）。两套丝杠分别沿x轴和y轴方向布置，通过丝杠的伸缩运动，带动末端执行器（携带棋子）在平面内实现精确移动。
  

https://github.com/user-attachments/assets/d90897b4-2650-4570-8088-a61d5d9886fb

#### 硬件构成
总体的的结构连接件使用3D打印。
![结构设计图带棋盘](https://github.com/user-attachments/assets/fa3b1786-76ad-4c73-81ff-9d37f5715e40)
![三字棋装置 drawio](https://github.com/user-attachments/assets/26191e89-1e4f-4bbc-9fc7-8ab842aa82b0)
#### 技术难点
1. 步进电机的控制：采用freertos的多任务并行，给x,y轴电机同时输出pwm控制信号。使得棋子可以沿着任意轨迹运动。
2.  Nac小电脑和stm32之间的I2C通信
3.  $alpha-beta$剪枝算法
4.  3D打印结构件
5.  添加了串口屏（触控）的交互方向。可以用它控制机器人拾取棋子。
![触控屏交互界面](https://github.com/user-attachments/assets/7eba8e55-7e4d-4a54-b2a8-52e1091f8c61)
#### 花絮
![Representation2](https://github.com/user-attachments/assets/e94ee9f2-8c7b-47e9-b2dc-87bf852d2fff)
![Representation3](https://github.com/user-attachments/assets/e2f75a30-a106-4cf6-af93-3e6bd7c6fd06)
![结构设计图](https://github.com/user-attachments/assets/ff36c5c6-8748-4ef2-919d-13b19937b509)


https://github.com/user-attachments/assets/03ddc080-e471-4e68-9968-d545d53ab935


