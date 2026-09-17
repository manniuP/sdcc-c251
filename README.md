# sdcc-c251 — SDCC 的 MCS-51 / MCS-251 支持

[SDCC](https://sdcc.sourceforge.net/)（Small Device C Compiler）的 **MCS-251（Intel 80251）**
目标移植分支，面向 STC / AI 系列芯片。

> **说明**
> - 本分支当前的提交**未修改任何 SDCC 源码**，仅新增/重命名了 README。
> - 本仓库作为**克隆基底**：以后若要「让 SDCC 支持某些特性」，就在此基础上修改
>   `src/`、`sdas/`、`device/` 等并提交，无需改动本说明之外的既有代码。

- 上游：SDCC（sourceforge `git-mirror`）；本仓库为 [`gevico/sdcc-c251`](https://github.com/gevico/sdcc-c251) 的 fork
- 分支 `mcs251-backend` 的唯一改动为 README（如上）；`main` 与上游 fork 一致
- MCS-251 支持：`sdcc -mmcs251`（24 位地址空间等），与 Zig 自举后端共用 ASxxxx 链接流程
- 上游 SDCC 的原始 README 已重命名为 [`README-sdcc.md`](README-sdcc.md)
- 相关仓库：
  - Zig 自举后端：<https://github.com/manniuP/zig-mcs51-backend>
  - 配套工具链集成仓（示例 / 库 / 设备表 / 文档）：<https://github.com/manniuP/mcs8051>

## 目录

| 路径 | 说明 |
| --- | --- |
| `src/`、`sdas/`、`device/`、`sim/`、`debugger/`、`support/` | SDCC 本体（含 MCS-251 目标与汇编器/链接器） |
| `docs/` | 文档 / GitHub Pages 站点 |

## 许可

SDCC 本体为 **GPL-2.0**（见 [`COPYING`](COPYING)），其运行库另有条款。
