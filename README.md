# 🫀 Cardiology Skills for Claude Code · 心血管内科 Claude Code 技能包

> A collection of bilingual (EN/ZH) clinical reference skills for cardiologists using Claude Code.
> Offline-first, no setup, guideline-based.
> 中英双语心血管内科 Claude Code 技能集 — 离线可用、零配置、指南驱动。

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Claude Code](https://img.shields.io/badge/Claude%20Code-Compatible-orange)](https://claude.ai/code)

---

## 📦 Skills Included · 包含技能

| Skill · 技能 | Slash Command | Covers · 涵盖 |
|-------------|---------------|----------------|
| 🧮 **Cardiac Scores** · 评分系统 | `/cardiac-scores` | CHA₂DS₂-VASc, HAS-BLED, GRACE, TIMI, HEART, Wells, Crusade, Killip, Framingham, SCORE2 — 14 scoring systems |
| 💊 **Anticoagulation** · 抗凝管理 | `/anticoagulation` | NOAC/DOAC dosing, warfarin INR, heparin, perioperative bridging, DAPT, bleeding reversal |
| 📖 **Cardiac Drugs** · 药物速查 | `/cardiac-drugs` | Antihypertensives, antiarrhythmics, GDMT for HF, lipid-lowering, vasopressors, SGLT2i/GLP-1RA |
| 📊 **ECG Interpretation** · 心电图 | `/ecg-help` | STEMI localization, wide QRS differential, conduction blocks, electrolyte patterns, critical values |
| 🫀 **Echo Reference** · 心脏超声 | `/echo-reference` | Chamber dimensions, valve quantification, diastolic function, pulmonary pressure, cardiomyopathies |
| 🩸 **Lipid Management** · 血脂管理 | `/lipid-management` | LDL-C targets, statin equivalents, non-statin agents, statin intolerance pathway |
| 🩻 **Interventional Cards** · 介入 | `/cardiac-intervention` | PCI indications, stent selection, CIN prevention, TAVR, MitraClip, pacemaker criteria |
| 💗 **Hypertension** · 高血压 | `/hypertension` | Diagnosis & staging, secondary HTN workup, combination therapy, resistant HTN, emergencies |
| 📝 **Templates** · 病历文书 | `/cardiac-templates` | Admission notes, discharge summaries, PCI reports, CCU notes, consent forms |

---

## 🚀 Installation · 安装

**Prerequisites / 前提**: [Claude Code](https://claude.ai/code) installed.

### Option 1: Git Clone

```bash
git clone https://github.com/YOUR_USERNAME/cardiology-claude-skills.git
cp -r cardiology-claude-skills/skills/* ~/.claude/skills/        # macOS / Linux
# or
Copy-Item -Recurse cardiology-claude-skills/skills/* $env:USERPROFILE\.claude\skills\   # Windows
```

### Option 2: Download ZIP

1. **Code → Download ZIP** from this repo
2. Extract, then copy all folders inside `skills/` to:
   - Windows: `C:\Users\<YourName>\.claude\skills\`
   - macOS/Linux: `~/.claude/skills/`
3. Restart Claude Code

### Verify · 验证

Type `/` in Claude Code — all `cardiac-*` skills should appear.

---

## 📖 Usage · 使用

Open Claude Code and describe the case in **Chinese or English** — the skills work in both languages.

```
"65M, atrial fibrillation, hypertension, diabetes, no prior stroke.
Calculate CHA₂DS₂-VASc and recommend anticoagulation."

"患者65岁男，房颤，高血压，糖尿病，无卒中史。
算一下CHA₂DS₂-VASc评分，推荐抗凝方案。"
```

Claude will output structured results with clinical recommendations.

---

## 🎯 Design · 设计理念

| Principle | Description |
|-----------|-------------|
| **Zero-code** · 零代码 | Pure Markdown — doctors can modify content themselves |
| **Offline** · 离线 | No internet required; patient data never leaves the machine |
| **Guideline-based** · 循证 | ESC / AHA / ACC / Chinese guidelines referenced |
| **Bilingual** · 双语 | All skills respond in EN or ZH based on user input |
| **Structured output** · 结构化 | Uniform format, ready for clinical documentation |

---

## ⚠️ Disclaimer · 免责声明

> **This tool is a clinical reference aid, NOT a substitute for professional medical judgment.**
> All scores and drug recommendations must be verified by a licensed healthcare professional
> against current guidelines and individual patient circumstances.
>
> **No patient data is collected, stored, or transmitted.** All computation is local.
>
> 本工具仅供医疗专业人士**参考辅助**使用，**不能替代临床判断**。
> 所有评分和用药建议需由执业医师结合患者情况最终决策。
> 数据基于公开发表指南，可能存在更新延迟。

---

## 🔄 Changelog · 更新

- **2026-05** — v1.0: Initial release with 9 bilingual skills

---

## 🤝 Contributing · 贡献

Pull requests welcome! Areas for contribution:
1. Fix errors / update outdated guidelines
2. Add new scoring systems, drugs, or subspecialties
3. Improve English translations
4. Add more cardiology domains (heart failure, arrhythmia, congenital, etc.)

---

**Maintained by cardiologists, for anyone who reads ECGs at 3 AM.**
