# 嘉立创（JLCPCB / EasyEDA）相关开源项目

**结论：** 目前**没有**发现嘉立创官方或社区提供的开源喷墨打印机控制板、喷头驱动器或完整开源打印机方案。

嘉立创侧重点是 PCB 制造 + EDA 软件。社区开源项目主要是：
- EasyEDA / 嘉立创 EDA 扩展与插件
- Gerber 转换、BOM 导出、元件库
- AI / MCP 接口用于自动化设计

## 代表项目
- **jlcmcp**（嘉立创 EDA MCP Server）：https://github.com/hyl64/jlcmcp  
  AI 助手直接控制嘉立创 EDA（布局、布线、DRC 等）。
- **EDA-Toolbox**：https://github.com/JasonYANG170/EDA-Toolbox  
  嘉立创 EDA / EasyEDA 实用工具集。
- **kicad-jlcpcb-tools**：https://github.com/harry10086/kicad-jlcpcb-tools  
  KiCad 生成嘉立创 BOM + CPL。
- **openjlc / FreeJLC**：Gerber 转换为嘉立创格式的工具。
- EasyEDA 官方扩展组织：https://github.com/orgs/easyeda/repositories （多个 PCB 辅助工具）

## 与打印机的关系
在其他开源喷墨项目中（例如 tuwrraphael/inkjet-printer）有自制打印头驱动 PCB，这些 PCB 可以用嘉立创打样，但嘉立创本身并不提供打印机控制方案。

如果需要自制喷头驱动板或控制板，可以参考上面的开源电子设计，然后用嘉立创制造 PCB。
