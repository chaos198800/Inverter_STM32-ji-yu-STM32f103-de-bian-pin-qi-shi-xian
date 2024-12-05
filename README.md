# Inverter_STM32：基于STM32f103的变频器实现

## 项目描述

本项目是一个基于STM32f103微控制器的简单变频器实现。项目参考了瑞萨（Renesas）MCU SH7137的实现思路，旨在通过STM32f103实现变频器的核心功能。

## 项目进展

- **2014/10/24 9:00am**：完成了按键、12864液晶显示屏以及SPWM波产生的驱动程序。
- **2014/10/27 8:35am**：修复了之前定时器干扰液晶显示的BUG。问题原因是定时器中断内程序运行时间过长，影响了液晶的时序。通过优化中断内的计算，减少了程序运行时间，提高了效率，几乎消除了对液晶时序的干扰。
- **2014/11/12**：参考瑞萨的思路重新改写了程序，下午测试相电压显示正常。
- **2014/11/21**：线电压完全稳定正常，接上电机后可以转动，但力度不足且有振动。在增降频率时偶尔出现停转现象。
- **2014/12/1**：进一步优化和测试，项目仍在持续改进中。

## 主要功能

- **按键控制**：通过按键实现变频器的参数设置和控制。
- **12864液晶显示**：实时显示变频器的工作状态和参数。
- **SPWM波产生**：生成用于驱动电机的SPWM波形。

## 已知问题

- 在某些情况下，电机转动力度不足且有振动。
- 在增降频率时，偶尔会出现电机停转的现象。

## 未来计划

- 进一步优化电机控制的算法，提高电机的转动稳定性和力度。
- 增加更多的保护机制，确保变频器在各种工况下的稳定运行。
- 完善用户界面，提供更友好的操作体验。

## 如何使用

1. 下载本仓库的源代码。
2. 使用STM32开发环境（如Keil、IAR等）打开项目文件。
3. 根据需要修改配置参数，编译并下载到STM32f103开发板上。
4. 连接电机和相关外设，启动变频器进行测试。

## 贡献

欢迎任何形式的贡献，包括但不限于代码优化、BUG修复、功能扩展等。请通过提交Issue或Pull Request的方式参与项目。

## 许可证

本项目采用开源许可证，具体许可证类型将在后续更新中明确。

---

感谢您对本项目的关注和支持！

## 下载链接

[Inverter_STM32基于STM32f103的变频器实现](https://pan.quark.cn/s/6df7f82c7afa)