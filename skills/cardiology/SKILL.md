---
name: cardiology
description: >
  Master entry point for all cardiology Claude Code skills. First-time user guide,
  interactive skill navigator, and quick reference menu. Start here if you're new.
  心血管技能包总入口。首次使用向导、交互式导航、快速参考菜单。新用户从这里开始。
triggers:
  - cardio: cardiology/cardio/cardiac/heart/心内科/心血管/心脏
  - help: help/guide/menu/start/overview/welcome/帮助/向导/菜单/导航/入门/开始/概述/使用帮助
  - what-can-you-do: what can you do/what skills do you have/available skills/能做什么/有哪些功能/怎么用/有什么技能
  - cardiology-skills: cardiology skills/cardiac skills/heart skills/all skills/技能列表
metadata:
  author: Cardiology Claude Skills
  version: "1.0"
  languages: [en, zh]
---

# 🫀 Cardiology Skills — Main Menu · 心血管技能包总入口

Welcome! This is the master guide to all 10 cardiology skills.
欢迎！以下是全部 10 个心血管技能的入口导航。

---

## 🚀 Quick Start · 快速开始

**If this is your first time:** Just describe your situation below, and I'll guide you to the right skill.
**首次使用：** 直接描述你的需求，我会引导你到对应技能。

Examples · 示例：
- *"我想算一下房颤患者的卒中风险"* → `/cardiac-scores`
- *"帮我看看这个心电图"* → `/ecg-help`
- *"我胸口有点闷，要不要去医院"* → `/heart-check`
- *"PCI 术后 DAPT 用多久"* → `/anticoagulation`
- *"帮我写一份心梗入院记录"* → `/cardiac-templates`

---

## 📋 All Skills · 全部技能

| # | Command | Best for... · 适用场景 |
|---|---------|----------------------|
| 🚦 | `/heart-check` | **Patients & public**: chest pain, palpitations, dyspnea self-triage. 胸痛心悸气短自查分流。 |
| 🧮 | `/cardiac-scores` | **Risk calculation**: CHA₂DS₂-VASc, HAS-BLED, GRACE, TIMI, HEART, Wells, etc. 14种评分。 |
| 💊 | `/anticoagulation` | **Anticoagulation**: NOAC dosing, warfarin INR, heparin, bridging, DAPT, bleeding reversal. 抗凝用药。 |
| 📖 | `/cardiac-drugs` | **Drug reference**: antihypertensives, antiarrhythmics, HF GDMT, statins, pressors, SGLT2i. 药物速查。 |
| 📊 | `/ecg-help` | **ECG interpretation**: STEMI localization, arrhythmia differential, blocks, electrolytes. 心电图判读。 |
| 🫀 | `/echo-reference` | **Echocardiography**: normal values, valve grading, diastolic function, PASP. 心脏超声参考。 |
| 🩸 | `/lipid-management` | **Lipid management**: LDL-C targets, statin equivalents, non-statin agents. 血脂管理。 |
| 🩻 | `/cardiac-intervention` | **Intervention**: PCI, stent selection, TAVR, MitraClip, pacemaker, CIN prevention. 介入诊疗。 |
| 💗 | `/hypertension` | **Hypertension**: staging, secondary workup, combination therapy, emergencies. 高血压管理。 |
| 📝 | `/cardiac-templates` | **Documentation**: admission notes, discharge summaries, PCI reports, consent forms. 病历模板。 |

---

## 🎯 Find the Right Skill · 找技能

Tell me what you need, and I'll route you:

| I want to... · 我想... | Use this · 用这个 |
|------------------------|-------------------|
| Check if my symptoms need ER · 自查要不要去急诊 | `/heart-check` |
| Calculate a risk score · 算一个临床评分 | `/cardiac-scores` |
| Look up a drug dose · 查药物剂量 | `/cardiac-drugs` |
| Manage anticoagulation · 管理抗凝方案 | `/anticoagulation` |
| Read an ECG · 判读心电图 | `/ecg-help` |
| Interpret echo values · 解读心脏超声数值 | `/echo-reference` |
| Adjust lipid-lowering therapy · 调降脂方案 | `/lipid-management` |
| Plan PCI or check indications · PCI决策/适应证 | `/cardiac-intervention` |
| Manage hypertension · 管理高血压 | `/hypertension` |
| Generate clinical documentation · 生成病历文书 | `/cardiac-templates` |

---

## 💡 Tips · 使用技巧

- **Skills work in both English and Chinese.** Just speak naturally. 中英文都能触发。
- **Combine skills.** Say *"calculate GRACE score AND recommend DAPT"* — both skills activate. 可以同时用多个技能。
- **Update the skills yourself.** All files are plain Markdown in `~/.claude/skills/`. Edit anytime. 所有技能均为纯文本 Markdown，医生可自行修改更新。
- **Offline.** No internet needed. Patient data stays on your machine. 离线运行，数据不出电脑。

---

*Not sure where to start? Just tell me what you're working on.*
*不知道从哪里开始？告诉我你在做什么，我帮你选。*
