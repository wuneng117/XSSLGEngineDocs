# 范例场景

作为演示的范例场景是Scenes/Demo\_1.unity. 接下来对场景中的所有节点(图1)一一做介绍.

<figure><img src="assets/image (7).png" alt=""><figcaption><p> 图1</p></figcaption></figure>



### Camera

如图2所示, Camera主要有3个节点组成. 因为我们用到了Cinemachine插件. 如果不知道Cinemachine是什么,可以先看看官方的介绍, 真的是一个很棒的插件!

<figure><img src="assets/image (1).png" alt=""><figcaption><p>图2</p></figcaption></figure>

#### Main Camera

场景中的主相机.

#### CM\_vcam

Cinemachine的虚拟相机, 为了实现SRPG相机, 主要使用了以下脚本:

* Cinemachine Input Provider: Cinemachine提供的输入控制相机脚本, 控制是基于Input System插件实现的.
* Cinemachine Confiner: Cinemachine提供的脚本,用于控制摄像机的移动范围.
* XSCamera: 本插件实现的SPRG相机,通过使用上面两个脚本, 实现鼠标在屏幕边缘时移动视野范围, 方向键控制相机角度.

#### CM\_confine

节点上的Box Collider控制相机移动范围, 不需要自己设置, 在初始化游戏时会根据地图tile的范围自动生成.



### XSGridEditor

XSGridEditor是插件的重要组成部分, 如图3所示, 主要有3个节点.

<figure><img src="assets/image (9).png" alt=""><figcaption><p>图3</p></figcaption></figure>

#### XSGridEditor

提供了一些编辑tile时的常用功能.

#### TileRoot

用XSGridEditorBrush添加的tile都放在这个节点下. 你可以通过调整节点上脚本Grid的CellSize改变tile的大小.

#### UnitRoot

用XSUnitNodeBrush添加的Unit都放在这个节点下.

#### PrefabRoot

用XSPrefabNodeBrush添加的对象默认放在这个节点下, 你也可以通过XSPrefabNodeBrush的配置改成其他节点, 并没有限制.

### main

挂载了测试场景用的脚本XSBattleMgr, 用于演示如何显示移动范围, unit移动.
