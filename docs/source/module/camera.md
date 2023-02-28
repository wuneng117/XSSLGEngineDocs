### Camera
Camera是处理游戏中相机的移动,旋转的相关逻辑. 在这里作为演示的范例场景是Scenes/Demo_1.unity. 如图所示, 我们可以在范例场景中找到这3个组成Camera的节点. 其中我们用到了Cinemachine插件. 如果不知道Cinemachine是什么,可以先看看官方的介绍, 真的是一个很棒的插件!

![](assets/image1.png)

#### Main Camera

Unity场景默认自带的主相机.

#### CM_vcam

Cinemachine的虚拟相机, 为了实现SRPG相机, 主要使用了以下脚本:

* Cinemachine Input Provider: Cinemachine提供的输入控制相机脚本, 控制是基于Input System插件实现的.
* Cinemachine Confiner: Cinemachine提供的脚本,用于控制摄像机的移动范围.
* XSCamera: 本插件实现的SPRG相机,通过使用上面两个脚本, 实现鼠标在屏幕边缘时移动视野范围, 方向键控制相机角度.

#### CM\_confine

节点上的Box Collider控制相机移动范围, 不需要自己设置, 在初始化游戏时会根据地图tile的范围自动生成.
