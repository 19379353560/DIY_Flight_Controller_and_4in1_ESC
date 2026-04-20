# DIY 4合1 飞控 & 75A 电调

![75A 4-in-1 ESC banner](assets/cover.svg)

[![Open hardware](https://img.shields.io/badge/open-hardware-orange)](https://github.com/19379353560/DIY_Flight_Controller_and_4in1_ESC)
[![ESC](https://img.shields.io/badge/ESC-75A%20x4-red)](https://github.com/19379353560/DIY_Flight_Controller_and_4in1_ESC)
[![DSHOT600](https://img.shields.io/badge/protocol-DSHOT600-blue)](https://github.com/19379353560/DIY_Flight_Controller_and_4in1_ESC)
[![Stars](https://img.shields.io/github/stars/19379353560/DIY_Flight_Controller_and_4in1_ESC?style=social)](https://github.com/19379353560/DIY_Flight_Controller_and_4in1_ESC/stargazers)
[![Last commit](https://img.shields.io/github/last-commit/19379353560/DIY_Flight_Controller_and_4in1_ESC)](https://github.com/19379353560/DIY_Flight_Controller_and_4in1_ESC/commits/main)
[![Review snapshot](https://img.shields.io/github/v/release/19379353560/DIY_Flight_Controller_and_4in1_ESC?include_prereleases&label=review%20snapshot)](https://github.com/19379353560/DIY_Flight_Controller_and_4in1_ESC/releases/tag/review-2026-04-19)

> **English summary:** Open FPV hardware project for a 10-layer 75A 4-in-1 ESC
> board. The repository includes Gerber manufacturing files, schematic PDF, PCB
> previews, and design notes for DSHOT600, high-current routing, and Infineon
> gate-driver based MOSFET control.
>
> 自主设计的 FPV 无人机飞控与 4合1 电调一体板，从原理图到 PCB 布局全程独立完成。

> **Status:** Download the [review snapshot](https://github.com/19379353560/DIY_Flight_Controller_and_4in1_ESC/releases/tag/review-2026-04-19)
> and review [PROJECT_STATUS.md](PROJECT_STATUS.md) before manufacturing or
> powering this design. Hardware review and build reports are welcome through
> [the current ESC review request](https://github.com/19379353560/DIY_Flight_Controller_and_4in1_ESC/issues/1).

---

## 硬件规格

| 参数 | 规格 |
|---|---|
| 类型 | 4合1 电调（四路电调集成于单板） |
| 持续电流 | 75A × 4 |
| 支持协议 | DSHOT600 / DSHOT300 / PWM / Oneshot |
| PCB 层数 | **10 层** |
| MOS 驱动 | **英飞凌（Infineon）栅极驱动 IC** |
| 适用电压 | 3S ~ 6S LiPo |

---

## 设计亮点

### 10 层 PCB

10 层板设计为大电流路径提供了充裕的铜皮截面积与多层并联导流，相比常见的 4 层板：

- 电源层与地层各有多层并联，载流能力大幅提升
- 信号层与功率层完全隔离，消除大电流切换对 PWM 信号的干扰
- 更低的 PCB 走线阻抗，减少高电流下的压降与发热

### 英飞凌栅极驱动

采用英飞凌（Infineon）专用 MOS 栅极驱动 IC，相比通用驱动方案：

- 更快的栅极充放电速度，降低 MOS 管开关损耗
- 内置死区时间控制，防止上下桥臂直通
- 更强的驱动能力，支持大尺寸低 Rds(on) MOS 管，降低导通损耗
- 工业级可靠性，适应高温、高电流工作环境

### DSHOT600 数字协议

支持 DSHOT600 数字电调协议：

- 无需油门校准，数字信号抗干扰能力强
- 双向 DSHOT 支持转速反馈（RPM Telemetry），配合 INAV/Betaflight 实现 RPM 滤波
- 相比 PWM/Oneshot，延迟更低、精度更高

---

## 仓库文件

| 文件 | 说明 |
|---|---|
| `Gerber_75A电调_2026-03-17.zip` | PCB 制造文件，可直接提交打样 |
| `SCH_Schematic1_2026-03-17.pdf` | 完整原理图 |
| `PCB_75A电调_*.png` | PCB 各层预览图 |

---

## PCB 预览

![PCB 顶层](PCB_75A电调_2026-03-17.png)

---

## 相关项目

- [SkyPilot H743 飞控](https://github.com/19379353560/skypilot) — 配套飞控主板
- [INAV 优化固件](https://github.com/19379353560/inav) — 配套飞控固件

---

## Feedback Wanted

English feedback is welcome. The most useful review areas are high-current
routing, MOSFET gate-drive layout, thermal behavior, DSHOT signal integrity, and
manufacturing checks before ordering boards.

Start here: [75A 4-in-1 ESC review request](https://github.com/19379353560/DIY_Flight_Controller_and_4in1_ESC/issues/1)
or [discussion](https://github.com/19379353560/DIY_Flight_Controller_and_4in1_ESC/discussions/2).

See [ROADMAP.md](ROADMAP.md) for the current review, prototype, and validation
plan.

Related guide: [FPV hardware review checklist](https://19379353560.github.io/hardware-review-guide.html).

Safety notes: [SAFETY.md](SAFETY.md).
