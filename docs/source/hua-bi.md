# 画笔

本插件提供了3个画笔XSGridEditorBrush, XSUnitNodeBrush, XSPrefabNodeBrush, 用于简单编辑SRPG的网格地图. 画笔都是基于2D Tilemap Editor插件, 因此你需要先安装这个插件.

安装完毕后, 从菜单栏Window->2D->Tile Palette打开画笔界面, 如下图所示:

<img src="assets/image (3).png" alt="" data-size="original">

1. 提供的画笔只实现了红框内的3个按钮, 其他按钮是不实现的.
2. 这个我们用不到.
3. 画笔的主要功能区, 在这里可以切换画笔.

接下来介绍画笔的主要功能区

![](docs/assets/image8.png)

1. 画笔添加的对象都是prefab对象, 在这里指定好读取prefab的路径后, prefab的预览图会在4中显示. 使用XSGridEditorBrush和XSUnitNodeBrush时, 只有添加了脚本XSTileNode, XSunitNode的prefab才会在4中正常显示, XSPrefabNodeBrush则没有限制.
2. 显示画笔使用的prefab对象.
3. 设置添加对象的角度, 这样我们就不用为多个方向添加多个prefab了...
4. 选择画笔使用的prefab对象.

### XSGridEitorBrush

用于画tile的画笔, 表示unit可以移动的格子.

### XSUnitEditorBrush

用于画unit的画笔, unit必须在tile上才能添加.

### XSPrefabEditorBrush

用于画任何prefab的画笔, 同一格子上的prefab还会根据中心点叠加.
