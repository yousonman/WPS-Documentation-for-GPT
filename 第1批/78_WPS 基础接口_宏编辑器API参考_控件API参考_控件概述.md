# 控件概述

WPS宏编辑器提供了命令按钮、 标签、文本框、复合框、列表框、复选框等控件，其跟api对象对应关系如下。

| 控件类型       | API对象       | 功能         |
|----------------|---------------|--------------------------------------------------------|
| 窗体       | UserForm      | 用于选中或是移动控件对象。              |
| 命令按钮   | CommandButton | 创建一个可以让用户选择，以完成一个命令的按钮                      |
| 标签       | Label         | 用于显示用户不能编辑的文本或图像，例如图形下的标题文本。          |
| 文本框     | TextEdit      | 用于输入或改变文本内容。                |
| 复合框     | ComboBox      | 复合框由一个文本输入控件和一个下拉菜单组成，用户可以从预先定义的列表中的选择一个选项，同时也可以直接通过文本框输入 |
| 列表框     | ListBox       | 用来显示用户可以选择的项目列表。如果不能一次显示全部项目的话，列表可以滚动。                 |
| 复选框     | CheckBox      | 可以显示出多重选择，用户可以选择一个或者多个选项，如果选中多个选项则显示出多重选择。         |
| 选项按钮   | OptionButton  | 可以显示出多重选择，用户只能选择一个。  |
| 滚动条     | ScrollBar   |提供在长列表工程或大量信息中快速浏览的图形工具，以比例方式指示出当前位置，或是做为一个输入设备，或速度及数量的指示器。 |
| 水平布局器 | HLayout       | 将内部的控件按照水平方向排布，一列一个。|
| 垂直布局器 | VLayout       | 将内部的控件按照垂直方向排布，一行一个。|
| 水平间隔   | HSpacer       | 填充水平方向上无用的空隙。              |
| 垂直间隔   | VSpacer       | 填充垂直方向上无用的空隙。              |
| 旋转按钮   | SpinButton    | 一种与其它控件并用微调控制的控件，也可以用来对一个范围的值或工程列表做向前或向后的遍历。     |
| 切换按钮   | ToggleButton  | 创建一个切换开关的按钮。                |
| 框架       | Frame         | 可以创建一个图形或控件的功能组。要为多个控件创建组，可先画框架，接着在框架中添加控件。       |
| 多页       | MultiPage   | 包含一个选项卡栏和一个页面区的容器类组件，通过切换选项卡来切换不同页面，从而达到在同一个窗口中自由切换不同的内容。  |

> WPS 开发文档： [WPS 基础接口/宏编辑器API参考/控件API参考/控件概述](https://qn.cache.wpscdn.cn/encs/doc/office_v19/topics/WPS%20%E5%9F%BA%E7%A1%80%E6%8E%A5%E5%8F%A3/%E5%AE%8F%E7%BC%96%E8%BE%91%E5%99%A8API%E5%8F%82%E8%80%83/%E6%8E%A7%E4%BB%B6API%E5%8F%82%E8%80%83/%E6%8E%A7%E4%BB%B6%E6%A6%82%E8%BF%B0.html)

------------------------------------------------------------------------
