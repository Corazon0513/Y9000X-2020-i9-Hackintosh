# 联想Y9000X 2020 顶配 黑苹果OC引导
### [Corazon0513](https://github.com/Corazon0513)/[Y9000X-2020-i9-Hackintosh](https://github.com/Corazon0513/Y9000X-2020-i9-Hackintosh)

---

硬盘M位为原厂PM981A**已屏蔽**，硬盘S位为SN750。更换了DW1820A无线网卡

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
0. ~~触摸板随机暴毙~~。
    - 感谢[liminghao1630/Y9000X-1080P-Hackintosh](https://github.com/liminghao1630/Y9000X-1080P-Hackintosh)的触摸板驱动方法，已正常驱动。
    - 但是出现过几次触摸板间歇性卡顿，睡眠/重启可解决。
0. Apple Watch解锁不好使。
    - 重新登陆iCloud**似乎能**解决。
0. 系统运行几秒卡几秒（偶发现象）。
    - 目前只能选择强制重启。
    - 怀疑是显卡驱动存在bug。
0. Fn键功能不全。
    - 注：亮度调节是**Fn+K**与**Fn+B**。
0. 指纹无法解锁（估计有生之年无解）。
0. 一瞬性花屏（不影响使用（对我来说））。
0. 外接显示未经测试，还请反馈(~~如果真的有人关注这个Repository的话)~~。
0. 睡眠有概率暴毙，且CPU温度超级高。
    - 追查崩溃日志后，问题源于核显驱动，目前暂未解决，遇到了只能强制关机。
