# Thinkpad-X1C4-Hackintosh，Model 20FB，2022年3月7日
Thinpad X1 Carbon 4th(2016) Hackintosh EFI
- OpenCore: ......**最新版0.7.8**
- SystemInfo: MacOS Catalina 10.15.7 (19H2)
- HardwareInfo: https://psref.lenovo.com/syspool/Sys/PDF/ThinkPad/ThinkPad_X1_Carbon_4th_Gen/ThinkPad_X1_Carbon_4th_Gen_Spec.PDF
 - IGPU: HD Graphics 520
 - CPU: Skylake, Intel Core i7-6600U
 - Disk: MZNLN512HMJP-000L7 Samsung 512GB SATA III 6Gb/s PM871a M.2 Solid State Drive
 - 主板芯片: Mobile 6th/7th Generation Intel(R) Processor Family I/O LPC Contraller(U Premium SKU)-9D48
 - Audio: Conexant CX20753/4;Intel Skylake HDMI
 - Network: Intel Ethernet Connection I219-LM（有线）
 - Network: Intel 18260NGW WiGig(Douglas Peak) Network Adapter,Intel Dual Band Wireless-AC 8260 AC 2x2 HMC WiFi Adapter（无线）

## 联想驱动管理硬件检测报告
================================================================
- 当前操作系统		Windows 10 64位
- 主机编号		20FBA01MCDR90M7BDF
- CPU系列		第六代智能英特尔酷睿i7
- CPU型号		i7-6600U
- CPU主频		2.6GHz
- 最高睿频		3.4GHz
- CPU缓存		4MB
- 核心架构		Skylake
- 核心/线程数		2/4
- 制程工艺		光刻  14nm
- 指令集		64-bit
- 功耗			15W
- 内存容量		16GB
- 内存类型		1866MHz LPDDR3（板载）
- 插槽数量		无(此机型为板载内存)
- 最大内存容量		16GB
- 硬盘容量		512GB(M.2 SSD)
- 光驱类型		无光驱
- 光驱描述		无
- 触控屏		不支持
- 屏幕尺寸		14英寸
- 显示比例		16:9
- 屏幕分辨率		2560x1440
- 屏幕技术		LED背光IPS显示屏, 防眩目显示屏; 最大开合角度180度
- 显卡类型		集成显卡
- 显卡芯片		Intel HD Graphics 520
- 显存容量		共享系统内存
- 摄像头		720p HD 摄像头
- 音频系统		HD Audio, Conexant CX11852 codec, Dolby DAX2
- 扬声器		立体声扬声器 1W×2
- 麦克风		Built-in Dual Array Microphone(内置双阵列麦克风)
- 无线网卡		Intel Tri-Band Wireless 18260(2x2 AC)(集成WiGig与蓝牙)
- 有线网卡		Gigabit Ethernet(千兆以太网卡), 带有OneLink+ 转 VGA/RJ45 转换器
- 蓝牙			BT 4.1
- 数据接口		3个USB3.0(左侧的USB接口为Always On)
- 视频接口		HDMI, Mini-DP, OneLink+ 转 VGA/RJ45 转换器
- 音频接口		Combo jack(麦克风/耳机二合一接口)
- 其它接口		Lenovo Onelink+ 接口
- 扩展插槽		Micro SD读卡器
- 读卡器		Micro SD读卡器(可以支持UHS-II SD)
- 指取设备		TrackPad 经典触控板 多点触控 3+2按键
- 键盘描述		6行全尺寸键盘, 背光键盘
- 指纹识别		有
- 电池类型		4芯锂聚合物电池(52Wh)
- 续航时间		具体时间视使用环境而定
- 电源适配器		65W SLIM AC Adapter
- 预装操作系统		Win10专业版64位
- WWAN			本机不带WWAN
- 其他			硬盘传输规范与速率：SATA 3.0(6.0Gb/s)
- OFFICE		无


# Summary
- [] Audio (AppleALC alc-layout-id: 14)
- [] Trackpad\RedPoint multi gestures
- [] Native IntelWifi (itlwm)
- [] Native Buletooth
- [] Battery status
- [] HDMI output works fine
- [] mini DP may cause build-in display black screen

# Update
- 2022.03.09 启动报错 提示 "OC：Driver HfsPlus.efi at 1 cannot be loaded - Unsupported!"

             - 搜索判断是HfsPlus.efi文件错误，需重装下载。
             - 验证了下，在U盘的HfsPlus.efi文件大小显示176.2KB，实际正常的大小应该是37KB。（https://github.com/acidanthera/OcBinaryData/blob/master/Drivers/HfsPlus.efi)

- 2022.03.08 启动的时候报错 提示 "oc grabbed zero systm-id for sb. this is not allowed halting on critlcal error" 

            - 国光教程：基本就是【Misc】-->【security】下的【SecureBootModel 】的问题，默认【Default 】可以改为【Disabled 】或其他。
            - High Sierra-Catalina (10.13-10.15):
                 If your model is not listed below, set to Disabled.

- https://apple.sqlsec.com/9-%E5%B8%B8%E8%A7%81QA/#reloaded 十、常见 QA 国光的黑苹果安装教程
- https://dortania.github.io/OpenCore-Install-Guide/config.plist/security.html#misc Apple Secure Boot

# Thanks
- https://apple.sqlsec.com/ 国光的黑苹果安装教程：手把手教你配置 OpenCore
- https://dortania.github.io/OpenCore-Install-Guide/ Dortania's OpenCore Install Guide
