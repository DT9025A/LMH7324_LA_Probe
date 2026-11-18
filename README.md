# LMH7324_LA_Probe

使用 KiCad 进行设计的，基于 LMH7324 的 RIGOL PLA2216 逻分探头替代，在 DHO924S 上、62.5MHz 输入频率下实测可用。

![QQ图片20250116134415.jpg](https://image.lceda.cn/oshwhub/pullImage/65cffde63fc74316a18637dd5d69f0bd.jpg)

# 复刻指导

1. 请依据开源工程 [MSO5000/DHO900 逻辑探头](https://oshwhub.com/zoomf1/pla2216) 中的 "转接板新版本" 打样出转接板，并购买连接器；
2. 依据本工程中的 Gerber 文件打样出探头板，请勿直接使用立创 EDA 进行导出，以免出现意外的错误（即使打 1.6mm 板厚也可以大力出奇迹焊上 1.27mm 的 IDC 连接器）；
3. 购买元器件，LMH7324 在立创商城上约 80RMB / 片；
4. 进行焊接装配。

# 主要 BOM 清单

| 值 | 封装 | 数量 | 
| :---: | :---: | :---: |
| 3.3pF | 0402 | 16 |
| 27pF | 0402 | 16 |
| 100nF | 0402 | 64 |
| 499R | 0402 | 16 |
| 300R | 0402 | 16 |
| 90.9K | 0402 | 16 |
| 10K | 0402 | 16 |
| 49R9 | 4x0603 | 8 |
| 220R | 4x0603 | 8 |
| LMH7324 | WQFN-32-1EP_5x5mm_P0.5mm_EP3.1x3.1mm | 4 |

# Test pictures

校准截图：

![校准截图](https://image.lceda.cn/oshwhub/pullImage/2b80688fecf5411ea8ca110851d6c0ca.png)

62.5MHz 方波输入测试：

![QQ截图20250209165252.jpg](https://image.lceda.cn/oshwhub/pullImage/34a96b95e22c4ee1b5debf41b898cfae.jpg)

50MHz 正弦波输入测试：

![50MHz正弦波输入测试](https://image.lceda.cn/oshwhub/pullImage/a5cb5f6080d847f6ac6253db9d59dde5.png)

# References

- 感谢开源工程 [MSO5000/DHO900 逻辑探头](https://oshwhub.com/zoomf1/pla2216)
- 感谢 [EEVBlog](https://www.eevblog.com/forum/testgear/rpl1116-active-logic-probe-pod-for-1000z-series-teardown/) 中分享资料的各位

---

# LMH7324_LA_Probe

A KiCad-designed, LMH7324-based replacement for the RIGOL PLA2216 logic probe. Verified working on the DHO924S at **62.5 MHz input frequency**.

## Replication Instructions

1. **Adapter board**: Fabricate the adapter board according to the **“New Version of Adapter Board”** in the open-source project [MSO5000/DHO900 Logic Probe](https://oshwhub.com/zoomf1/pla2216), and purchase the connector.

   > **Note for non-Chinese users:** The adapter board is a third-party project hosted on OSHWHub (oshwhub.com). Downloading files from that site may require WeChat registration and a China mobile phone number, which can be a barrier for users outside China. The adapter project is released under **GPL 3.0**, but the project page also states "reprinting is prohibited without the author's authorization" — these two statements appear to be in tension. Please respect the original author's terms. This project links to / references the adapter design to the extent its license permits.

2. **Probe board**: Fabricate the probe board using the Gerber files provided in this project. **Do not export directly from LCEDA/JLCEDA**, to avoid unexpected errors. (Even with a 1.6 mm board thickness, a 1.27 mm IDC connector can still be soldered with some effort.)

3. **Components**: Purchase the components. The LMH7324 is approximately **80 RMB per piece** on LCSC (12/2024).

4. **Assembly**: Solder and assemble the boards.

## Main BOM

| Value | Package | Qty |
| :---: | :---: | :---: |
| 3.3pF | 0402 | 16 |
| 27pF | 0402 | 16 |
| 100nF | 0402 | 64 |
| 499R | 0402 | 16 |
| 300R | 0402 | 16 |
| 90.9K | 0402 | 16 |
| 10K | 0402 | 16 |
| 49R9 | 4x0603 | 8 |
| 220R | 4x0603 | 8 |
| LMH7324 | WQFN-32-1EP_5x5mm_P0.5mm_EP3.1x3.1mm | 4 |

## Test Pictures

- Calibration screenshot: 

![校准截图](https://image.lceda.cn/oshwhub/pullImage/2b80688fecf5411ea8ca110851d6c0ca.png)
  
- 62.5 MHz square wave input test: 

![QQ截图20250209165252.jpg](https://image.lceda.cn/oshwhub/pullImage/34a96b95e22c4ee1b5debf41b898cfae.jpg)
  
- 50 MHz sine wave input test: 

![50MHz正弦波输入测试](https://image.lceda.cn/oshwhub/pullImage/a5cb5f6080d847f6ac6253db9d59dde5.png)

## Specifications & Known Limitations

| Parameter | Value / Note |
| :--- | :--- |
| Front-end IC | LMH7324 (quad 700 ps high-speed comparator with RSPECL outputs) |
| Compatible oscilloscopes | RIGOL DHO924S (verified); PLA2216-style adapter required for MSO5000/DHO900 series |
| Verified input frequency | **62.5 MHz** |
| Probe PCB | 6-layer, **1.2 mm** thickness (ideal); 1.6 mm used in this design for cost saving |
| Adapter PCB | 2-layer, **1.2 mm** thickness |
| Ribbon cable | Recommended **≤ 0.5 m** to keep IR drop low |
| Impedance matching | **Not performed** due to the long ribbon cable; keep the default PCB stackup from JLCPCB (JLC06161H-3313 / 1.6mm) |
| Higher-frequency testing | **Not available** — no equipment/conditions to test above 62.5 MHz at the time of design |

> **Important:** The probe board is designed with a **1.2 mm** ideal thickness. If you order 1.6 mm for the probe main board to save cost, be aware that soldering the 1.27 mm IDC connector requires extra effort ("brute force" may be needed).

## JLCPCB Ordering Notes

- **Probe PCB**: 6-layer, **1.2 mm** thickness (ideal). If ordering 1.6 mm for cost reasons, expect a tighter fit for the IDC connector.
- **Adapter PCB**: 2-layer, **1.2 mm** thickness.
- **Surface finish**: **ENIG** is recommended.
- **Stencil**: Frameless SMD stencil, **"Custom Size"** (smaller non-framed option) to keep shipping cheap. The stencil should match the top side.
- **Stackup**: Keep the default stackup — impedance matching was not performed because of the long ribbon cable. JLC06161H-3313 / 1.6mm is used in this fabrication.
- **Do not re-export from the editor**: Use the provided Gerbers directly.

## DIY / Assembly Notes

- The project uses **0402 SMD components** and the **LMH7324 in a 5×5 mm WQFN package**, making hand assembly challenging.
- **Parts sourcing**: LCSC (立创商城) supports ordering/backorder and is a practical route for most BOM items. The 50-pin connectors and ribbon cable can be sourced from AliExpress — check pitch, pinout, and orientation carefully.
- **Recommended soldering approach**: Stencil for the top side, hot plate for the top side, and hand-solder the remaining bottom-side parts. This is the method used by the original builder.
- **DRC note**: The linked adapter board design has some **DRC errors** reported in Issue#2 (e.g., clearance between two ground points). The provided Gerbers are the intended fabrication files; do not re-export from the editor and expect DRC to pass cleanly without the same waivers.

## References

- Thanks to the open-source project [MSO5000/DHO900 Logic Probe](https://oshwhub.com/zoomf1/pla2216).
- Thanks to everyone who shared information in the [EEVBlog thread](https://www.eevblog.com/forum/testgear/rpl1116-active-logic-probe-pod-for-1000z-series-teardown/).