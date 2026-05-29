---
name: heart-check
description: >
  Rapid cardiac symptom triage for the general public. Step-by-step interactive assessment
  of chest pain, palpitations, dyspnea, syncope, and other cardiac warning signs.
  Outputs risk level with clear action guidance: emergency, urgent care, or home observation
  with safety instructions. Based on standard cardiac triage protocols.
triggers:
  - chest-pain: chest pain/heart pain/chest discomfort/chest tightness/胸痛/胸口痛/心口痛/胸闷/心脏疼
  - palpitations: palpitations/heart racing/heart pounding/irregular heartbeat/skipped beats/心悸/心跳快/心跳乱/心慌
  - dyspnea: shortness of breath/can't breathe/breathless/difficulty breathing/呼吸困难/喘不上气/气短/憋气
  - syncope: fainting/passed out/blackout/near-fainting/dizziness/晕倒/晕厥/眼前发黑/头晕/差点晕倒
  - heart-check: heart check/cardiac check/heart symptom assess/heart self-check/heart triage/心脏自查/心脏评估/心脏筛查/心脏分流
  - heart-symptoms: heart symptoms/ cardiac symptoms/心脏症状/心脏不舒服/心脏难受
metadata:
  author: Cardiology Claude Skills
  version: "1.0"
  languages: [en, zh]
---

# Rapid Cardiac Triage · 心脏快速评估分流

## ⚠️ Read This First · 请先阅读

> **This tool is for informational triage only. It does NOT diagnose or replace professional medical evaluation.**
> **When in doubt, always err on the side of seeking medical care.**
> **If symptoms are severe or you feel something is seriously wrong, call emergency services immediately.**

> 此工具仅供信息筛查参考，不构成诊断，不能替代专业医疗评估。
> 如有疑虑，请务必就医。症状严重或自觉情况危急时请立即拨打急救电话。

---

## Triage Protocol · 评估流程

The assessment follows 4 sequential phases. **Ask ONE phase at a time. Do not jump ahead.**
逐步评估，每次只问一个阶段的问题。

---

### Phase 0: Emergency Red Flags — STOP AND CALL EMERGENCY NOW
### 阶段0：危急信号 —— 立即停止，呼叫急救

**Ask these questions first. If ANY answer is YES → instruct the user to call emergency services immediately (120/911).**

按顺序询问以下问题。**任何一项回答"是" → 立即告知呼叫急救 (120/911)**。

| # | Question · 问题 | Why This Matters |
|---|-----------------|-----------------|
| 1 | Are you experiencing **crushing/squeezing chest pain** lasting >15 minutes, not relieved by rest? 是否正感到**压榨性胸痛**持续超过15分钟且休息不缓解？ | Possible acute MI · 可能急性心梗 |
| 2 | Is the chest pain **radiating to your jaw, left shoulder/arm, or back**? 胸痛是否**放射到下颌、左肩/左臂或背部**？ | Classic ACS presentation · 典型ACS表现 |
| 3 | Are you **struggling to breathe** at rest, or can you only breathe comfortably sitting upright? 静息下是否**呼吸困难**，需要坐起来才能呼吸？ | Possible acute heart failure · 可能急性心衰 |
| 4 | Did you **lose consciousness (faint/pass out)**? 你是否**晕倒/失去意识**了？ | Possible arrhythmia/arrest · 可能心律失常/猝死风险 |
| 5 | Are you having **severe palpitations with dizziness, chest pain, or near-fainting**? 是否**心慌/心悸同时伴有头晕、胸痛或濒死感**？ | Possible VT/SVT with instability · 可能不稳定心律失常 |
| 6 | Are you **coughing up pink frothy sputum**? 是否在**咳粉红色泡沫痰**？ | Acute pulmonary edema · 急性肺水肿（心衰） |
| 7 | Is your heart rate **extremely fast (>150 bpm at rest) or extremely slow (<40 bpm with symptoms)**? 静息心率是否**极快（>150次/分）或极慢（<40次/分并伴有不适）**？ | Hemodynamic compromise · 血流动力学不稳定 |

**If ANY "YES" above:**
```
🚨 DO NOT DELAY. CALL 120/911 NOW.

While waiting for help:
• Stop all activity. Sit or lie down.
• If you have aspirin at home and are NOT allergic, chew 300mg (unless contraindicated).
• If you have nitroglycerin prescribed, take as directed.
• Unlock your door so paramedics can enter.
• Do NOT drive yourself to the hospital.
• Do NOT eat or drink anything.
• Stay on the phone with emergency services.

🚨 不要拖延，立即拨打120/911。

等待救援期间：
• 停止一切活动，坐下或半卧。
• 如家中有阿司匹林且不过敏，嚼服300mg（除非有禁忌）。
• 如有医生处方的硝酸甘油，按医嘱服用。
• 打开房门以便急救人员进入。
• 不要自行驾车去医院。
• 不要进食或饮水。
• 与急救调度保持通话。
```

**Only proceed to Phase 1 if ALL Phase 0 answers are NO.**
**只有当阶段0所有问题回答"否"，才继续阶段1。**

---

### Phase 1: Identify the Primary Symptom
### 阶段1：确定主要症状

Ask the user: "Which of the following best describes what you're feeling right now?"
询问用户："以下哪项最能描述你现在的感受？"

| Option | Primary Symptom |
|--------|----------------|
| A | **Chest pain / pressure / tightness / discomfort** · 胸痛/胸闷/压迫感/不适 |
| B | **Palpitations / heart racing / heart skipping / irregular beat** · 心悸/心慌/心跳乱/漏跳 |
| C | **Shortness of breath / difficulty breathing** · 气短/呼吸困难 |
| D | **Dizziness / lightheadedness / near-fainting** · 头晕/眼前发黑/差点晕倒 |
| E | **Swelling in legs/ankles + fatigue** · 下肢水肿+乏力 |
| F | **Other / multiple symptoms** · 其他/多种症状 |

Based on the choice, go to the corresponding detailed assessment section.

---

### Phase 2: Detailed Assessment (by symptom)
### 阶段2：详细评估（按症状分类）

#### PATH A: Chest Pain · 胸痛评估

Ask each question. Tally the risk points.

**Part 1: Pain Characteristics · 疼痛特征**

| Question | Low Risk (0) | Medium Risk (+1) | High Risk (+2) |
|----------|-------------|------------------|----------------|
| Quality · 性质 | Sharp/stabbing (针扎/刀刺样) | Burning/pressure (烧灼/压迫感) | Squeezing/crushing/heaviness (压榨/沉重感) |
| Location · 位置 | Pinpoint, one finger can cover (针尖大小,单指可覆盖) | Diffuse left chest (弥漫性左侧) | Central chest/retrosternal (胸骨后正中) |
| Radiation · 放射 | No radiation (无放射) | Neck/throat only (仅颈部) | Jaw/shoulder/left arm/back (下颌/左肩/左臂/背部) |
| Duration · 持续 | Seconds, fleeting (<30s) (几秒即过) | Minutes, variable (数分钟,反复) | >15 min, constant (持续超过15分钟) |
| Trigger · 诱发 | Only with movement/touch (仅活动或触摸时) | With exertion (劳累时) | At rest / wakes from sleep (静息/夜间痛醒) |
| Relief · 缓解 | Immediate with position change (改变姿势立即缓解) | With rest in <5 min (休息5分钟内缓解) | Not relieved by rest or nitroglycerin (休息或硝酸甘油无效) |

**Part 2: Associated Symptoms · 伴随症状** (each +1 if present · 每项+1分)

| Symptom | Check |
|---------|-------|
| Nausea / vomiting · 恶心/呕吐 | ☐ |
| Cold sweat / diaphoresis · 出冷汗 | ☐ |
| Shortness of breath · 呼吸困难 | ☐ |
| Palpitations · 心悸/心慌 | ☐ |
| Dizziness / near-fainting · 头晕/濒死感 | ☐ |
| Extreme fatigue (unusual) · 异常极度疲劳 | ☐ |

**Part 3: Risk Factors · 危险因素** (each +1 if present · 每项+1分)

| Risk Factor | Check |
|-------------|-------|
| Age ≥55 (male) or ≥65 (female) · 男≥55或女≥65 | ☐ |
| Known coronary artery disease / prior MI / stent · 已知冠心病/心梗/支架 | ☐ |
| Hypertension · 高血压 | ☐ |
| Diabetes · 糖尿病 | ☐ |
| Current smoker or quit <1 year · 目前吸烟/戒烟不足1年 | ☐ |
| High cholesterol / on statin · 高血脂/服用他汀 | ☐ |
| Family history of early MI (♂<55, ♀<65) · 早发心梗家族史 | ☐ |
| Known peripheral or cerebrovascular disease · 外周/脑血管病 | ☐ |

**Chest Pain Risk Score:**

| Total Score | Risk Level | Action |
|------------|------------|--------|
| 0-3 | LOW · 低风险 | See Observation Plan · 见观察方案 |
| 4-7 | MODERATE · 中风险 | See Urgent Care Plan · 见尽快就医方案 |
| ≥8 | HIGH · 高风险 | See Emergency Plan · 见急诊方案 |

---

#### PATH B: Palpitations · 心悸评估

| Question | Low Risk (0) | Higher Risk (+1) |
|----------|-------------|------------------|
| Onset · 发作 | Gradual, over minutes (逐渐开始) | Sudden, like flipping a switch (突然发作) |
| Pattern · 节律 | Regular, steady fast beat (规律快速) | Irregular, chaotic, "flip-flop" (杂乱无章) |
| Rate · 心率 (if known) | 60-120 bpm | >120 bpm or <50 bpm |
| Duration · 持续 | <5 minutes | >30 minutes or ongoing |
| Associated · 伴随 | None (无不适) | Chest pain / dyspnea / dizziness / near-fainting / cold sweat (胸痛/气短/头晕/冷汗) |
| History · 病史 | First episode, otherwise healthy (首次发作,平素健康) | Known AF/SVT/VT / structural heart disease / prior ablation (已知房颤/室上速/室速/器质性心脏病/消融史) |

**Palpitations Risk Score:**

| Total Score | Risk Level | Action |
|------------|------------|--------|
| 0-1 | LOW · 低风险 | See Observation Plan · 见观察方案 |
| 2-3 | MODERATE · 中风险 | See Urgent Care Plan · 见尽快就医方案 |
| ≥4 or ANY syncope | HIGH · 高风险 | See Emergency Plan · 见急诊方案 |

---

#### PATH C: Shortness of Breath · 呼吸困难评估

| Question | Low Risk (0) | Higher Risk (+1) |
|----------|-------------|------------------|
| Onset · 起病 | Chronic, stable (慢性,稳定) | Acute onset or worsening (<1 week) (急性/近期加重) |
| At rest? · 静息时? | No, only with significant exertion (仅大量活动时) | Yes, even at rest or lying flat (静息/平卧时即出现) |
| Orthopnea · 端坐呼吸 | Can lie flat comfortably (可平卧) | Need pillows / sit up to breathe (需垫高枕头/坐起才能呼吸) |
| PND · 阵发性夜间 | No (无) | Wake up at night gasping (夜间憋醒,需坐起) |
| Edema · 水肿 | No leg swelling (无) | Legs/ankles swelling, weight gain (下肢水肿,体重增加) |
| Sputum · 痰 | Dry cough (干咳) | Pink frothy sputum → **IMMEDIATE ER** (粉红泡沫痰→急诊) |
| Chest pain · 胸痛 | No (无) | With chest pain → reassess with PATH A (有胸痛→转A评估) |

**Dyspnea Risk Score:**

| Total Score | Risk Level | Action |
|------------|------------|--------|
| 0-1 | LOW · 低风险 | See Observation Plan · 见观察方案 |
| 2-3 | MODERATE · 中风险 | See Urgent Care Plan · 见尽快就医方案 |
| ≥4 or pink sputum or onset <2h | HIGH · 高风险 | See Emergency Plan · 见急诊方案 |

---

#### PATH D: Dizziness / Near-Fainting · 头晕/近晕厥

| Question | Low Risk (0) | Higher Risk (+1) |
|----------|-------------|------------------|
| True syncope? · 真正晕厥? | No, just dizziness (无,仅头晕) | Yes, lost consciousness (是,失去意识) → **≥1 episode → HIGH RISK** |
| Relation to posture · 与体位关系 | Gradual, when standing up slowly (缓缓站起时) | Sudden, with no warning (毫无预兆突然发生) |
| Palpitations before? · 发作前心悸? | No (无) | Yes, heart racing/pounding before (有心悸/心慌先兆) |
| During exertion? · 运动中发生? | No (否) | Yes, during or right after exercise (运动中/刚结束后) |
| Recovery · 恢复 | Immediate, fully alert (立即清醒) | Confused after, slow recovery (事后迷糊/恢复慢) |
| Injury? · 受伤? | No (无) | Yes, fell and hurt self (摔倒受伤) |
| Known heart disease? | No (无) | Known LV dysfunction / HCM / AS / arrhythmia (已知左室功能障碍/肥厚心/主动脉瓣狭窄/心律失常) |

**Dizziness Score:**

| Total Score | Risk Level | Action |
|------------|------------|--------|
| 0-1 | LOW · 低风险 | See Observation Plan · 见观察方案 |
| 2-3 | MODERATE · 中风险 | See Urgent Care Plan · 见尽快就医方案 |
| ≥4 or true syncope | HIGH · 高风险 | See Emergency Plan · 见急诊方案 |

---

#### PATH E: Leg Swelling + Fatigue · 下肢水肿+乏力

| Question | Low Risk (0) | Higher Risk (+1) |
|----------|-------------|------------------|
| Extent · 范围 | Ankles only (仅脚踝) | Up to shins/knees or above (小腿/膝盖以上) |
| Symmetry · 对称性 | Unilateral → **consider DVT** (单侧→需排查DVT) | Bilateral (双侧) |
| Pitting · 凹陷性 | No (否) | Yes, dent stays after pressing (按压后有凹陷) |
| Orthopnea/PND | No (无) | Yes (有) → assess with PATH C |
| Weight gain · 体重增加 | No (无) | Yes, rapid weight gain >2kg/week (体重迅速增加) |
| Known HF? · 已知心衰? | No (无) | Yes (是) → **HIGH RISK if worsening** |

---

#### PATH F: Multiple / Other Symptoms · 多种症状

If the user reports multiple symptoms, prioritize in this order:
1. Syncope / near-syncope → use PATH D
2. Chest pain → use PATH A
3. Severe dyspnea → use PATH C
4. Palpitations → use PATH B

---

### Phase 3: Risk Output & Action Plan
### 阶段3：风险判定与行动方案

---

#### 🟢 LOW RISK · 低风险 — Observation Plan · 观察方案

```
Based on your responses, your symptoms appear to be LOW RISK for a cardiac emergency.
This does NOT rule out a heart problem, but there is no indication for immediate emergency care.

✅ WHAT TO DO · 你可以这样做：
  • Monitor your symptoms. If they worsen, seek medical evaluation.
    观察症状变化，如加重则就医。
  • Schedule a non-urgent doctor visit (within 1-2 weeks) for a baseline evaluation:
    — ECG, blood pressure check, basic bloodwork (lipids, glucose).
    预约门诊做基础检查：心电图、血压、血脂、血糖。
  • Keep a symptom diary: when does it happen, what triggers it, how long it lasts.
    记录症状日记：何时发作、诱因、持续时间。
  • If you have a home BP monitor, check your BP twice daily.
    如家中有血压计，早晚测血压。

❌ WHAT TO AVOID · 避免以下行为：
  • Do NOT ignore symptoms that worsen or change character.
    不要忽视加重或性质改变的症状。
  • Do NOT start intense exercise until evaluated.
    未评估前不要开始剧烈运动。
  • Do NOT use stimulants (energy drinks, excessive caffeine, recreational drugs).
    避免兴奋性物质（能量饮料、过量咖啡因、违禁药物）。
  • Do NOT self-medicate with unknown supplements or herbal remedies for "heart health."
    不要自行服用未经证实的"护心"保健品。

🔄 RETURN TO ASSESSMENT IF · 如出现以下情况请重新评估：
  • Pain becomes squeezing/crushing
  • Pain lasts >15 min
  • You faint or near-faint
  • You develop shortness of breath at rest
  • Heart rate becomes very fast (>120) or very slow (<45) with symptoms
```

---

#### 🟡 MODERATE RISK · 中风险 — Urgent Care Plan · 尽快就医方案

```
Based on your responses, your symptoms are MODERATE RISK.
You should seek medical evaluation soon (today or tomorrow, NOT emergent but don't delay).

✅ WHAT TO DO · 你应该：
  • Visit an urgent care center, cardiology clinic, or hospital outpatient department TODAY.
    今天到急诊科/心内科门诊就诊。
  • Get a 12-lead ECG and, if indicated, cardiac enzyme tests (troponin).
    做12导联心电图，必要时查心肌酶（肌钙蛋白）。
  • If palpitations: request a 24h Holter monitor if episodes are daily, or an event recorder.
    如为心悸：要求动态心电图（Holter）或事件记录器。
  • If chest pain: consider exercise stress test or coronary CTA per physician assessment.
    如为胸痛：根据医生评估考虑运动负荷试验或冠脉CTA。
  • Bring a list of all medications you take.
    携带所有正在服用的药物清单。

❌ WHAT TO AVOID · 绝对避免：
  • Do NOT wait >48 hours to seek care.
    不要等待超过48小时才就医。
  • Do NOT do strenuous exercise or heavy lifting.
    不要进行剧烈运动或重体力劳动。
  • Do NOT take aspirin preventively without discussing with a doctor first.
    未经医生指导不要自行服用阿司匹林预防。
  • Do NOT drive yourself if you feel dizzy or unwell — ask someone to take you.
    如感头晕/不适,不要自己开车,请他人陪同。

🔴 RE-EVALUATE IMMEDIATELY if symptoms become constant, severe, or you faint.
如症状变为持续性/加重/出现晕厥，立即重新评估。
```

---

#### 🔴 HIGH RISK · 高风险 — Emergency Plan · 急诊方案

```
⚠️ DO NOT WAIT. GO TO THE EMERGENCY DEPARTMENT NOW. ⚠️

Your responses indicate HIGH RISK for a potentially serious cardiac condition.
You need immediate medical evaluation.

✅ IMMEDIATE ACTIONS · 立即行动：
  1. Call 120/911 or have someone drive you to the nearest ER immediately.
     拨打120/911或让他人立即送你去最近的急诊科。
  2. Stop all activity. Sit or lie down in a comfortable position.
     停止一切活动。坐下或半卧位。
  3. Tell the ER triage nurse: "I have [chest pain/palpitations/dyspnea/syncope] with HIGH-RISK features."
     到急诊后告诉分诊护士你属于高危症状（胸痛/心悸/呼吸困难/晕厥+高危特征）。

📋 BRING WITH YOU:
  • List of current medications
  • Any previous ECG or cardiac test results
  • ID and insurance card
  • Phone charger

❌ DO NOT:
  • Drive yourself if you have chest pain or feel faint.
  • Eat or drink anything (may need procedures).
  • Take any new medication without telling the ER doctor.
  • Delay hoping symptoms will go away.

⚠️ 不要拖延就医。你的症状存在需紧急评估的心脏风险。
```

---

## Output Format · 输出格式

After completing all phases, present the result in this format:

```
╔══════════════════════════════════════╗
║  🫀 HEART CHECK RESULT · 心脏评估结果 ║
╠══════════════════════════════════════╣
║  Symptom Path:  [A/B/C/D/E/F]       ║
║  Risk Score:    X points            ║
║  Risk Level:    🟢 LOW / 🟡 MODERATE / 🔴 HIGH ║
╠══════════════════════════════════════╣
║  [Action plan — output the relevant ║
║   plan from Phase 3 above]          ║
╚══════════════════════════════════════╝

🩺 This is a triage tool, not a diagnosis.
   Please consult a healthcare professional for definitive evaluation.
   此为分流评估工具,非诊断。请务必咨询医生获得确切评估。
```

---

## Important Notes for the AI · AI 评估注意事项

1. **Always start from Phase 0.** Never skip the emergency red flags.
   必须从阶段0开始，不可跳过危急信号筛查。

2. **One question at a time.** Ask 3-4 questions per round, then wait for the user to respond.
   每次问3-4个问题，等待用户回答后再继续。

3. **When in doubt, escalate.** If you are uncertain about the risk level, always choose the higher tier.
   不确定时，永远选择更高的风险等级。

4. **Re-evaluate.** If the user reports changing or worsening symptoms, restart from Phase 0.
   如用户报告症状变化或加重，从阶段0重新开始。

5. **Language.** Respond in the language the user uses. Default to Chinese for Chinese-speaking users.
   用用户使用的语言回应。中国用户默认使用中文。

6. **Tone.** Be calm, professional, but convey appropriate urgency for high-risk findings.
   保持冷静专业，但对高风险发现传递适当的紧迫感。
