# Serenity 供应链卡点 Skill 合集 - 综合分析项目

<div align="center">
  <img src="./BestSkillFromAT.png" alt="BestSkillFromAT" width="720">
</div>

## 项目概述

本项目分析了 10 个基于 **Serenity (@aleabitoreddit)** 投资方法论的 GitHub 仓库，每个仓库都从不同角度提炼和应用了"供应链卡点"投资策略，最终整合为一个统一的终极框架。

> **Serenity 是谁？** Reddit WSB 传奇人物，以"RISC-V+AI"框架在 2019-2024 年间实现约 3800% 收益率。核心方法论：沿着产业链向上游追溯，找到"一旦断货，万亿产业就要地震"的关键节点——那个节点上的小盘股，就是下一个暴击机会。

---

## 仓库总览 (10/10)

| # | 仓库 | 特色 | 评分 |
|---|------|------|------|
| 1 | [muxuuu/serenity-skill](https://github.com/muxuuu/serenity-skill) | 核心方法论 + 最系统化 | ⭐⭐⭐⭐⭐ |
| 2 | [lanfuli/aleabito-serenity-skills](https://github.com/lanfuli/aleabito-serenity-skills) | 推文档案库 + 注意力雷达 | ⭐⭐⭐⭐ |
| 3 | [haskaomni/serenity](https://github.com/haskaomni/serenity) | Alpha 假设 + 本地数据库 | ⭐⭐⭐⭐ |
| 4 | [W-Y-P/Serenity-aleabitoreddit-skill](https://github.com/W-Y-P/Serenity-aleabitoreddit-skill) | 完整框架 + 财务翻译最深 | ⭐⭐⭐⭐⭐ |
| 5 | [ZadAnthony/serenity-skill](https://github.com/ZadAnthony/serenity-skill) | 中文 Claude 版 + 防幻觉最强 | ⭐⭐⭐⭐⭐ |
| 6 | [fadewalk/serenity-stock-choke](https://github.com/fadewalk/serenity-stock-choke) | A 股卡脖子 + 政策适配最佳 | ⭐⭐⭐⭐⭐ |
| 7 | [leslieyeo/serenity-reply](https://github.com/leslieyeo/serenity-reply) | 深度资料 + 心智模型蒸馏 | ⭐⭐⭐⭐ |
| 8 | [zongmin-yu/serenity-skills](https://github.com/zongmin-yu/serenity-skills) | 半导体供应链 + 垂直领域 | ⭐⭐⭐ |
| 9 | [yan-labs/serenity-aleabitoreddit](https://github.com/yan-labs/serenity-aleabitoreddit) | 推文档案 + 战绩校准 + skills.sh | ⭐⭐⭐⭐⭐ |
| 10 | [xvhaoran778-cyber/Serenity.SKILL](https://github.com/xvhaoran778-cyber/Serenity.SKILL) | 跨市场卡点 + 贝叶斯更新 | ⭐⭐⭐⭐ |

> 仓库 #9 此前因 SSL 问题未能获取，现已解决。仓库 #10 为 Oxagata-prog/serenity-skill (404) 的社区替代方案。详见 [ANALYSIS_SUMMARY.md](./docs/ANALYSIS_SUMMARY.md) 中的完整分析。

---

## 项目结构

```
BestSerenitySkillFromAT/
├── README.md                          # 本文件
├── SKILL.md                           # v3.0 Skill 入口 (各平台一行安装)
├── FINAL_UNIFIED_SKILL.md             # v2.0 存档版 Skill (单文件)
├── LICENSE                            # MIT
│
├── skills/serenity-unified/           # v3.0 模块化 Skill
│   ├── SKILL.md                       #   核心指令 (~200 行)
│   ├── knowledge/                     #   参考知识库
│   │   ├── market-adaptation.md       #     A 股/美股/全球市场适配
│   │   ├── mental-models.md           #     心智模型 + 决策启发式
│   │   └── supply-chain-map.md        #     供应链地图
│   └── templates/                     #   报告模板
│       ├── single-stock-report.md     #     单股报告模板
│       └── sector-report.md           #     赛道报告模板
│
├── docs/                              # 分析文档
│   ├── ANALYSIS_SUMMARY.md            #   10 仓库逐一深度对比
│   └── DEEP_OPTIMIZATION_REPORT.md    #   深度优化分析
│
├── muxuuu-serenity-skill/             # 仓库 1-10 (克隆的子仓库)
│   ...                                #   完整列表见下方克隆命令
```

---

## 核心文档

- [SKILL.md](./SKILL.md) — **v3.0 Skill (推荐使用)**，根目录入口，各平台一行安装
- [skills/serenity-unified/](./skills/serenity-unified/) — 模块化结构 (核心指令 + knowledge/ + templates/)
- [FINAL_UNIFIED_SKILL.md](./FINAL_UNIFIED_SKILL.md) — v2.0 存档版 (单文件 691 行)
- [docs/ANALYSIS_SUMMARY.md](./docs/ANALYSIS_SUMMARY.md) — 10 仓库逐一深度分析、核心差异矩阵、关键洞察
- [docs/DEEP_OPTIMIZATION_REPORT.md](./docs/DEEP_OPTIMIZATION_REPORT.md) — 三种演化路径、四代防幻觉机制等独立分析

---

## 快速开始

### 一行安装

根据你的 Agent 工具，选一条命令执行即可：

```bash
# Codex — 告诉 Codex:
"帮我从 GitHub 拉取 yux1azhengye/BestSerenitySkillFromAT 并把根目录的 SKILL.md 安装为 skill"

# skills.sh (Codex 通用)
npx skills add yux1azhengye/BestSerenitySkillFromAT

# Claude Code (全局，任意目录可用)
git clone https://github.com/yux1azhengye/BestSerenitySkillFromAT.git ~/.claude/skills/serenity-unified-skill

# Cursor
git clone https://github.com/yux1azhengye/BestSerenitySkillFromAT.git /tmp/serenity && cp /tmp/serenity/SKILL.md .cursor/rules/serenity-unified.mdc

# Gemini CLI
git clone https://github.com/yux1azhengye/BestSerenitySkillFromAT.git /tmp/serenity && cp /tmp/serenity/SKILL.md GEMINI.md
```

### 触发示例

```
/serenity 分析一下 $NVDA 这只票值不值得
帮我用 Serenity 的方式看 1.6T 光模块这条链还有没有没被定价的卡点
用 Serenity 的方式看 A 股 AI 半导体哪个最值得研究
```

### 按需选择原始仓库

- **A 股用户**：`fadewalk/serenity-stock-choke` 或 `ZadAnthony/serenity-skill`
- **美股用户**：`W-Y-P/Serenity-aleabitoreddit-skill` 或 `muxuuu/serenity-skill`
- **追踪 Serenity 本人**：`lanfuli/aleabito-serenity-skills` (6,120 帖 + 注意力雷达)
- **本地可视化**：`haskaomni/serenity` (`python3 scripts/server.py --port 8787`)

### 克隆全部仓库

```bash
git clone https://github.com/muxuuu/serenity-skill.git muxuuu-serenity-skill
git clone https://github.com/lanfuli/aleabito-serenity-skills.git lanfuli-aleabito-serenity-skills
git clone https://github.com/haskaomni/serenity.git haskaomni-serenity
git clone https://github.com/W-Y-P/Serenity-aleabitoreddit-skill.git WYP-Serenity-aleabitoreddit-skill
git clone https://github.com/ZadAnthony/serenity-skill.git ZadAnthony-serenity-skill
git clone https://github.com/fadewalk/serenity-stock-choke.git fadewalk-serenity-stock-choke
git clone https://github.com/leslieyeo/serenity-reply.git leslieyeo-serenity-reply
git clone https://github.com/zongmin-yu/serenity-skills.git zongmin-yu-serenity-skills
git clone https://github.com/yan-labs/serenity-aleabitoreddit.git yan-labs-serenity-aleabitoreddit
git clone https://github.com/xvhaoran778-cyber/Serenity.SKILL.git xvhaoran778-cyber-Serenity-SKILL
```

---

## 免责声明

**不是投资建议 (NOT investment advice)**。本项目仅用于学习、研究投资分析方法论。任何标的、信念分档、估值区间都不构成买卖建议；真金白银请自行 DYOR。

**第三方独立提炼，非官方、未获授权背书**。本项目基于多个公开仓库自底向上整合，与 @aleabitoreddit 没有任何关联。

**他的战绩均为其本人自述、未经独立审计**，引用时务必带此限定。投资有风险，决策风险与后果由使用者自行承担。

---

## 许可证

MIT — 随便用，随便改，随便造。方法论提炼内容供个人学习/研究使用，底层投资观点版权归原作者所有。

---

## 致谢

感谢以下开源作者：@muxuuu、@ZadAnthony、@W-Y-P、@fadewalk、@lanfuli、@haskaomni、@leslieyeo、@zongmin-yu、@yan-labs、@xvhaoran778-cyber。

以及原始方法论来源：**Serenity (@aleabitoreddit)** — X/Twitter 上的 AI/半导体供应链分析师。

---

*本文档于 2026 年 6 月 7 日更新*
