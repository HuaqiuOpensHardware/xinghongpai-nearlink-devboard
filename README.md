# 星鸿派-星闪开发板

本仓库用于归档华秋开源硬件社区项目 **星鸿派-星闪开发板** 的公开资料，来源页面为：

https://p.eda.cn/d-1328625634846441472

归档日期：2026-07-15

## 归档原则

- 仅做资料归档与 GitHub 上传，未改动原始硬件文件、软件源码、BOM、文档或工具包。
- 所有上游附件均以源站下载得到的原始压缩包或原始文件形式保存。
- 新增内容仅包括本 `README.md`、`MANIFEST.json` 校验清单，以及 `enclosure/README.md` 归档说明。
- 若需要查看源码或硬件设计，请在本地解压对应 zip；仓库内不展开源码，避免引入无意修改。

## 项目简介

星鸿派-星闪开发板是一款面向物联网、智能家居、无线通信教学与嵌入式实验的开源开发板。项目基于海思 WS63V100 系列平台，围绕 Wi-Fi、BLE 与 SLE/星闪通信能力，配套 OpenHarmony 示例、Hispark 非 OH SDK 示例、课程文档、官方芯片资料和 KiCad 硬件设计文件。

开发板板载常用实验外设，适合从基础 GPIO、定时器、消息队列等系统能力开始，逐步扩展到 OLED 显示、温湿度采集、按键输入、继电器/风扇/水泵等外设控制场景。

## 核心信息

| 项目 | 内容 |
| --- | --- |
| 项目名称 | 星鸿派-星闪开发板 |
| 项目作者 | 星鸿派 |
| 源站发布时间 | 2026-01-15 13:37:14 |
| 主控平台 | 海思 WS63V100 系列 |
| 无线能力 | Wi-Fi、BLE、SLE/星闪 |
| 操作系统/生态 | OpenHarmony，另含 Hispark 官方 SDK 方式示例 |
| 硬件形态 | KiCad 双层 PCB，源站标注 PCB 尺寸约 96 mm x 70 mm |
| 源站许可证标注 | CERN Open Hardware License |
| 备注 | 源站正文另提到 Apache 2.0 商用友好声明；实际使用前请以附件内许可证或项目方最终说明为准。 |

## 板载与扩展资源

| 模块 | 说明 |
| --- | --- |
| USB Type-C | 供电与数据连接入口 |
| 稳压电源 | 5 V 转 3.3 V 供电链路 |
| USB 转串口 | CH340N，用于串口调试或下载辅助 |
| 温湿度传感器 | AHT20，I2C 温湿度采集 |
| 显示屏 | 0.96 英寸 I2C OLED，128 x 64 |
| 输入按键 | 多个用户按键与复位按键 |
| 指示灯 | 电源/状态提示 |
| 扩展接口 | 预留外设扩展引脚，便于连接实验模块 |

## 仓库目录

```text
.
├── assets/
│   └── images/                    # 源站封面、预览图、二维码等图片素材
├── docs/
│   ├── course/                    # 课程文档压缩包
│   └── ws63-official/             # WS63 系列官方文档压缩包
├── enclosure/
│   └── README.md                  # 外壳/结构件归档说明
├── hardware/
│   ├── bom/                       # 生产 BOM
│   └── pcb/                       # KiCad PCB/原理图工程压缩包
├── software/
│   ├── hispark-sdk-non-oh/        # Hispark 官方 SDK 方式示例
│   ├── resources/                 # 烧录、串口、驱动等软件资料
│   └── source/                    # OpenHarmony 示例源码压缩包
├── MANIFEST.json                  # 文件来源、大小、SHA256 校验
└── README.md
```

## 文件清单

| 路径 | 内容 | 大小 |
| --- | --- | ---: |
| `hardware/pcb/01-星鸿派PCB.zip` | KiCad 硬件工程，包含 `.kicad_sch`、`.kicad_pcb`、`.kicad_pro` | 2.08 MB |
| `hardware/bom/BOM_Board1_Schematic1_2026-01-09.xlsx` | 生产 BOM 与元件清单 | 13.2 KB |
| `software/source/02-程序源码.zip` | OpenHarmony 示例源码，含线程、定时器、GPIO、OLED、AHT20、PWM、Wi-Fi 等示例 | 589 KB |
| `software/resources/03-软件资料.zip` | USB 转串口驱动、串口调试助手、海思芯片烧录工具等 | 11.5 MB |
| `docs/course/04-课程文档.zip` | 开发环境、烧录、外设实验、Wi-Fi 等课程文档 | 5.33 MB |
| `software/hispark-sdk-non-oh/05-Hispark官方SDK方式（非OH）.zip` | Hispark 官方 SDK 方式示例代码 | 3.31 MB |
| `docs/ws63-official/06-WS63系列官方文档.zip` | WS63V100 官方 PDF/CHM/Markdown 资料 | 22.9 MB |
| `assets/images/cover.png` | 项目封面图 | 264 KB |
| `assets/images/schematic-preview.png` | 原理图预览图 | 106 KB |
| `assets/images/pcb-preview.png` | PCB 预览图 | 473 KB |

完整下载来源、字节大小与 SHA256 校验值见 `MANIFEST.json`。

## 外壳与结构件说明

本次从源站可见附件与压缩包目录清单中，未发现独立外壳、结构件或 3D 打印文件，例如 `.stl`、`.step`、`.stp`、`.iges`。因此仓库保留 `enclosure/README.md` 作为归档说明；若项目方后续公开外壳文件，可按原始文件形式补充到 `enclosure/` 目录。

## 使用建议

1. 克隆仓库后，根据需要解压对应资料包。
2. 硬件设计请优先查看 `hardware/pcb/01-星鸿派PCB.zip`，使用 KiCad 打开工程文件。
3. 物料采购、焊接或复刻前，请核对 `hardware/bom/` 中的 BOM，并结合原理图、PCB 与实物版本确认封装和替代料。
4. OpenHarmony 示例请从 `software/source/02-程序源码.zip` 解压后查看。
5. 非 OpenHarmony/Hispark SDK 方式示例请查看 `software/hispark-sdk-non-oh/`。
6. 烧录、串口、驱动类工具请查看 `software/resources/03-软件资料.zip`。
7. WS63V100 芯片能力、AT、MQTT、HTTP、lwIP、TLS/DTLS、文件系统等接口资料请查看 `docs/ws63-official/06-WS63系列官方文档.zip`。

## 校验方式

可使用 PowerShell 校验单个文件：

```powershell
Get-FileHash "hardware\pcb\01-星鸿派PCB.zip" -Algorithm SHA256
```

也可以与 `MANIFEST.json` 中记录的 `sha256` 字段逐项比对。

## 重要声明

- 本仓库是资料归档仓库，不是上游项目的开发分支。
- 上传归档未对硬件、软件、文档、工具包内容做二次编辑。
- 版权、商标、许可证和使用风险以原项目方及附件内声明为准。
- 第三方工具、驱动、烧录软件和芯片文档可能各自带有独立许可或使用限制，使用前请自行核对。
