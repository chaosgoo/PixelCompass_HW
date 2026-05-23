# PixelCompass 文件说明与制作指南

[![English](https://img.shields.io/badge/Language-English-blue.svg)](./README.md)
[![Chinese](https://img.shields.io/badge/%E8%AF%AD%E8%A8%80-%E7%AE%80%E4%BD%93%E4%B8%AD%E6%96%87-red.svg)](#)

欢迎来到 PixelCompass 硬件资料库！本仓库包含了制作现实版《我的世界》磁石罗盘所需的全套开源生产资料。

完整图文教程： 具体的焊接步骤、BOOT 烧录截图等保姆级教程，请移步博客查看：[PixelCompass：一个成本更低、支持网页配置的《我的世界》实体罗盘](https://chaosgoo.com/pixelcompass-a-better-minecraft-compass-irl/)。


硬件包中包含了用于 PCB 制造的Gerber 文件、电路原理图以及辅助焊接工具。

* **`Gerber` 文件夹：** 如果你不需要修改电路设计，可以直接使用 Gerber 文件夹内的 `.zip` 压缩包，上传到任何 PCB 样板工厂（如立创商城、捷配等）一键下单打板。
* **`ibom.html` (交互式 BOM)：** 纯手工焊接的辅助工具（它还支持将物料清单导出为 `.xlsx` 表格）。
* **注意：** 在网页中只需点击任意元器件，即可高亮显示其在电路板上的具体物理位置。物料清单中标记为 **"ANT-F-2-2.4G-1.0mmFR4-WCH"** 的项目是一个**板载天线占位符**，不对应任何实体电子料，焊接时直接忽略即可。
* **`Acrylic_Panel_2026-05-23.epanm`:** 立创面板定制的专属工程文件。下单亚克力面板时，直接把这个文件上传到立创面板定制平台即可。
* **`PET.dwg`:** 用于裁切内部 PET 匀光膜/扩散膜的二维设计图纸（可用剪刀对照尺寸手工裁切）。

---

# 3D 打印外壳与结构件

所有的 3D 打印文件和打印配置（Print Profiles）均已托管至 **MakerWorld**：
[在 MakerWorld 获取 3D 打印文件](https://makerworld.com/en/models/2834513-minecraft-compass-irl%23profileId-3158927)

该外壳专为《我的世界》实体罗盘 v2 版本进行了精细优化与重构。打印盘（Plates）拆分为了以下几个版本：

* **盘 1（标准版 - 半透亚克力方案）：** 包含标准的外壳 `body` 部件。该配置专门用于搭配前表面 **1mm 厚、顶面 UV 印刷的黑色半透亚克力面板**。为了达到最佳的光线扩散效果，你需要在夹层中放置一张 **PET LGT075J 扩散膜**。
* **盘 2（多色版 - 无需亚克力）：** 包含一个完整的 `faceplate` 结构件，适合拓竹 AMS 进行多色打印。你可以完美还原游戏里经典的像素质感。耗材颜色推荐（参考 TiX 的配色方案）：
    * 黑、白两色：无特定品牌要求。
    * 深灰色：推荐 **拓竹官方耗材 10105**（或同等颜色）。
    * 浅灰色：推荐 **拓竹官方耗材 16101**（或同等颜色）。


* **盘 3（实验性双 AMS 六色版）：** 这是我早期的双 AMS 测试方案。我曾花了大把时间测试了无数种颜色组合、买了一堆料，但始终没找到最“完美”的效果，因此本盘仅供参考。

---

## 额外硬件注意事项

* **电池规格：** 外壳内部的电池仓是专为 **601535 锂电池 (280mAh)** 设计的。如果你计划换用更大容量的电池以获取更长的续航，你需要自行修改 3D 外壳的源文件以适配更大的电池尺寸。

---

## 固件与激活

* **`PixelCompass_Firmware_v1.0.bin`：** 编译好的固件。请使用 WCH（沁恒）官方提供的 **WCHISPTool** 烧录工具将其烧录至电路板中。
* **在线配置网页（Web Dashboard）：** [https://dash.chaosgoo.com/pixelcompass/](https://dash.chaosgoo.com/pixelcompass/)
* **如何激活：** 设备首次连接 Dashboard 需要输入免费的激活码。请直接前往我的 Ko-fi 店铺免费申领（系统会自动发信）：**[在 Ko-fi 免费获取激活码](https://ko-fi.com/s/ba9368da91)**。
设备首次连接 Dashboard 需要输入免费的激活码才能完成初始化。
如果你对如何进入 BOOT 模式、如何烧录芯片或者如何获取免费激活码感到困惑，我们在博客文章中用完整的带图步骤进行了解释：
**阅读 [PixelCompass：一个成本更低、支持网页配置的《我的世界》实体罗盘](https://chaosgoo.com/pixelcompass-a-better-minecraft-compass-irl/)**
