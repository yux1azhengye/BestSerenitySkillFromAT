# 供应链与垂直领域知识 (按需引用，非执行指令)

来源: zongmin-yu/serenity-skills, muxuuu/serenity-skill

## AI 基础设施供应链地图

### L0: 终端应用
- Hyperscaler AI factories (NVIDIA GB300 NVL72, Google TPU pods)
- Enterprise AI clusters
- Edge AI devices

### L1: 系统集成
- Server OEMs (Dell, HPE, Supermicro)
- Network equipment (Arista, Juniper)
- Storage systems

### L2: 模组/子系统
- GPU/TPU modules
- Optical transceivers (CPO, pluggable)
- Memory modules (HBM, GDDR)
- Power supplies

### L3: 器件/芯片
- Compute chips (GPU, TPU, CPU)
- Memory chips (HBM, DRAM, NAND)
- Optical components (lasers, modulators, detectors)
- Power semiconductors

### L4: 代工/封装/测试
- Foundries (TSMC, Samsung, Intel)
- Packaging (CoWoS, InFO, FCBGA)
- Testing (probe cards, handlers)

### L5: 外延/设备
- Epiwafers (InP, SOI, GaN)
- Equipment (lithography, etch, deposition)
- Materials (photoresist, gases, targets)

### L6: 材料/衬底
- Substrates (InP, SOI, SiC, GaN)
- Feedstock (polysilicon, metals)
- Specialty chemicals

---

## 光子学栈 (Photonics Stack)

### CPO (Co-Packaged Optics) 卡点层

1. **CW Lasers**: Continuous wave 激光器 (SIVE, AAOI, LITE)
2. **Optical Transceivers**: 光收发器 (LITE, COHR, INPHI)
3. **Silicon Photonics**: 硅光子平台 (GlobalFoundries, Intel, Tower)
4. **InP Substrates**: 磷化铟衬底 (AXTI, Sumitomo, JX Nippon)
5. **pBN Crucibles**: pBN 埚 (唯一供应商)
6. **Testing/Qualification**: 测试认证 (Keysight, Anritsu)

### 经典战例 (仅作示例，数据需实时更新)

| 标的 | 卡点定位 | 表现 (示例) |
|------|---------|------------|
| $AXTI | InP 衬底全球唯三产商，6 英寸产能全球稀缺 | $12 -> $104+ |
| $AAOI | CPO 激光器主力，微软/谷歌核心供应商 | - |
| $SIVE | CPO 激光器 + 硅光子，德国 K 受益产线 | 2 个月 +316% |
| $IQE | Compound semiconductor epiwafers | 2 个月 +316% |
| $RPI | LSE 小盘，帖发后两天涨 50% | Bloomberg/Reuters/FT 全报了 |

> 以上数据为历史示例，使用时必须用实时数据校准。

---

## 半导体设备栈

### 关键设备

| 环节 | 龙头 | 卡点程度 |
|------|------|---------|
| Lithography | ASML (EUV/DUV) | 极高 (全球唯一 EUV) |
| Etch | Lam Research, TEL | 高 |
| Deposition | Applied Materials, ASM International | 高 |
| CMP | Applied Materials, Ebara | 中高 |
| Metrology | KLA, Hitachi High-Tech | 高 |
| Testing | Teradyne, Advantest | 中高 |

### 卡点材料

| 材料 | 主要供应商 | 卡点程度 |
|------|-----------|---------|
| Photoresist | JSR, TOK, Shin-Etsu | 极高 (日企垄断) |
| Specialty Gases | Linde, Air Liquide | 高 |
| Targets | Honeywell, JX Nippon | 中高 |
| Polishing Pads | Dow, Fujimi | 中 |

---

## 其他垂直领域模板 (待扩展)

以下领域需要后续补充详细的供应链地图和卡点分析:

- **机器人**: 减速器 (哈默纳科/纳博特斯克)、伺服电机、控制器
- **电力液冷**: 冷板、CDU、液冷管路、冷却液
- **内存 HBM**: TSV 封装、HBM 堆叠、先进封装产能
