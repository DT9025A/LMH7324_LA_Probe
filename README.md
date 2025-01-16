# LMH7324_LA_Probe

使用 KiCad 进行设计的，基于 LMH7324 的 RIGOL PLA2216 逻分探头替代，在 DHO924S 上、50MHz 输入频率下实测可用。

![QQ图片20250116134415.jpg](https://image.lceda.cn/oshwhub/pullImage/65cffde63fc74316a18637dd5d69f0bd.jpg)

# 复刻指导

1. 请依据开源工程 [MSO5000/DHO900 逻辑探头](https://oshwhub.com/zoomf1/pla2216) 中的 "转接板新版本" 打样出转接板，并购买连接器；
2. 依据本工程中的 Gerber 文件打样出探头板，请勿直接使用立创 EDA 进行导出，以免出现意外的错误（即使打 1.6mm 板厚也可以大力出奇迹焊上 1.27mm 的 IDC 连接器）；
3. 购买元器件，LMH7324 约 80RMB / 片；
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

50MHz 正弦波输入测试：

![50MHz正弦波输入测试](https://image.lceda.cn/oshwhub/pullImage/a5cb5f6080d847f6ac6253db9d59dde5.png)

5MHz 方波输入测试：

![方波输入测试](https://image.lceda.cn/oshwhub/pullImage/dd0323e8d4c540e383031ebf70f871f9.png)

# References

- 感谢开源工程 [MSO5000/DHO900 逻辑探头](https://oshwhub.com/zoomf1/pla2216)
- 感谢 [EEVBlog](https://www.eevblog.com/forum/testgear/rpl1116-active-logic-probe-pod-for-1000z-series-teardown/) 中分享资料的各位
