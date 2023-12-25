该 EFI 包含完整的驱动与补丁。由于 C940-14 4K 版本的特殊性。该 EFI 配置仅能用于完成设置向导后，顺利进入系统的前提下使用。

直接用于引导安装过程，会显示异常或者花屏

该 EFI 配置在 DP 节点下的显卡设备属性注入了 EIDI 信息。如果你的设备屏幕不是 4K 或者是其他型号的。也会显示异常或者花屏。

如遇到显示问题可尝试删除 AAPL00,override-no-connect 字段

通过终端输入 ioreg -l | grep IODisplayEDID 可获得你自己设备的 EDID 信息。更新到 AAPL00,override-no-connect 字段下即可
具体方法查阅（EDID 注入方法）word 文档