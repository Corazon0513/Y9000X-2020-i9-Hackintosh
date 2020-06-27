# 联想Y9000X 2020 顶配 黑苹果OC引导
### [Corazon0513](https://github.com/Corazon0513)/[Y9000X-2020-i9-Hackintosh](https://github.com/Corazon0513/Y9000X-2020-i9-Hackintosh)

---

硬盘M位为原厂PM981A**已屏蔽**，硬盘S位为SN750。更换了DW1820A无线网卡。

⚠️注意: 如果新增加(或替换)的非PM981A硬盘位于M槽（靠近笔记本出风口的硬盘位），您需要将ACPI文件夹下的SSDT-DNVMe.aml与SSDT-DNVMe2文件**互换文件名**，否则无法正常识别硬盘。

解锁了[CFG](http://bbs.pcbeta.com/viewthread-1845189-1-1.html)， 实测顶配(i9-32G-2T-UHD)的CFG地址也是0x3E，可放心按照教程修改。

感谢[@WangRicky](https://github.com/WangRicky)前辈的[Y9000X-HACKINTOSH](https://github.com/WangRicky/Y9000X-HACKINTOSH)，本EFI基于他的EFI修改而来！


自用EFI，有需要可**自取使用**（白嫖许可）。

欢迎提issue交流！

## 三码已删除，请自行添加。
## 如对您有帮助，请 ~~一键三连~~ **🌟点亮Star**。


---

## 目前存在的问题（以及可能的问题）：
0. 外放无声。
    - 正在尝试开发驱动，如有兴趣请移步[Corazon0513/VoodooI2CTAS2770](https://github.com/Corazon0513/VoodooI2CTAS2770)。

1. 蓝牙不稳定。
    - 具体现象为蓝牙鼠标间歇性断连，尚未确认是DW1820还是macOS的问题。
  
2. 睡眠有概率暴毙，且CPU温度超级高。
    - ~~追查崩溃日志后，问题源于核显驱动，目前暂未解决，遇到了只能强制关机。~~
    - ~~查询了一下相关信息，似乎白果也存在此问题，可能是macOS的核显驱动存在问题，看之后苹果如何处理这个issue。~~
    - 启用了PowerTimeoutKernelPanic这个Quirk，目前暂未出现该问题。

3. Apple Watch解锁不好使。
    - 重新登陆iCloud**似乎能**解决。
    - 在我的白果(iMac (27-inch, Late 2013))上，解锁似乎有些时候也不稳定…

4. **系统运行几秒卡几秒（偶发现象）。**
    - 目前~~只能选择强制重启。~~重启肯定能解决，但是有出现过问题自行消失的情况，很迷惑。
    - 在出现该问题的时候，通过操作系统的关机/重启行为必定导致死机。
    - 目前定位到Framebuffer驱动可能存在Bug。

5. ~~触摸板随机暴毙。~~
    - 感谢[liminghao1630/Y9000X-1080P-Hackintosh](https://github.com/liminghao1630/Y9000X-1080P-Hackintosh)的触摸板驱动方法，已正常驱动。
    - 但是出现过几次触摸板间歇性卡顿，睡眠/重启可解决。

6. Fn键功能不全。
    - 注：亮度调节是**Fn+K**与**Fn+B**。
    - 在我的Niz plum micro84键盘上，按下Pause Break键是亮度+， 按下ScrLock(Fn+Pause Break)是亮度-。

7. 指纹无法解锁（有生之年无解系列）。

8. 一瞬性花屏（不影响使用（对我来说））。

9.  外接HDMI好使，理论上DVI/VGA也好使，DP请自行测试。
