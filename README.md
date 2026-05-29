# 🫀 Cardiology Skills for Claude Code · 心血管内科 Claude Code 技能包

> A collection of bilingual (EN/ZH) clinical reference skills for cardiologists using Claude Code.
> Offline-first, no setup, guideline-based.
> 中英双语心血管内科 Claude Code 技能集 — 离线可用、零配置、指南驱动。

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Claude Code](https://img.shields.io/badge/Claude%20Code-Compatible-orange)](https://claude.ai/code)

---

## 📦 Skills Included · 包含技能

| Skill | Command | Description |
|-------|---------|-------------|
| 🫀 **Main Menu** | `/cardiology` | **Start here.** Interactive skill navigator, first-time user guide, and quick reference menu. Helps you find the right skill for your task. 总入口向导。 |
| 🚦 **Heart Check** | `/heart-check` | Interactive cardiac symptom triage for patients & the public. Step-by-step chest pain, palpitations, dyspnea, and syncope assessment. Outputs risk level with clear action guidance. |
| 🧮 **Cardiac Scores** | `/cardiac-scores` | Calculate 14 cardiology risk scores: CHA₂DS₂-VASc, HAS-BLED, GRACE, TIMI, HEART, Wells, Crusade, Killip, Framingham, SCORE2. Provide patient data → structured output. |
| 💊 **Anticoagulation** | `/anticoagulation` | NOAC/DOAC dosing, warfarin INR, heparin/LMWH, perioperative bridging, DAPT duration, and bleeding reversal. Input patient data → regimen. |
| 📖 **Cardiac Drugs** | `/cardiac-drugs` | Cardiovascular drug reference: antihypertensives, antiarrhythmics, HF GDMT, statins, vasopressors/inotropes, SGLT2i, GLP-1RA. Query by drug or class → dosing & cautions. |
| 📊 **ECG Interpretation** | `/ecg-help` | ECG interpretation: STEMI localization, arrhythmia differential (WCT/SVT/AF/VT), conduction blocks, electrolyte patterns, QT analysis, critical values. Describe ECG → read. |
| 🫀 **Echo Reference** | `/echo-reference` | TTE normal values (ASE/EACVI), chamber dimensions, valve grading, diastolic function, right heart/PASP, pericardial disease, cardiomyopathies, prosthetic valves. Input values → report. |
| 🩸 **Lipid Management** | `/lipid-management` | LDL-C targets by ASCVD risk, statin intensity equivalents, non-statin agents (ezetimibe, PCSK9i, inclisiran, bempedoic acid), statin intolerance pathway, and monitoring protocols. |
| 🩻 **Interventional** | `/cardiac-intervention` | PCI indications, stent selection, DAPT duration, CIN prevention, PCI complications, structural interventions (TAVR, MitraClip, LAAO, PFO), and pacemaker/CRT/ICD indications. |
| 💗 **Hypertension** | `/hypertension` | Diagnosis & staging, BP measurement (office/home/ABPM), secondary HTN workup, pharmacotherapy (monotherapy to resistant HTN), special populations, hypertensive emergencies with IV drug guide. |
| 📝 **Templates** | `/cardiac-templates` | Admission notes, discharge summaries, procedure reports (PCI, pacemaker, TAVR), CCU progress notes, death summaries, consultation requests, and informed consent forms. |

---

## 🚀 Installation · 安装

**Prerequisites / 前提**: [Claude Code](https://claude.ai/code) installed.

### Option 1: Git Clone

```bash
git clone https://github.com/mmmactavish/cardiology-claude-skills.git
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
