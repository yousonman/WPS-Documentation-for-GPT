# Dialog 对象

## 简介

代表内置的 ET 对话框。

## 说明

Dialog 对象是 Dialogs 集合的成员。 Dialogs 集合包含 ET 中的所有内置对话框。不能在集合中新建或添加内置对话框。 Dialog 对象只能在 Show 方法中用来显示相应的对话框。

ET Visual Basic 对象库包含许多内置对话框的内置常量。每个常量的前缀均为“xlDialog”，随后即为对话框的名称。例如， “应用名称” 对话框常量为 xlDialogApplyNames ， “查找文件” 对话框常量为 xlDialogFindFile 。这些常量是 XlBuiltinDialog 枚举类型的成员。

使用 Di alogs ( *index* )（其中 *index* 是用于标识对话框的内置常量）可返回单个 Dialog 对象。下例运行 “文件” 菜单中的内置 “打开” 对话框。如果 ET 成功地打开了文件，则 Show 方法返回 True ；如果用户取消了对话框，则返回 False 。

``` JavaScript
let dlgAnswer = Application.Dialogs.Item(xlDialogOpen).Show()
```

## 方法

| 序号 | 名称                 | 说明                                                                                                                                              |
|:----:|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------|
|  1   | [Show](#Dialog.Show) | 显示内置的对话框，等待用户输入数据，然后返回一个代表用户响应的 Boolean 值 。如果用户单击“确定”，则返回 True ；如果用户单击“取消”，则返回 False 。 |

## 属性

| 序号 | 名称                               | 说明                                                                                                                                                                                                                            |
|:----:|:-----------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|  1   | [Application](#Dialog.Application) | 如果不使用对象识别符，则该属性返回一个 Application 对象，该对象表示 ET 应用程序。如果使用对象识别符，则该属性返回一个表示指定对象（可对一个 OLE 自动操作对象使用本属性来返回该对象的应用程序）创建者的 Application 对象。只读。 |
|  2   | [Creator](#Dialog.Creator)         | 返回一个 32 位整数，该整数指示在其中创建此对象的应用程序。只读 Long 类型。                                                                                                                                                      |
|  3   | [Parent](#Dialog.Parent)           | 返回指定对象的父对象。只读。                                                                                                                                                                                                    |

## 成员方法

### Dialog.Show

显示内置的对话框，等待用户输入数据，然后返回一个代表用户响应的 **Boolean** 值 。如果用户单击“确定”，则返回 **True** ；如果用户单击“取消”，则返回 **False** 。

**语法**

**express.Show ( *Arg1* , *...* , *Arg30* )**

\*express是一个代表 Dialog 对象的变量。

**参数**

| 名称    | 必选/可选 | 数据类型 | 说明                                                                   |
|---------|-----------|----------|------------------------------------------------------------------------|
| *Arg1*  | 可选      | Variant  | 仅应用于内置对话框，是命令的初始参数。有关详细信息，请参阅“注解”部分。 |
| *...*   | 可选      | Variant  | 仅应用于内置对话框，是命令的初始参数。有关详细信息，请参阅“注解”部分。 |
| *Arg30* | 可选      | Variant  | 仅应用于内置对话框，是命令的初始参数。有关详细信息，请参阅“注解”部分。 |

**说明**

对于内置对话框，如果用户单击 **“确定”** ，则本方法返回 **True** ；如果用户单击 **“取消”** ，则返回 **False** 。

可以使用单个对话框同时更改许多属性。例如，可以使用“设置单元格格式”对话框更改 Font 对象的所有属性。

对于一些内置对话框（如 **“打开”** 对话框），可以使用 *arg1* , *arg2* , ..., *arg30* 设置初始值。要查找想设置的参数，请在 **内置对话框参数列表** 中查找相应的对话框常量。例如，搜索 **xlDialogOpen** 常量以查找 **“打开”** 对话框的参数。有关内置对话框的详细信息，请参阅 Dialogs 集合。

**示例**

``` JavaScript
/* 本示例显示“打开”对话框*/
Application.Dialogs.Item(xlDialogOpen).Show()
```

## 成员属性

### Dialog.Application

如果不使用对象识别符，则该属性返回一个 **Application** 对象，该对象表示 ET 应用程序。如果使用对象识别符，则该属性返回一个表示指定对象（可对一个 OLE 自动操作对象使用本属性来返回该对象的应用程序）创建者的 **Application** 对象。只读。

**语法**

**express.Application**

\*express是一个代表 Dialog 对象的变量。

**示例**

``` JavaScript
/* 本示例显示一条有关创建 myObject 的应用程序的消息*/
function test() {
    let myObject = Application.ActiveWorkbook
    if(myObject.Application.Value == "ET") {
        alert("This is an ET Application object.")
    }
    else {
        alert("This is not an ET Application object.")
    }
}
```

### Dialog.Creator

返回一个 32 位整数，该整数指示在其中创建此对象的应用程序。只读 **Long** 类型。

**语法**

**express.Creator**

\*express是一个代表 Dialog 对象的变量。

**说明**

如果该对象是在 ET 中创建的，则此属性返回字符串 XCEL，它等同于十六进制的数字 5843454C。 **Creator** 属性是为 Macintosh 上的 ET 设计的，在 Macintosh 上，每个应用程序都具有一个四字符的创建者代码。例如，ET 的创建者代码为 XCEL。

### Dialog.Parent

返回指定对象的父对象。只读。

**语法**

**express.Parent**

\*express是一个代表 Dialog 对象的变量。

> WPS 开发文档： [WPS 基础接口/表格 API 参考/Dialog](https://qn.cache.wpscdn.cn/encs/doc/office_v19/index.htm)

------------------------------------------------------------------------
