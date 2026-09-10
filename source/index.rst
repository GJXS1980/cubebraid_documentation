CubeBraid SDK Documentation
===========================

.. toctree::
   :titlesonly:
   :maxdepth: 1
   :hidden:

   About-CubeBraid
   Get-Started
   Releases
   SDK-Architecture
   Submodules
   Developer-Tools
   API-Reference
   Migration-and-Upgrades
   The-CubeBraid-Project
   Contact
   Contributing

**CubeBraid SDK 是专为工业自动化与机器人协同开发打造的高性能综合软件开发包。**

从底层的机械臂控制、PLC 通信、工业相机图像采集，到传感器数据处理与通用日志/配置管理，CubeBraid SDK 为您的自动化与机器人应用提供了完整的模块化解决方案。

:ref:`了解更多关于 CubeBraid SDK <AboutCubeBraid>`

本文档适用于 **CubeBraid SDK v1.0 及以上版本**。如果您正在寻找特定子模块（如 `KawasakiSDK`、`CameraSDK` 或 `PLC_SDK`）的详细接口说明，请参阅 :doc:`API-Reference` 或查阅各子模块专项指南。

快速入门
--------

* :doc:`安装指南 <Get-Started/Installation>`
  - 环境依赖配置与 CubeBraid SDK 的安装/集成说明
* :doc:`快速上手 <Get-Started/Quickstart>`
  - 新手必看！通过简单的示例项目快速掌握 SDK 的基础调用流程
* :doc:`子模块指南 <Submodules>`
  - 详细了解 AGV、Camera、Json、Kawasaki、Logger、PLC、Robot 和 Sensor 8 大核心模块的使用方法
* :doc:`开发者工具 <Developer-Tools>`
  - 提供调试工具、日志分析器与常用配置模板的快速使用说明
* :doc:`API 参考手册 <API-Reference>`
  - 完整的 C++ 与 Python API 接口声明与参数手册

CubeBraid SDK 核心子模块
-------------------------

* **AGV_SDK**：移动机器人（AMR/AGV）导航、运动控制与状态监听
* **CameraSDK**：工业相机（梅卡曼德、海康、大华、Basler 等）图像采集与图像流管理
* **JsonSDK**：系统配置文件解析与数据序列化工具
* **KawasakiSDK**：川崎（Kawasaki）机械臂专用底层通信与 AS 指令控制
* **LoggerSDK**：全 SDK 统一的高性能日志记录与格式化输出
* **PLC_SDK**：工业 PLC（西门子 S7、欧姆龙 FINS、Modbus）寄存器读写通信
* **RobotSDK**：通用机械臂运动学与位姿控制抽象层
* **SensorSDK**：激光雷达、超声波及力控传感器数据采集与预处理

社区与开发者资源
----------------

如果您在开发过程中遇到问题，或希望参与 CubeBraid SDK 的建设：

* :doc:`贡献指南 <Contributing>`
  - 代码提交规范、文档编写标准以及 Pull Request 流程
* :doc:`版本发布日志 <Releases>`
  - 查看 SDK 的历史更新日志、最新特性与 Roadmap
* :doc:`联系与支持 <Contact>`
  - 提交 Bug 反馈、功能需求建议或获取技术支持响应

更多信息请访问 `CubeBraid 官方网站 <https://www.cubebraid.com/>`__。