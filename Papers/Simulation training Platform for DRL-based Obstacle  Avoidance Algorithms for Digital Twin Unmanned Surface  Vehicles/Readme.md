## 基于深度强化学习的数字孪生无人艇避障算法仿真训练平台

**作者:** 周治国、陈佳伟、祖博文、刘世棋、周学华

**发表时间:** xxxxxx

**期刊/会议:**xxxxxx

**链接:** [文章链接]()

**代码仓库:** [代码仓库链接]()

**相关资源:** [其他资源链接，如数据集、演示视频等]()

### 概要

- 深度强化学习训练平台中环境和智能体的构建对避障算法模型的应用性能有重要影响。目前的深度强化学习训练平台通常使用理想化的环境和粒子无人艇模型，未考虑无人艇和环境的动力学特性，降低了算法训练数据的维数，简化了智能体的奖励函数，导致避障算法模型难以在实际中应用。
- 本文提出了基于数字孪生概念的无人艇深度强化学习避障算法仿真与训练平台的设计。实现了避障算法的仿真、训练和性能评估，提供了从仿真训练到实际部署的框架。
- 为了验证环境仿真的真实感，进行了无人艇旋转和紧急制动实验。
- 通过调整海况高度和障碍物布局来评估无人船避障算法的有效性，并选择更有效的模型在真船上进行部署和测试。
- 实验表明，该仿真训练平台能够提供更接近实际环境的感知数据的深度强化学习算法。它可以有效地训练、测试和评估无人船深度强化学习避障算法。此外，所部署的算法对真船具有较好的泛化性。

### 背景

-  水面无人艇（USV）作为小型水上任务智能平台，具有灵活性高、智能化、隐蔽性好等特点。它们在水质评估、海岸线测绘、安全和救援行动等领域都有应用。
-  自主避障是USV智能的一个基本方面。由于无人潜航器的作业环境复杂，既受静态障碍物的影响，也受波浪、水流等移动障碍物等动态因素的影响，有效的自主避障对于成功完成任务至关重要。
-  深度强化学习（DRL）为无人艇导航和避障引入了一个新的维度，利用深度学习处理高维传感器数据，并利用强化学习进行决策和规划。DRL需要在USV代理及其环境之间进行大量的试错交互，以不断改进自我策略。由于在真实环境中使用物理设备进行训练时存在成本高、可控性低、可重复性有限、安全性不高等挑战，研究人员通常采用构建虚拟场景的方式在无人系统中进行DRL算法的训练和验证。
-  现有的培训平台在环境因素、agent模型、可视化等方面存在不同程度的不足。一些平台将航行场景理想化，忽略了风、波浪和水流等元素，而另一些平台则将USV过于简化为点模型，忽略了其运动特性。此外，现有平台通常依赖于损害可视化的基本模型。这些平台提供了与实际航行条件不同的数据，完成了算法训练和部分有效性论证。然而，在改进和训练算法时，调整仅限于这些环境和模型的范围，从而削弱了算法的实用性和泛化性。
-  数字孪生提供了一种连接物理和虚拟领域的方法，将现实世界的对象、过程或系统映射到它们的数字对应物上，从而实现无缝集成。虽然DRL为USV导航和避障铺平了新的道路，但Digital Twins可以在这个方向上提供重要的支持。


### 关键贡献

- 提出了一种基于深度强化学习的数字孪生无人艇避障算法仿真训练平台。通过将数字孪生概念引入平台设计，我们可以在虚拟环境中模拟各种复杂的任务场景，包括风、浪、流、动态障碍物等各种影响因素。它具有丰富的导航场景、逼真的运动仿真、良好的传感器仿真结果等特点，并为实船对接交互提供端到端的验证解决方案，使我们能够在更真实的环境中训练和验证深度强化学习算法。
- 该平台在导航场景构建中融入了数字孪生的思想，提供了高水平的精细化、高保真模型和良好的可视化结果。它可以提供复杂的天气环境，并可以为传感器提供与实际情况相似的数据。
- 该平台可以模拟风浪环境，计算作用在船舶上的力，提供船舶姿态变化信息，更好地模拟船舶在真实水域条件下的运动。
- 该平台提供各种模拟传感器，包括GPS、激光雷达、IMU和摄像头。每个传感器提供多个配置参数选项，可根据实际传感器进行配置。它还提供噪声模拟，以更好地模拟现实世界的数据条件。
- 该平台提供了一个从模拟训练到实际部署的框架，使基于ROS的算法能够快速部署。

### 实验结果

- 本文提出了一个用于数字孪生无人船深度强化学习算法的模拟训练平台。该平台解决了USV的理想化环境和简化的点质量模型导致的算法模型的性能较差和泛化能力有限的问题。模拟训练平台采用模块化设计理念，每个模块都表现出低耦合性，以便于未来的维护和升级。

- 在运动模拟实验中，USV在该平台上的运动数据与真实世界导航的偏差小于10%。这展示了反映客观运动模式的高度运动模拟精度。构建的虚拟环境和模拟传感器提供了与真实世界场景非常相似的数据，支持了模拟的准确性。在真实世界的部署过程中，各种算法的成功率与在虚拟仿真环境中获得的结果有很强的相关性。这表明，使用该平台在非理想条件下训练的算法可以在真实世界的场景中提供可比较的结果，从而展示出强大的泛化能力。

- 除了模拟USV运动，该平台还便于算法训练和验证。因此，为智能USV算法的研究和泛化性能的测试提供了一个稳健的基准。该平台的预期用户群包括无人水面舰艇领域的广泛开发人员。此外，它在最大限度地减少海上调试工作量、增强算法适应性和加快算法开发周期方面发挥着至关重要的作用。

- ![image-20231023150021764](Readme.assets/image-20231023150021764.png)

  ![image-20231023150050802](Readme.assets/image-20231023150050802.png)

  ![image-20231023150113554](Readme.assets/image-20231023150113554.png)

  ![image-20231023150126264](Readme.assets/image-20231023150126264.png)

  ![image-20231023150135688](Readme.assets/image-20231023150135688.png)

![image-20231023150158490](Readme.assets/image-20231023150158490.png)

![image-20231023150213856](Readme.assets/image-20231023150213856.png)

![image-20231023150235649](Readme.assets/image-20231023150235649.png)

![image-20231023150252147](Readme.assets/image-20231023150252147.png)

### 引用

[1] Z. Liu, Y.Zhang, X.Yu and Y.chi, “Unmanned surface vehicles: An overview of developments and challenges,” *Annu.* *Rev.* *Control*, vol.41, pp. 71-93, 2016.

[2] J. Tang, S. Lao, and Y. Wan, “Systematic review of collision-avoidanceapproaches for unmanned aerial vehicles,” *IEEE Syst. J.*,vol. 16, no. 3, pp. 4356–4367, 2021.

[3] X. Zhao and S. Ding, “A review of deep reinforcement learning,”*Computer science*, vol. 45, no. 7, pp. 1–6, 2018.

[4] J. Yan, Q. Zhang, and X. Hu, “Review of path planning techniques based on reinforcement learning,” *Computer Engineering*, vol. 47, no. 10, pp. 16–25, 2021.

[5] S. Chen, Y. Chen, S. Zhang, and N. Zheng, “A novel integrated simulation and testing platform for self-driving cars with hardware in the loop,” *IEEE Transactions on Intelligent Vehicles*, vol. 4, no. 3, pp. 425– 436, 2019.

[6] L. Zheng, J. Yang, H. Cai, M. Zhou, W. Zhang, J. Wang, and Y. Yu, “Magent: A many-agent reinforcement learning platform for artificial collective intelligence,” in *Proceedings of the AAAI conference on artificial intelligence*, vol. 32, 2018.

[7] K. Cobbe, O. Klimov, C. Hesse, T. Kim, and J. Schulman, “Quantifying generalization in reinforcement learning,” in *International Conference on Machine Learning*, pp. 1282–1289, PMLR, 2019.

[8] X. Xiao, Z. Xu, Z. Wang, Y. Song, G. Warnell, P. Stone, T. Zhang, S. Ravi, G. Wang, H. Karnan, *et al*, “Autonomous ground navigation in highly constrained spaces: Lessons learned from the benchmark autonomous robot navigation challenge at icra 2022 [competitions],” *IEEE Robotics & Automation Magazine*, vol. 29, no. 4, pp. 148–156, 2022.

[9] Z. Xu, B. Liu, X. Xiao, A. Nair, and P. Stone, “Benchmarking reinforcement learning techniques for autonomous navigation,” in *2023 IEEE International Conference on Robotics and Automation (ICRA)*, pp. 9224–9230, IEEE, 2023.

[10] T. H.-J. Uhlemann, C. Lehmann, and R. Steinhilper, “The digital twin: Realizing the cyber-physical production system for industry 4.0,” *Procedia Cirp*, vol. 61, pp. 335–340, 2017.

[11] L. Fan, Y. Zhu, J. Zhu, Z. Liu, O. Zeng, A. Gupta, J. Creus-Costa, S. Savarese, and L. Fei-Fei, “Surreal: Open-source reinforcement learning framework and robot manipulation benchmark,” in *Conference on Robot Learning*, pp. 767–782, PMLR, 2018.

[12] S.-Y. Shin, Y.-W. Kang, and Y.-G. Kim, “Obstacle avoidance drone by deep reinforcement learning and its racing with human pilot,” *Applied sciences*, vol. 9, no. 24, p. 5571, 2019.

[13] A. Rafiei, A. O. Fasakhodi, and F. Hajati, “Pedestrian collision avoidance using deep reinforcement learning,” *International journal of automotive technology*, vol. 23, no. 3, pp. 613–622, 2022.

[14] R. Cimurs, I. H. Suh, and J. H. Lee, “Goal-driven autonomous exploration through deep reinforcement learning,” *IEEE Robotics and Automation Letters*, vol. 7, no. 2, pp. 730–737, 2021.

[15] M. Kirtas, K. Tsampazis, N. Passalis, and A. Tefas, “Deepbots: A webots-based deep reinforcement learning framework for robotics,” in *Artificial Intelligence Applications and Innovations: 16th IFIP WG 12.5 International Conference*, AIAI 2020, Neos Marmaras, Greece, June 5– 7, 2020, Proceedings, Part II 16, pp. 64–75, Springer, 2020.

[16] H. Yuan, J. Ni, and J. Hu, “A centralised training algorithm with d3qn for scalable regular unmanned ground vehicle formation maintenance,” *Iet.* *Intell.* *Transp.* *Sy**.*, vol. 15, no. 4, pp. 562–572, 2021.

[17] Y. Yang, Z. Hou, H. Chen, and P. Lu, “Drl-based path planner and its application in real quadrotor with lidar,” *J.* *Intell.* *Robot.* *Syst**.*, vol. 107, no. 3, p. 38, 2023.

[18] C. Fu, X. Xu, Y. Zhang, Y. Lyu, Y. Xia, Z. Zhou, and W. Wu, “Memory-enhanced deep reinforcement learning for uav navigation in 3d environment,” *Neural.* *Comput.* *Appl**.*, vol. 34, no. 17, pp. 14599–14607, 2022.

[19] X. Xu, Y. Lu, X. Liu, and W. Zhang, “Intelligent collision avoidance algorithms for usvs via deep reinforcement learning under colregs,” *Ocean.* *Eng**.*, vol. 217, p. 107704, 2020.

[20] X. Wu, H. Chen, C. Chen, M. Zhong, S. Xie, Y. Guo, and H. Fujita, “The autonomous navigation and obstacle avoidance for usvs with anoa deep reinforcement learning method,” *Knowl-based.* *Syst**.*, vol. 196, p. 105201, 2020.

[21] B. Sangiovanni, G. P. Incremona, M. Piastra, and A. Ferrara, “Selfconfiguring robot path planning with obstacle avoidance via deep reinforcement learning,” *IEEE Contr. Syst. Lett.*, vol. 5, no. 2, pp. 397–402, 2020.

[22] P. Wang, R. Liu, X. Tian, X. Zhang, L. Qiao, and Y. Wang, “Obstacle avoidance for environmentally-driven usvs based on deep reinforcement learning in large-scale uncertain environments,” *Ocean.* *Eng**.*, vol. 270, p. 113670, 2023.

[23] R. Song, Y. Liu, and R. Bucknall, “Smoothed a* algorithm for practicalunmanned surface vehicle path planning,” *Appl.* *Ocean.* *Res**.*, vol. 83, pp. 9–20, 2019.

[24] R. Sawada, K. Sato, and T. Majima, “Automatic ship collision avoidance using deep reinforcement learning with lstm in continuous action spaces,” *J.Mar.Sci.Tech-japan**.*, vol. 26, pp. 509– 524, 2021.

[25] M. Paravisi, D. H. Santos, V. Jorge, G. Heck, L. M. Gonc¸alves, and A. Amory, “Unmanned surface vehicle simulator with realistic environmental disturbances,” *Sensors-basel**.*, vol. 19, no. 5, p. 1068, 2019.

[26] A. Dosovitskiy, G. Ros, F. Codevilla, A. Lopez, and V. Koltun, “Carla: An open urban driving simulator,” in *Conference on robot learning* , pp. 1–16, PMLR, 2017.

[27] S. Shah, D. Dey, C. Lovett, and A. Kapoor, “Airsim: High-fidelity visual and physical simulation for autonomous vehicles,” in *Field and Service Robotics: Results of the 11th International Conference*, pp. 621–635, Springer, 2018.

[28] S.-K. Ueng, D. Lin, and C.-H. Liu, “A ship motion simulation system,” *Virtual**.**Real-london**.*, vol. 12, pp. 65–76, 2008.

[29] K. Benedict, M. Kirchhoff, M. Gluch, S. Fischer, and M. Schaub, “Simulation augmented manoeuvring design and monitoring–a new method for advanced ship handling,” *TransNav**.*, vol. 8, no. 1, pp. 131–141, 2014
