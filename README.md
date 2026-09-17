# sdcc-c251 — SDCC 的 MCS-51 / MCS-251 支持

[SDCC](https://sdcc.sourceforge.net/)（Small Device C Compiler）的 **MCS-251（Intel 80251）**
目标移植分支，并内置配套的 **Zig + C 工具链工作区**（`toolchain/`），面向 STC / AI 系列芯片。

- 上游：SDCC（sourceforge `git-mirror`）；本仓库为 [`gevico/sdcc-c251`](https://github.com/gevico/sdcc-c251) 的 fork
- 在 SDCC 中加入 `mcs251` 目标：`sdcc -mmcs251`（24 位地址空间、1T 时序等），并与 Zig 自举后端共用 ASxxxx 链接流程
- 配套工具链：`toolchain/`（示例、库、设备描述表、xmake 构建、中文文档），见
  [`toolchain/README.md`](toolchain/README.md)
- 上游 SDCC 的原始 README 已重命名为 [`README-sdcc.md`](README-sdcc.md)

## 目录

| 路径 | 说明 |
| --- | --- |
| `src/`、`sdas/`、`device/`、`sim/`、`debugger/`、`support/` | SDCC 本体（含 MCS-251 目标与汇编器/链接器） |
| `toolchain/` | 配套 Zig/C 工具链工作区（示例、库、设备表、文档、构建脚本） |
| `docs/` | 文档 / GitHub Pages 站点 |

## 许可

SDCC 本体为 **GPL-2.0**（见 [`COPYING`](COPYING)），其运行库另有条款；
本仓库新增的 `toolchain/` 内容同样以 **GPL-2.0** 发布。
