# Serenity Supply Chain Chokepoint Skill Collection — Unified Analysis Project

<div align="center">
  <img src="./BestSkillFromAT.png" alt="BestSkillFromAT" width="720">
</div>

---

> **🌐 中文读者:** 见 [README.md](./README.md) 获取中文版本。
>
> **English readers:** you're in the right place. This is the complete English README.

---

## Project Overview

This project analyzes 10 GitHub repositories based on the **Serenity (@aleabitoreddit)** investment methodology. Each repository refines and applies the "supply chain chokepoint" investment strategy from a different angle, ultimately integrated into one unified ultimate framework.

> **Who is Serenity?** A Reddit WSB legend who achieved ~3,800% returns from 2019-2024 using the "RISC-V+AI" framework. Core methodology: trace upstream along the supply chain to find the critical node where *"if supply stops, a trillion-dollar industry shakes"* — the small-cap stock sitting at that node is the next asymmetric opportunity.

---

## Repository Overview (10/10)

| # | Repository | Highlight | Rating |
|---|-----------|-----------|--------|
| 1 | [muxuuu/serenity-skill](https://github.com/muxuuu/serenity-skill) | Core methodology, most systematic | ⭐⭐⭐⭐⭐ |
| 2 | [lanfuli/aleabito-serenity-skills](https://github.com/lanfuli/aleabito-serenity-skills) | Tweet archive + attention radar | ⭐⭐⭐⭐ |
| 3 | [haskaomni/serenity](https://github.com/haskaomni/serenity) | Alpha hypothesis + local database | ⭐⭐⭐⭐ |
| 4 | [W-Y-P/Serenity-aleabitoreddit-skill](https://github.com/W-Y-P/Serenity-aleabitoreddit-skill) | Full framework, deepest financial translation | ⭐⭐⭐⭐⭐ |
| 5 | [ZadAnthony/serenity-skill](https://github.com/ZadAnthony/serenity-skill) | Chinese Claude edition, strongest anti-hallucination | ⭐⭐⭐⭐⭐ |
| 6 | [fadewalk/serenity-stock-choke](https://github.com/fadewalk/serenity-stock-choke) | A-share chokepoint, best policy adaptation | ⭐⭐⭐⭐⭐ |
| 7 | [leslieyeo/serenity-reply](https://github.com/leslieyeo/serenity-reply) | Deep materials + mental model distillation | ⭐⭐⭐⭐ |
| 8 | [zongmin-yu/serenity-skills](https://github.com/zongmin-yu/serenity-skills) | Semiconductor supply chain, vertical domain | ⭐⭐⭐ |
| 9 | [yan-labs/serenity-aleabitoreddit](https://github.com/yan-labs/serenity-aleabitoreddit) | Tweet archive + track record calibration + skills.sh | ⭐⭐⭐⭐⭐ |
| 10 | [xvhaoran778-cyber/Serenity.SKILL](https://github.com/xvhaoran778-cyber/Serenity.SKILL) | Cross-market chokepoint + Bayesian updating | ⭐⭐⭐⭐ |

> Repo #9 was previously inaccessible due to SSL issues — now resolved. Repo #10 is the community replacement for Oxagata-prog/serenity-skill (404). See [ANALYSIS_SUMMARY.md](./docs/ANALYSIS_SUMMARY.md) for the full analysis.

---

## Project Structure

```
BestSerenitySkillFromAT/
├── README.md                              # Chinese README
├── README.en.md                           # This file (English)
├── SKILL.md                               # v3.0 Skill entry (Chinese)
├── SKILL.en.md                            # v3.0 Skill entry (English)
├── FINAL_UNIFIED_SKILL.md                 # Archived v2.0 (single file)
├── LICENSE                                # MIT
│
├── skills/serenity-unified/               # v3.0 Modular Skill
│   ├── SKILL.md                           #   Core instructions (Chinese, ~200 lines)
│   ├── SKILL.en.md                        #   Core instructions (English)
│   ├── knowledge/                         #   Reference knowledge base
│   │   ├── market-adaptation.md           #     A-share / US / Global (Chinese)
│   │   ├── market-adaptation.en.md        #     English version
│   │   ├── mental-models.md               #     Mental models + heuristics (mixed CN/EN)
│   │   └── supply-chain-map.md            #     Supply chain maps (mixed CN/EN)
│   └── templates/                         #   Report templates
│       ├── single-stock-report.md         #     Single-stock template (Chinese)
│       ├── single-stock-report.en.md      #     English version
│       ├── sector-report.md               #     Sector template (Chinese)
│       └── sector-report.en.md            #     English version
│
├── docs/                                  # Analysis documents
│   ├── ANALYSIS_SUMMARY.md                #   10-repo deep comparison
│   └── DEEP_OPTIMIZATION_REPORT.md        #   Deep optimization analysis
│
├── muxuuu-serenity-skill/                 # Repos 1-10 (cloned sub-repos)
│   ...
```

---

## Core Documents

- **[SKILL.en.md](./SKILL.en.md)** — **v3.0 Skill (recommended)**, root entry point, one-line install for all platforms
- **[skills/serenity-unified/SKILL.en.md](./skills/serenity-unified/SKILL.en.md)** — Core English instructions (9-step workflow, criteria, anti-hallucination)
- **[skills/serenity-unified/](./skills/serenity-unified/)** — Modular structure (core instructions + knowledge/ + templates/)
- **[FINAL_UNIFIED_SKILL.md](./FINAL_UNIFIED_SKILL.md)** — v2.0 archived version (single file, 691 lines)
- **[docs/ANALYSIS_SUMMARY.md](./docs/ANALYSIS_SUMMARY.md)** — 10-repo deep comparison, core difference matrix, key insights
- **[docs/DEEP_OPTIMIZATION_REPORT.md](./docs/DEEP_OPTIMIZATION_REPORT.md)** — Evolution paths, anti-hallucination mechanisms, independent analysis

---

## Quick Start

### One-Line Install

Pick the command for your agent:

```bash
# Codex — Tell Codex:
"Pull yux1azhengye/BestSerenitySkillFromAT from GitHub and install root SKILL.md as a skill"

# skills.sh (Codex universal)
npx skills add yux1azhengye/BestSerenitySkillFromAT

# Claude Code (global, works from any directory)
git clone https://github.com/yux1azhengye/BestSerenitySkillFromAT.git ~/.claude/skills/serenity-unified-skill
# For English version, swap the entry point:
cp ~/.claude/skills/serenity-unified-skill/SKILL.en.md ~/.claude/skills/serenity-unified-skill/SKILL.md

# Cursor
git clone https://github.com/yux1azhengye/BestSerenitySkillFromAT.git /tmp/serenity && cp /tmp/serenity/SKILL.en.md .cursor/rules/serenity-unified.mdc

# Gemini CLI
git clone https://github.com/yux1azhengye/BestSerenitySkillFromAT.git /tmp/serenity && cp /tmp/serenity/SKILL.en.md GEMINI.md
```

### Trigger Examples

```
/serenity analyze whether $NVDA is worth investing right now
Use Serenity's method to find unpriced chokepoints in the 1.6T optical transceiver chain
Find unknown bottlenecks in the AI infrastructure supply chain
Rank the best chokepoint candidates in US semiconductors under $2B market cap
Challenge this thesis: is the InP substrate bottleneck already priced in?
```

### Pick an Original Repo by Need

- **US stock investors**: `W-Y-P/Serenity-aleabitoreddit-skill` or `muxuuu/serenity-skill`
- **A-share (China) investors**: `fadewalk/serenity-stock-choke` or `ZadAnthony/serenity-skill`
- **Track Serenity himself**: `lanfuli/aleabito-serenity-skills` (6,120 posts + attention radar)
- **Local visualization**: `haskaomni/serenity` (`python3 scripts/server.py --port 8787`)

### Complementary Tools

While this skill provides the analytical framework, you'll need real-time data to feed it. A few tools that pair well with the chokepoint workflow:

- **SEC filings / transcripts**: direct from EDGAR, Fool Earnings Call Transcripts, or your broker's research portal
- **Supply chain OSINT**: LinkedIn supplier page changes, industry conference PPTs (GTC, OFC), trade journal teardowns
- **Terminal-based market data**: If you live in the terminal like many of us, **[AlphaTerminal](https://github.com/NLRX-WJC/AlphaTerminal)** provides a clean TUI for quick price checks, screener results, and macro snapshots without breaking your flow to open a browser — handy when you're bouncing between a 10-K and a supplier list and just need to spot-check a ticker's market cap or sector comps at a glance

### Clone All Repos

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

## What's Inside the Skill

The unified skill (`SKILL.en.md`) packs a complete chokepoint investing research engine:

- **9-Step Workflow** — from scope gate through independent review
- **9 Good-Chokepoint Criteria** — monopoly/irreplaceability, tiny market cap vs massive downstream TAM, designed-in + multi-customer, certification cycle mispricing, balance sheet survival, supply-demand imbalance, policy/geopolitical moat, low institutional ownership, valuation margin of safety
- **Red Flag Scan** — 12+ red flags that downgrade or veto a thesis (infinite ATM dilution = hard veto)
- **Valuation Framework** — relative valuation + share/cross-layer method, with precision-downgrade rules
- **Anti-Hallucination Mechanisms** — fabrication guard, freshness guard, evidence tier labels, mandatory independent review
- **Market Adaptation** — US (SEC filings), China A-share (CNINFO/exchange announcements), HK, TW, JP, KR, EU

---

## Disclaimer

> **NOT investment advice.** This project is for learning and studying investment analysis methodology only. No ticker, conviction tier, or valuation range constitutes buy/sell advice; do your own research before committing real capital.
>
> **Third-party independent synthesis, unofficial and unauthorized.** This project is a bottom-up integration from multiple public repositories and has no affiliation with @aleabitoreddit.
>
> **All track records are self-reported and unaudited.** Always cite with this qualifier. Investing involves risk; users bear full responsibility for their decisions and consequences.

---

## License

MIT — use freely, modify freely, build freely. Methodology synthesis content is for personal learning/research use; underlying investment views are copyright their original authors.

---

## Acknowledgments

Thanks to the following open-source authors: [@muxuuu](https://github.com/muxuuu), [@ZadAnthony](https://github.com/ZadAnthony), [@W-Y-P](https://github.com/W-Y-P), [@fadewalk](https://github.com/fadewalk), [@lanfuli](https://github.com/lanfuli), [@haskaomni](https://github.com/haskaomni), [@leslieyeo](https://github.com/leslieyeo), [@zongmin-yu](https://github.com/zongmin-yu), [@yan-labs](https://github.com/yan-labs), [@xvhaoran778-cyber](https://github.com/xvhaoran778-cyber).

And the original methodology source: **Serenity (@aleabitoreddit)** — AI & semiconductor supply chain analyst on X/Twitter.

---

*Last updated: June 10, 2026*
