# Serenity 供应链卡点 Skill 合集 - 综合分析

## 概述

本文档分析了10个基于 Serenity (@aleabitoreddit) 投资方法论的 GitHub 仓库，每个仓库都从不同角度提炼和应用了"供应链卡点"投资策略。

---

## 仓库分析汇总

### 1. muxuuu/serenity-skill (核心方法论) ⭐⭐⭐⭐⭐

**定位**: 最完整的通用方法论框架  
**版本**: 1.0.0  
**语言**: 英文为主，支持中文输出

**核心特点**:
- **完整的研究工作流**: market story → system change → required parts → supply-chain layers → scarce constraints → public companies → evidence
- **深度研究默认**: 要求至少20家公司候选、25+信息来源
- **证据分级系统**: 强/中/弱/未验证线索四级分类
- **多市场适配**: A股、港股、美股、台湾、日本、韩国、欧洲全覆盖
- **评分工具**: 内置 `serenity_scorecard.py` 可重复评分脚本

**关键方法论**:
```
1. 设置范围 (市场/主题/时间窗口)
2. 故事转系统变化 (技术/经济驱动因素)
3. 映射价值链 (8层:下游需求→物理基础设施)
4. 找到稀缺层 (低供应商数/长认证/难扩张)
5. 建立公司宇宙 (≥20候选)
6. 收集证据 (优先一手来源)
7. 优先级排序 (需求压力/接近稀缺层/供应商集中度)
8. 解释失败条件
9. 给出下一步研究动作
```

**适用场景**: 
- 主题扫描 (A股AI半导体、CPO、HBM等)
- 单公司挑战
- 候选比较
- 学习模式

**独特价值**: 最系统化、工具最完整、跨市场能力最强

---

### 2. lanfuli/aleabito-serenity-skills (推文档案库 + 注意力雷达) ⭐⭐⭐⭐

**定位**: 数据驱动型 - 追踪Serenity本人的关注点  
**数据来源**: 6,120条帖子 (2025-07-02 → 2026-05-30), 750个ticker

**三个互锁技能**:

#### ① follow-aleabito (数据层)
- 通过X API抓取她的发帖
- 生成简报、累计提及分析、研究地图
- 全档案回填功能

#### ② serenity-method (分析方法通用化)
- 把她的风格套到任意股票
- 关键卡点/供应链OSINT发现 → 第一性原理 → Buffett五问质量门
- 叙事vs基本面卫生检查

#### ③ serenity-radar (注意力流向预测)
- 计算注意力动量 (升温标的、新进、重仓核心、主题轮动)
- 候选发生器 + 检查清单，不是预言机
- 包含她扛过的2025年11月回撤(IREN −38% / NBIS −35%)数据

**独特价值**: 
- **唯一基于真实历史数据的仓库** (6,120条帖子实证分析)
- 能预测"她下一步可能看什么"
- 避免过拟合到单边上涨窗口

**风险提醒**:
- 幸存者偏差 (档案天然偏向成功标的)
- 单账号脆弱性 (一个人、一种风格、一个时代)

---

### 3. haskaomni/serenity (Alpha假设 + 信号仪表盘) ⭐⭐⭐⭐

**定位**: 可视化 + 本地数据库方案  
**技术栈**: Python + SQLite + Yahoo Finance API

**核心功能**:
- 抓取X GraphQL curl，解析@aleabitoreddit帖子
- 抽取$SYMBOL，写入本地SQLite
- 下载日线价格 (Yahoo chart接口)
- Web Dashboard可视化

**Codex Skill**:
- `skills/serenity-stock-scorer`: 对单个ticker输出0-100的Serenity语料信号分
- 基于本地SQLite快照，不依赖网络

**部署方式**:
```bash
python3 scripts/ingest.py all --max-pages 10 --days 500 --min-mentions 3
python3 scripts/server.py --port 8787
# 访问 http://127.0.0.1:8787
```

**独特价值**:
- **完全本地化运行** (隐私保护)
- 可视化仪表盘直观展示
- 托管版可用 ([app.k2ai.dev](https://app.k2ai.dev))

**使用限制**: 需要从Chrome DevTools手动复制X登录态curl

---

### 4. W-Y-P/Serenity-aleabitoreddit-skill (完整框架) ⭐⭐⭐⭐⭐

**定位**: 模型无关的 chokepoint investing 框架  
**兼容性**: Codex, Claude Code, Cursor, Gemini CLI, Windsurf等

**核心哲学**:
> "Look beneath obvious AI winners and ask which obscure physical inputs can stop the whole buildout."

**七步工作流**:
```
1. 定义候选者和下游需求驱动
2. 映射供应链 (表格: Layer/Physical constraint/Known suppliers...)
3. 评分 chokepoint (不可替代性/稀缺性/需求杠杆/客户验证/经济捕获/市场忽视)
4. 构建证据阶梯 (一手源 > 技术源 > 社交媒体)
5. 转换为财务情景 (Base/Bull/Bear + 稀释审计)
6. 追踪催化剂和无效化点
7. 产出研究输出 (Thesis/Chokepoint Map/Evidence Table/Financial Scenario/Catalyst Calendar/Risk Checklist)
```

**输出模板**: 结构化的Markdown报告，包含:
- Chokepoint Map表格
- Evidence Quality表格
- Financial Translation表格
- Positioning Constraints表格
- Catalysts日历
- Risks清单

**独特价值**:
- **最注重财务翻译** (营收/毛利/EBITDA/现金/债务/稀释)
- 明确的证据质量分级
- 模型无关，任何Agent都能用

---

### 5. ZadAnthony/serenity-skill (中文Claude版) ⭐⭐⭐⭐⭐

**定位**: 最深入的中文实现 + 反确认偏误机制  
**知识底座**: 2071条推文自底向上提炼 + methodology.md (61.9KB)

**核心立场**:
1. 把市场当物理系统，不当ticker feed
2. 别问"这票能买吗"，要问"该查哪一层"
3. AI是苦力不是军师
4. Alpha = 信息合成的时间差

**输出契约 **(严格):
- **结论先行**: 一句话thesis + 客观空间 + 方向性买卖定档 (🔥Fire Sale ~ Sell五档)
- **事实底座**: 业务拆分/市值/营收/backlog/客户集中度 (每个数配"意味着什么")
- **分析**: 是不是好卡点 + 该值多少 (bear/base/bull三档，绑死假设)
- **结论与边界**: 值不值得 + 什么会证伪 + 适用边界

**独特创新**:
1. **反确认偏误内置**:
   - 风险/bear先写、bull后写 (顺序锁死)
   - 强制输出"什么会证伪这个thesis"
   - 用户有方向性暗示时反向加压

2. **独立复核机制**:
   - 派独立reviewer sub-agent挑刺反驳
   - 无sub-agent环境降级路径明确
   - 复核没过别硬发

3. **中文表达规范 **(必守):
   - 术语三分 (保留原文/首次给解释/直接译)
   - 禁英式句法 + 禁生造词 (信念档/五连判/用户头等内部黑话不得外泄)
   - 排版克制 (加粗≤25处)

4. **取数纪律 **(极严):
   - 一手源强制清单 (10-K/10-Q/8-K/IR原值 + as-of)
   - 虚构守门双向 (先在10-K找，找不到才标[推断])
   - 时效守门 (专门搜as-of前~60天新8-K/IR)
   - 精度降级规则 (含[推断]假设→降级为数量级/方向)

**赛道报告结构**:
- 赛道判定 (近端已定价 vs 远端未开闸)
- 先看懂这条链 (科普层，非专业读者必给)
- 供应链栈分层图 (L0→L5各层实时市值)
- 卡点层定位
- 剩余不对称在哪 (未发现>已re-rate)
- 催化剂/先行信号
- 红旗/证伪/边界

**独特价值**:
- **最严格的防幻觉机制** (独立复核 + 取数纪律)
- **最适合中文用户** (表达规范 + 教学融在分析里)
- **最透明** (methodology.md完整公开2071条推文提炼过程)

---

### 6. fadewalk/serenity-stock-choke (A股卡脖子) ⭐⭐⭐⭐⭐

**定位**: A股专用卡脖子选股框架 v2.0  
**数据源**: neodata-financial-search + westock-data

**六步通用推理链路**:
```
1. 定位板块所处周期阶段 (需求爆发期/技术跃迁期/供给受限期)
2. 溯源供应链，定位"卡脖子"节点 (终端→组装→零部件→材料→上游化工/矿产)
3. 找A股对应标的，建立"卡脖子定位"标签 (四维信号卡)
4. 筛选"真瓶颈"与"伪概念" (六条排除规则严格执行)
5. 多空双向确认 (不做单边多头)
6. 输出结构化分析报告 (七个部分强制包含)
```

**A股特色适配**:
| 维度 | 美股原版 | A股适配 |
|------|---------|--------|
| 政策权重 | 较低 | **极高** (政策直接催化) |
| 主力资金 | 对冲基金/机构 | **公募+私募+游资** |
| 散户结构 | 较少 | **散户占比高** |
| 壳资源 | 无此概念 | 小市值有**壳价值**溢价 |
| 国产替代 | 非核心 | **核心逻辑之一** |

**A股独有信号**:
- 龙虎榜 (营业部游资席位)
- 融资融券余额变化
- 主力净流入 (>5亿=机构明显建仓)
- 政府工作报告 (每年3月)
- 卡脖子清单 (国务院发布)

**工具箱**:
- neodata: 板块行情/供需缺口/研报/政策
- westock-data: 筹码成本/大宗交易/融资余额/机构评级/北向资金

**独特价值**:
- **唯一专为A股设计的仓库**
- 政策权重极高适配
- 游资/散户情绪纳入考量
- 国产替代作为核心逻辑

---

### 7. zongmin-yu/serenity-skills (半导体供应链) ⭐⭐⭐

**定位**: AI基础设施与半导体供应链专用  
**数据来源**: Serenity所有200+点赞的帖子 (1,000+条，跨越8个月)

**包含内容**:
- **4题快筛**: 判断是不是真的卡脖子
- **8步流程**: 怎么沿供应链往上游走
- **标准输出格式**: 分析报告的结构化模板
- **适用边界**: 什么情况下管用，什么情况下不管用

**安装方式**:
- Claude Code/Codex: 复制CLAUDE.md到项目根目录
- Cursor: 复制.cursor/rules/serenity-guidelines.mdc到.cursor/rules/

**独特价值**:
- **专注半导体/AI基础设施垂直领域**
- 轻量级，易集成
- 基于高赞帖子提炼 (质量过滤)

---

### 8. leslieyeo/serenity-reply (深度资料 + 心智模型蒸馏) ⭐⭐⭐⭐

**定位**: 认知操作系统蒸馏 (不只是方法，是思维框架)  
**调研深度**: 6维度 (1,700+推文、Substack长访谈、第三方分析、批评者观点)

**蒸馏层次**:
| 层次 | 数量 | 说明 |
|------|------|------|
| 心智模型 | 5个 | 供应链瓶颈理论、瓶颈博弈vs扩张估值、NVIDIA信号读取、信息不对称套利、正和市场观 |
| 决策启发式 | 8条 | chokepoint测试、NVIDIA跟随、欧洲小盘优先、反meme stock标签、机构跟随确认、反期权铁律、DYOR底线、地缘政治折价 |
| 表达DNA | 完整 | 高频词汇、句式指纹、回复风格、幽默模式、风险披露习惯 |
| 内在矛盾 | 3对 | gatekeeper张力、正确性张力、credential张力 |

**两种模式**:
- "Serenity会怎么看" → 第一人称扮演
- "帮我决定要不要买" → 顾问视角 (第三人称拆解，更安全)

**诚实边界 **(6条):
1. Credential未验证 (Nature论文/RISC-V成员/NVIDIA邀约均为self-reported)
2. 无公开认错记录
3. 幸存者偏差
4. 估值纪律缺失 (推广85x revenue小公司是真实弱点)
5. 调研时间局限 (2026年5月26日)
6. 一个不告诉你局限在哪的Skill，不值得信任

**质量验证**:
- Sanity Check (AXTI估值问题): ✅ 94%
- Edge Case (量子计算影响): ✅ 通过
- Style Check (表达辨识度): ✅ 8/10
- 一手来源占比: ✅ >70%

**独特价值**:
- **唯一蒸馏"表达DNA"和"内在矛盾"的仓库**
- 最透明的调研过程 (research文件夹全公开)
- 主动暴露局限性 (诚实度最高)
- 带质量验证报告

---

### 9. yan-labs/serenity-aleabitoreddit (推文档案库) ❌

**状态**: 克隆失败 (SSL/TLS连接失败)  
**预期定位**: 类似lanfuli的推文数据抓取和分析

**错误信息**:
```
fatal: unable to access 'https://github.com/yan-labs/serenity-aleabitoreddit.git/': 
schannel: failed to receive handshake, SSL/TLS connection failed
```

**可能原因**:
1. 仓库已设为私有
2. 仓库已被删除
3. 网络限制或DNS问题

**替代方案**: **lanfuli/aleabito-serenity-skills** 提供完全相同的功能
- ✅ 基于6,120条推文的完整档案
- ✅ X API数据抓取脚本
- ✅ 注意力雷达功能
- ✅ 提及分析和研究地图

**结论**: yan-labs仓库功能已被lanfuli仓库完全覆盖，无需额外获取。

---

### 10. Oxagata-prog/serenity-skill (轻量上手) ❌

**状态**: 仓库不存在 (404 Not Found)  
**预期定位**: 轻量级、简化版的Serenity skill，适合新手快速上手

**错误信息**:
```
remote: Repository not found.
fatal: repository 'https://github.com/Oxagata-prog/serenity-skill.git/' not found
```

**可能原因**:
1. 仓库从未存在（图片信息可能有误）
2. 仓库已被删除
3. 用户名错误或重命名

**替代方案**: **zongmin-yu/serenity-skills** 作为"轻量上手"的最佳替代
- ✅ 文件最少（仅10个文件 vs muxuuu的17个）
- ✅ README.zh.md仅1.9KB，极简风格
- ✅ CLAUDE.md仅3.4KB，易于理解
- ✅ 专注单一领域（半导体），学习曲线平缓

**其他轻量选择**:
- fadewalk/serenity-stock-choke (A股用户，六步法易理解)
- W-Y-P/Serenity-aleabitoreddit-skill (美股用户，模型无关)

**结论**: Oxagata仓库可能从未发布或已被删除，zongmin-yu提供更好的轻量级体验。

---

## 对比总结

### 按完整性排名

| 排名 | 仓库 | 完整性 | 理由 |
|------|------|--------|------|
| 1 | muxuuu/serenity-skill | ⭐⭐⭐⭐⭐ | 最系统化的工作流 + 工具最全 + 跨市场 |
| 2 | ZadAnthony/serenity-skill | ⭐⭐⭐⭐⭐ | 中文最佳 + 防幻觉机制最强 + 透明度最高 |
| 3 | W-Y-P/Serenity-aleabitoreddit-skill | ⭐⭐⭐⭐⭐ | 财务翻译最深入 + 模型无关 |
| 4 | fadewalk/serenity-stock-choke | ⭐⭐⭐⭐⭐ | A股专用 + 政策适配最好 |
| 5 | lanfuli/aleabito-serenity-skills | ⭐⭐⭐⭐ | 唯一基于真实历史数据 + 注意力雷达 |
| 6 | haskaomni/serenity | ⭐⭐⭐ | 可视化 + 本地化运行 |
| 7 | leslieyeo/serenity-reply | ⭐⭐⭐⭐ | 心智模型蒸馏 + 诚实度最高 |
| 8 | zongmin-yu/serenity-skills | ⭐⭐⭐ | 半导体垂直领域 + 轻量级 |

### 按特色分类

#### 🎯 方法论导向
- **muxuuu/serenity-skill**: 通用研究框架
- **W-Y-P/Serenity-aleabitoreddit-skill**: chokepoint investing框架
- **ZadAnthony/serenity-skill**: 中文操作化引擎

#### 📊 数据导向
- **lanfuli/aleabito-serenity-skills**: 推文档案 + 注意力雷达
- **haskaomni/serenity**: 本地数据库 + 可视化
- **yan-labs/serenity-aleabitoreddit**: (未获取)

#### 🇳 A股专用
- **fadewalk/serenity-stock-choke**: A股卡脖子框架v2.0
- **zongmin-yu/serenity-skills**: 半导体供应链 (偏A股)

#### 🧠 认知蒸馏
- **leslieyeo/serenity-reply**: 心智模型 + 表达DNA + 内在矛盾

### 核心差异矩阵

| 维度 | muxuuu | ZadAnthony | W-Y-P | fadewalk | lanfuli | haskaomni | leslieyeo |
|------|--------|-----------|-------|----------|---------|-----------|-----------|
| **语言** | 英/中 | 中文 | 英/中 | 中文 | 英/中 | 英/中 | 英/中 |
| **防幻觉** | 中等 | 极强 | 强 | 中等 | 弱 | 弱 | 强 |
| **数据基础** | 无 | 无 | 无 | 无 | 6,120帖 | 本地DB | 1,700帖 |
| **可视化工具** | 无 | 无 | 无 | 无 | 无 | Dashboard | 无 |
| **A股适配** | 有 | 有 | 无 | 专精 | 无 | 无 | 无 |
| **财务深度** | 中 | 深 | 最深 | 中 | 浅 | 浅 | 中 |
| **透明度** | 高 | 最高 | 高 | 高 | 高 | 中 | 最高 |
| **学习曲线** | 陡 | 中 | 中 | 平 | 陡 | 平 | 中 |

---

## 整合建议

### 终极SKILL架构

基于以上分析，建议整合为以下模块化架构:

```
serenity-unified-skill/
├── core/
│   ├── methodology.md          # 来自muxuuu/ZadAnthony的核心方法论
│   ├── workflow.md             # 九步工作流 (Scope Gate → 仓位逻辑)
│   └── output-contract.md      # 输出契约 (结论先行/判断显形)
│
├── data-layer/
│   ├── attention-radar/        # 来自lanfuli的注意力雷达
│   │   ├── patterns.md         # 6,120帖提炼的模式
│   │   └── radar.js            # 注意力动量计算
│   └── local-db/               # 来自haskaomni的本地数据库方案
│       ├── ingest.py           # X数据抓取
│       └── dashboard/          # 可视化
│
├── market-adapters/
│   ├── a-share/                # 来自fadewalk的A股适配
│   │   ├── policy-weight.md    # 政策权重
│   │   ├── signals.md          # 龙虎榜/融资/北向
│   │   └── tools.md            # neodata/westock查询
│   ├── us-market/              # 来自W-Y-P的美股适配
│   │   ├── filings.md          # SEC filings路径
│   │   └── liquidity.md        # 流动性/稀释风险
│   └── global/                 # 来自muxuuu的全球市场
│       ├── hk-jp-kr-eu.md      # 各地交易所filings
│       └── fx-geopolitics.md   # FX/地缘政治暴露
│
├── anti-hallucination/
│   ├── evidence-ladder.md      # 来自muxuuu的证据分级
│   ├── fact-checking.md        # 来自ZadAnthony的取数纪律
│   ├── independent-review.md   # 来自ZadAnthony的独立复核
│   └── precision-degradation.md # 精度降级规则
│
├── cognitive-model/
│   ├── mental-models.md        # 来自leslieyeo的5个心智模型
│   ├── heuristics.md           # 来自leslieyeo的8条决策启发式
│   ├── expression-dna.md       # 来自leslieyeo的表达DNA
│   └── limitations.md          # 来自leslieyeo的诚实边界
│
├── domain-specific/
│   ├── semiconductor/          # 来自zongmin-yu的半导体
│   │   ├── ai-infra-map.md     # AI基础设施地图
│   │   └── photonics-stack.md  # 光子学栈
│   └── verticals/              # 其他垂直领域模板
│       ├── robotics.md
│       ├── power-cooling.md
│       └── memory-hbm.md
│
├── tools/
│   ├── scorecard.py            # 来自muxuuu的评分工具
│   ├── validate_skill.py       # Skill结构验证器
│   ── examples/               # 示例报告
│       ├── a-share-ai-demo.md
│       └── us-photonics-demo.md
│
└── README.md                   # 统一入口文档
```

### 整合原则

1. **方法论统一**: 以muxuuu的九步工作流为主干，ZadAnthony的输出契约为标准
2. **数据增强**: 集成lanfuli的注意力雷达和haskaomni的本地数据库
3. **市场适配**: 保留fadewalk的A股专精和W-Y-P的美股深度
4. **防幻觉强化**: 采用ZadAnthony的独立复核 + 取数纪律 + 精度降级
5. **认知透明**: 融入leslieyeo的心智模型蒸馏和诚实边界
6. **垂直深化**: 保留zongmin-yu的半导体专业知识

### 使用场景路由

```
用户请求 → 路由器 → 选择模块组合

主题扫描 (A股AI半导体) → core + market-adapters/a-share + domain-specific/semiconductor
单公司挑战 (NVDA) → core + market-adapters/us-market + anti-hallucination
学习模式 (教方法) → core + cognitive-model + examples
注意力追踪 (她看什么) → data-layer/attention-radar
本地运行 (隐私保护) → data-layer/local-db
```

---

## 关键洞察

### 1. Serenity方法论的本质

所有仓库都认同的核心:
- **不是买铲子，是卡住卖铲人** (bottleneck the shovel sellers)
- **沿着钱流逆向追溯** (从下游capex往上推)
- **找single point of failure** (一旦断货整个产业停工)
- **小市值才有10x空间** (Sub-$2B门槛)
- **认证周期未反映当期营收 = 错杀机会**

### 2. 最大分歧点

**估值纪律**:
- muxuuu/W-Y-P/ZadAnthony: 强调估值纪律，反对85x revenue
- leslieyeo: 承认这是Serenity的真实弱点，Skill会复现这个弱点
- fadewalk: A股环境下更容忍高估值 (政策催化+游资炒作)

**Serenity本人角色**:
- ZadAnthony: 方法内化，Serenity按需冒头 (load-bearing时才提)
- lanfuli/leslieyeo: 追踪/模仿Serenity本人
- muxuuu/W-Y-P: 完全不提Serenity，纯方法论

### 3. 防幻觉机制演进

| 代际 | 代表仓库 | 机制 | 效果 |
|------|---------|------|------|
| Gen 1 | leslieyeo | 标注来源可信度 | 基础透明 |
| Gen 2 | muxuuu/W-Y-P | 证据分级 + 一手源优先 | 减少编造 |
| Gen 3 | ZadAnthony | 独立复核 + 取数纪律 + 精度降级 | 极强防幻觉 |
| Gen 4 | fadewalk | A股特有信号交叉验证 | 本土化防骗 |

### 4. 中文实现的突破

ZadAnthony的贡献:
- **中文表达规范**: 解决"英文翻过来"的问题
- **禁生造词**: 信念档/五连判/用户头等内部黑话不得外泄
- **教学融在分析里**: 读者看你怎么分析就学会了，不靠标签
- **反确认偏误内置**: bear先写、强制证伪门、反向加压

### 5. 数据驱动的局限

lanfuli/haskaomni的价值与风险:
- ✅ 价值: 基于真实历史数据，避免过拟合
- ❌ 风险: 幸存者偏差 (只看到成功的)、单账号脆弱性
- ⚖️ 平衡: 作为候选发生器，不是预言机

---

## 最终推荐

### 对于不同用户

**新手入门**:
1. 先用 **fadewalk/serenity-stock-choke** (A股用户) 或 **W-Y-P/Serenity-aleabitoreddit-skill** (美股用户)
2. 理解六步/七步工作流
3. 再看 **zongmin-yu/serenity-skills** 了解半导体垂直领域

**进阶研究**:
1. 切换到 **muxuuu/serenity-skill** 掌握完整方法论
2. 学习 **ZadAnthony/serenity-skill** 的防幻觉机制
3. 用 **haskaomni/serenity** 建立本地数据库

**深度定制**:
1. 阅读 **leslieyeo/serenity-reply** 理解心智模型和内在矛盾
2. 用 **lanfuli/aleabito-serenity-skills** 追踪注意力流向
3. 整合为个性化工作流

**生产环境**:
- 采用 **ZadAnthony/serenity-skill** 作为主干 (防幻觉最强)
- 集成 **lanfuli的注意力雷达** 作为数据层
- 根据市场选择 **fadewalk **(A股) 或 **W-Y-P **(美股) 作为适配器
- 定期用 **leslieyeo的诚实边界** 做自我审查

### 对于开发者

如果要创建统一的Serenity Skill:

1. **主干**: muxuuu的九步工作流 + ZadAnthony的输出契约
2. **防幻觉**: ZadAnthony的独立复核 + 取数纪律 + 精度降级
3. **数据层**: lanfuli的注意力雷达 + haskaomni的本地DB
4. **市场适配**: fadewalk (A股) + W-Y-P (美股) + muxuuu (全球)
5. **认知层**: leslieyeo的心智模型 + 诚实边界
6. **垂直领域**: zongmin-yu的半导体 + 自定义扩展

---

## 附录: 快速对照表

### 触发词对照

| 仓库 | 触发词 |
|------|--------|
| muxuuu | "用Serenity的方式看", "深度调研", "产业链/供应链/卡点/瓶颈" |
| ZadAnthony | `/serenity`, "分析一下$XXX", "帮我看XX链还有没有没被定价的卡点" |
| W-Y-P | "Serenity", "@aleabitoreddit", "chokepoint investing", "AI supply-chain bottlenecks" |
| fadewalk | "分析XX板块", "找XX卡脖子", "serenity分析", "A股瓶颈产业链" |
| lanfuli | "用Serenity的方法分析$X", "analyze $X like Serenity" |
| leslieyeo | "用Serenity的视角", "aleabitoreddit会怎么分析", "切换到Serenity模式" |

### 输出格式对照

| 仓库 | 输出风格 | 长度 | 结构化程度 |
|------|---------|------|-----------|
| muxuuu | 研究伙伴对话 | 中长 | 高 (表格+列表) |
| ZadAnthony | 投研报告 | 长 | 最高 (严格模板) |
| W-Y-P | 研究报告 | 中长 | 高 (Markdown表格) |
| fadewalk | 分析报告 | 中长 | 高 (七部分强制) |
| lanfuli | 五段式分析 | 短中 | 中 |
| leslieyeo | 对话/顾问 | 短中 | 低 (自然语言) |

### 证据标准对照

| 仓库 | 一手源要求 | 最低来源数 | 证据分级 |
|------|-----------|-----------|---------|
| muxuuu | 必须 | 25+ (深度扫描) | 强/中/弱/未验证 |
| ZadAnthony | 极严 (10-K/10-Q/8-K/IR) | 3+ (关键数字) | 已证实/管理层声称/推断/推测 |
| W-Y-P | 必须 | 2+独立确认 | 一级/二级/三级 |
| fadewalk | 推荐 | 无硬性要求 | 无明确分级 |
| lanfuli | 无 | 无 | 无 |
| leslieyeo | 推荐 | 无 | 可信度标注 |

---

*本文档于2026年6月6日完成，基于8个成功克隆的仓库分析 (yan-labs和Oxagata-prog未能获取)*
