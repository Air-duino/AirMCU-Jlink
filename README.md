# AirMCU-Jlink

AirMCU 系列的 Jlink 支持包

## 使用方法

### V7.62 以上的版本

V7.62 以上的 J-Link 版本对设备描述的 xml 进行了解耦，为了使 J-Link 软件能够识别新设备，需要将先前创建的 XML 文件放在中央 JLinkDevices 文件夹中。

我们可以在以下路径找到：

| 操作系统 |                         路径                          |
| :------: | :---------------------------------------------------: |
| Windows  |  C:\Users\<USER>\AppData\Roaming\SEGGER\JLinkDevices  |
|  MacOS   | $HOME/Library/Application Support/SEGGER/JLinkDevices |
|  Linux   |           $HOME/.config/SEGGER/JLinkDevices           |

如果没有找到`JLinkDevices`文件夹，可以手动创建一个。

打开该文件夹之后，将此仓库下的`AirM2M`文件夹复制过去即可。

### V7.62 以下的版本

V7.62 以下的版本，需要自行拼接设备的 xml，我们打开安装的`J-Link`的安装目录，找到`JLinkDevices.xml`文件，将此仓库下的`all.xml`文件中的内容复制插入到`JLinkDevices.xml`文件中最后的`</Database>`标签前。然后在`Devices`文件夹中新建一个`AirM2M`文件夹，然后将此仓库下的`AirM2M/FLM`中的全部 FLM 文件复制过去
