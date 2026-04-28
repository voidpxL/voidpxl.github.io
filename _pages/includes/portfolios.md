
# 💻 项目经历

<div class='paper-box'>
    <div class='paper-box-image'>
        <div><img src='images/projects/RVF.png' alt="sym" width="100%">
        </div>
    </div>
    <div class='paper-box-text' markdown="1">

[车载雷视融合]()

搭载大角度的摄像头及和4D毫米波雷达，进行基于边缘计算（瑞芯微RV1126B）的目标检测、目标跟踪和雷视融合跟踪，输出稳定融合轨迹（40m，15Hz），融合探测得到准确的目标类型、实际距离和速度信息，并进行对应的可视化展示和报警策略设计。

技术栈：目标检测YOLO系列、RKNN、多模态跟踪、单目测距、雷视融合机制、行驶区域检测。

</div>
</div>

<div class='paper-box'>
<div class='paper-box-image'>
<div><img src='images/projects/TC_cls.png' alt="sym" width="100%">
</div>
</div>
<div class='paper-box-text' markdown="1">

[交通雷达数据处理]()

交通雷达数据处理，包括车辆轨迹跟踪、目标分类（非机动车、小车、大车）、实现视觉辅助标注，流量检测和车道检测，完成远近多波束融合，覆盖更大范围。

技术栈：**静平台多目标跟踪算法**、轻量化机器学习分类和基于热力图的车道检测，基于图网络的多目标轨迹预测。

</div>
</div>

<div class='paper-box'>
<div class='paper-box-image'>
<div><img src='images/projects/无人机避障雷达.png' alt="sym" width="100%">
</div>
</div>
<div class='paper-box-text' markdown="1">

[无人机避障雷达]()

无人机前向远距离避障和探测雷达数据处理算法设计，探索**远距离、高帧数（300m、40Hz）**的多目标跟踪及id保持、目标/航迹筛选逻辑，设计预警机制。

技术栈：**动平台多目标跟踪算法**、聚类和航迹处理策略、 针对无人机特性的机制和参数设计、 自我姿态较准/建模（IMU+自我运动估计）。

</div>
</div>


<div class='paper-box'>
<div class='paper-box-image'>
<div><img src='images/projects/电力防外破.png' alt="sym" width="100%">
</div>
</div>
<div class='paper-box-text' markdown="1">

[雷视融合电力防外破]()

完成视觉标定、电力线缆建模、视觉实例分割、雷视匹配和外破物入侵预警全流程，基于 YOLO11 实现工程车外破物的实例分割，设计逆高斯分布采样，结合视觉匹配点计算和回转数法实现精细的雷视匹配。参与雷视融合 SDK 设计和调试，设计并推动完整的数据采集、模型构建、数据标注、模型训练和模型部署全流程。

技术栈：外破物检测和分割，悬链线建模。

</div>
</div>

<div class='paper-box'>
<div class='paper-box-image'>
<div><img src= 'images/projects/旋转平台.png' alt="sym" width="100%">
</div>
</div>
<div class='paper-box-text' markdown="1">

[360旋转雷达（在研）]()

雷达搭载在旋转平台上，水平机械扫描，俯仰天线阵列测角，实现360°全向的环境感知和避障。对标大疆的

评估多雷达固定安装的360°覆盖方案，处理多雷达点云拼接和重叠区域融合，处理交叠区域冗余和冲突问题，处理外参标定。

技术栈：时空同步机制，点云一致性和拼接问题、工程落地约束。

</div>
</div>

<div class='paper-box'>
<div class='paper-box-image'>
<div><img src= 'images/projects/RETP.png' alt="sym" width="100%">
</div>
</div>
<div class='paper-box-text' markdown="1">

[自我运动估计-全局重建-多目标预测一体化框架 social-RETP（研究向）]()

完成自我运动估计-多目标跟踪-全局目标转换-多目标预测四个部分的算法级联框架，在radarscenes和大陆408雷达上完成验证。基于ransac算法实现自我运动估计（包括速度和横摆率），与九轴IMU进行对比，趋势和效果与IMU差距较小。基于IMU横摆率和雷达自测速重建历史轨迹，与GPS进行对比，然后将轨迹从自身坐标系映射到全局坐标系，并基于全局坐标进行多目标跟踪和多目标轨迹预测（STGNN-based）。

技术栈：毫米波雷达自我运动估计、坐标全局重建、多目标跟踪、多目标预测。

</div>
</div>
