# 开源 DIY 打印机 / 喷头 / 液体分配方案

以下项目与「买喷头 + DIY 打印机」或精度液体分配相关，可作为香水/香薰机的硬件参考。

## 1. IPJ-Bio（开源压电喷墨打印头）
- **链接：** https://github.com/CentroEPiaggio/IPJ-Bio
- **描述：** 为生物打印优化的开源压电式喷墨打印头。包含设计、喷嘴板、补液系统、电子控制。已成功打印细胞。
- **相关性：** 高。可用于精度液体喷射。

## 2. Sidekick / Liquid-Handler（开源液体分配机器人）
- **链接：** https://github.com/rodolfokeesey/Liquid-Handler
- **描述：** 低成本开源台式液体分配机器人（约 $710）。4 路电磁阀驱动泵，10 µL 增量。适合实验室自动化。
- **相关性：** 高。精度定量分配参考。

## 3. tuwrraphael/inkjet-printer（陶瓷薄膜喷墨打印机）
- **链接：** https://github.com/tuwrraphael/inkjet-printer
- **描述：** 定制喷墨打印机（用于陶瓷电解质层）。含控制软件（Web）、Zephyr 固件、Xaar128 驱动 PCB、CAD。
- **相关性：** 中高。有完整打印头驱动电子与控制参考。

## 4. michelelizzit/printer（旧喷墨打印机改 3D 打印机）
- **链接：** https://github.com/michelelizzit/printer
- **描述：** 用旧喷墨打印机零件搭建闭环控制 3D 打印机，含 Arduino 固件。
- **相关性：** 中。机械结构与控制参考。

## 5. DIY-Inkjet-Printers/DIY_Inkjet_Printer
- **链接：** https://github.com/DIY-Inkjet-Printers/DIY_Inkjet_Printer
- **描述：** 压电驱动代码与相关文件。
- **相关性：** 中。

## 6. Open Printer（Open Tools）
- **链接：** https://www.hackster.io/news/the-open-printer-is-a-raspberry-pi-zero-w-powered-fully-open-highly-flexible-inkjet-printer-30948a1787cc
- **描述：** Raspberry Pi Zero W + STM32 开源喷墨打印机，使用商业 HP 墨盒/喷头（可加注/第三方），支持卷纸。无 DRM。
- **相关性：** 高。现成的开源喷墨方案。

## 7. Dominik Meffert DIY Inkjet & CIJ（Hackaday）
- DIY Piezo Inkjet: https://hackaday.io/project/167446-diy-inkjet-printer
- CIJ Printer: https://hackaday.io/project/178762-cij-printer
- **描述：** 从零搭建压电喷墨与连续喷墨（CIJ）打印机。
- **相关性：** 高。纯 DIY 喷头探索。

## 8. automated-spray-from-3Dprinter
- **链接：** https://github.com/ilario/automated-spray-from-3Dprinter
- **描述：** 把 3D 打印机改装为自动喷涂设备（替换挤出机为喷嘴 + 泵）。
- **相关性：** 中高。简单改装参考。

## 9. Reprappable-inkjet（RepRap Wiki）
- **链接：** https://reprap.org/mediawiki/index.php?title=Reprappable-inkjet
- **描述：** 可用 RepRap 打印出大部分零件的实验性压电喷墨头。
- **相关性：** 中。历史实验。

## 其他控制器
- Paintress（开源压电喷头控制栈）：https://hackaday.io/project/206811-paintress-open-inkjetprinthead-controller

**注：** 以上均为公开可查项目。喷墨打印头对液体粘度、表面张力、溶剂敏感，用于香水需额外验证兼容性。
