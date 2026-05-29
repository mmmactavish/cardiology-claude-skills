---
name: cardiac-intervention
description: >
  Interventional cardiology: PCI indications, stent selection, DAPT duration,
  CIN prevention, PCI complications, structural interventions (TAVR, MitraClip, LAAO, PFO),
  and pacemaker/CRT/ICD indications. Perioperative management included.
triggers:
  - PCI: PCI/coronary angiography/angioplasty/stent/revascularization/介入/冠脉造影/冠脉支架/血运重建
  - stent: stent/DES/BMS/drug-eluting stent/bioresorbable scaffold/支架/药物洗脱支架
  - CTO: CTO/chronic total occlusion/慢性闭塞
  - complication: PCI complication/stent thrombosis/in-stent restenosis/coronary perforation/no-reflow/支架内血栓/支架内再狭窄/冠脉穿孔/无复流
  - contrast: contrast nephropathy/CIN/PC-AKI/contrast-induced/对比剂肾病/造影剂/水化
  - TAVR: TAVR/TAVI/transcatheter aortic valve/经导管主动脉瓣置换
  - mitral: MitraClip/TEER/transcatheter mitral repair/二尖瓣钳夹/经导管二尖瓣修复
  - LAAO: LAAO/Watchman/left atrial appendage occlusion/左心耳封堵
  - PFO: PFO/ASD closure/卵圆孔封堵/房间隔缺损
  - pacemaker: pacemaker/CRT/ICD/CRTD/cardiac implantable device/起搏器适应证
  - preprocedural: preprocedural/periprocedural/hold anticoagulation/术前停药/围术期管理
metadata:
  author: Cardiology Claude Skills
  version: "1.0"
  languages: [en, zh]
---

# 心血管介入诊疗助手

覆盖冠脉介入、结构性心脏病介入、起搏器、围术期管理。

---

## 一、冠脉造影与 PCI 适应证

### 1.1 稳定型心绞痛 / CCS

| 临床情况 | 推荐等级 |
|---------|---------|
| 优化药物仍有症状 | I A（PCI 改善症状） |
| 左主干病变 | I A（PCI 或 CABG，SYNTAX 评分决定） |
| LAD 近段单支 | I A（PCI 改善预后） |
| 多支病变 + DM + SYNTAX≥33 | I A → CABG 优于 PCI |
| 大面积缺血（>10% LV） | I B（血运重建改善预后） |
| 无症状 / 轻度症状 / 无缺血证据 | III（不推荐） |

### 1.2 ACS（NSTEMI/UA）

| 策略 | 适用人群 |
|------|---------|
| **早期介入（24h内）** | GRACE >140、肌钙蛋白升高、ST段动态变化、GRACE 109-140 + 至少1项高危 |
| **紧急介入（2h内）** | 血流动力学不稳定、心源性休克、顽固性心绞痛、恶性心律失常、机械性并发症 |
| **择期介入** | 低危（GRACE ≤108）、无上述高危特征 |

### 1.3 STEMI

- **直接 PCI**：Door-to-balloon <90 min（就诊→球囊）
- **溶栓后 PCI**（药物-介入策略）：溶栓后 3-24h 常规冠脉造影
- **溶栓失败**：立即补救 PCI

---

## 二、支架选择

### 2.1 支架类型对比

| 特性 | DES（药物洗脱支架） | BMS（裸金属支架） | BRS（生物可吸收） |
|------|-------------------|-------------------|-------------------|
| 支架内再狭窄率 | 5-10% | 20-30% | 类似 DES |
| 支架血栓风险 | 0.5-1%/年 | 1-1.5%/年 | 略高（早期） |
| DAPT 时长 | 1-6月（新一代） | 1月 | 更长 |
| 适应证 | 绝大多数 | 高出血风险/需限期手术 | 年轻/大血管/患者意愿 |

### 2.2 选择原则

```
默认：新一代 DES（XIENCE/Resolute/Onyx/Orsiro/Synergy 等）
  — 绝大多数患者

高出血风险/近期需大手术：
  → DES + 缩短 DAPT（1-3月后转单抗）
  → 或 BMS（极少用了）

年轻 + 大血管 >3.0mm：
  → 可考虑 BRS（Absorb/Magmaris）

左主干/分叉：
  → 优选薄梁 DES（Orsiro/Xience等）
  → Provisional 单支架策略（首选）

钙化病变：
  → 旋磨/冲击波球囊（IVL）+ DES
```

### 2.3 IVUS/OCT 指导（IIa A 推荐）

**推荐使用**：左主干、长病变、分叉、CTO、支架内再狭窄、肾功能不全不能多造影

- IVUS：最小管腔面积 MLA <4.0mm²（LM）/ <2.4mm²（非LM）→ 有意义狭窄
- OCT：更高分辨率，评估钙化厚度、支架贴壁、内膜覆盖

---

## 三、DAPT 方案（PCI 后）

### 3.1 DAPT 时长决策流程

```
ACS PCI：
  → 阿司匹林 + 替格瑞洛（首选）/ 普拉格雷
  → DAPT 12月（标准）
  → 高出血风险（PRECISE-DAPT ≥25）→ 1-3月后单抗

CCS PCI：
  → 阿司匹林 + 氯吡格雷
  → DAPT 1-3月（新一代DES）/ 6月
  → 高缺血风险（复杂PCI）+ 低出血风险 → DAPT 延长>12月

PCI + 房颤（需抗凝）：
  → NOAC + 单抗（氯吡格雷）→ 1周-1月后→单用NOAC
  → 不推荐三联（NOAC + DAPT >1周）
```

### 3.2 缩短 DAPT 的方案（高出血风险）

| 时间 | 方案 |
|------|------|
| PCI 后 0-1月 | 阿司匹林 + 替格瑞洛 |
| 1月后 | 替格瑞洛 单抗（TWILIGHT方案）/ 阿司匹林单抗 |
| 或 | 阿司匹林 + P2Y12 → 1-3月后 → 单用P2Y12（GLOBAL LEADERS方案） |

---

## 四、对比剂肾病（CIN / PC-AKI）预防

### 4.1 风险分层

| 危险因素 | 分值 |
|----------|------|
| 低血压 | 5 |
| IABP | 5 |
| CHF（NYHA III-IV） | 5 |
| 年龄 >75 岁 | 4 |
| 贫血（Hct 男<39/女<36） | 3 |
| DM | 3 |
| 对比剂用量（每100mL） | 1 |
| 术前 Cr >1.5 mg/dL | 4 |
| eGFR <60→每降10 | 加权 |

**Mehran 评分风险**：≤5低(7.5%) / 6-10中(14%) / 11-16高(26%) / >16极高(57%)

### 4.2 预防方案

| 措施 | 详情 |
|------|------|
| **水化（最重要！）** | 等渗盐水 1mL/kg/h 术前 12h→术后 24h（EF低者减量） |
| **紧急 PCI 水化** | 等渗盐水 3mL/kg 术前1h bolus → 1mL/kg/h 术后6h |
| **对比剂选择** | 等渗/低渗，非离子型（碘克沙醇/碘佛醇/碘海醇） |
| **限量** | 最大用量 ≤ 3.7×eGFR（或 5mL/kg ÷ Cr） |
| **停药** | 术前 24-48h 停用二甲双胍、NSAIDs、利尿剂（酌减） |
| **NAC（乙酰半胱氨酸）** | 证据不足，已不常规推荐 |

### 4.3 eGFR <30 mL/min 或 极高危患者

- 等渗盐水充分水化
- 最小化对比剂用量
- 考虑 IVUS/OCT 辅助（减少造影次数）
- 术后 48-72h 监测 Cr

---

## 五、PCI 并发症处理

### 5.1 支架内血栓

| 时间 | 定义 |
|------|------|
| 急性 | PCI 后 <24h |
| 亚急性 | 24h-30天 |
| 晚期 | 30天-1年 |
| 极晚期 | >1年 |

**处理**：急诊造影 + 再次 PCI（考虑 IVUS/OCT 明确原因：贴壁不良/膨胀不全/边缘夹层）

### 5.2 无复流/慢血流

| 处理步骤 | 详情 |
|---------|------|
| 排除机械性 | 夹层/血栓/痉挛（造影确认） |
| 药物 | 腺苷 100-300μg IC / 硝普钠 100-200μg IC / 维拉帕米 100-200μg IC / 尼可地尔 2mg IC |
| 预防 | 旋磨/静脉桥血管 PCI 前预给药 |

### 5.3 冠脉穿孔（Ellis 分级）

| 分级 | 表现 | 处理 |
|------|------|------|
| I | 造影剂局部弹坑 | 鱼精蛋白 + 观察 |
| II | 心肌或心包少量染色 | 球囊低压封堵 + 鱼精蛋白 |
| III | 造影剂喷射穿出 | 球囊封堵 + 心包穿刺引流 + 覆膜支架/弹簧圈/外科 |

### 5.4 支架内再狭窄（ISR）

| 类型 | 治疗选择 |
|------|---------|
| 局灶性 ISR | 药物球囊（DCB）→ 首选 / DES 再植入 |
| 弥漫性 ISR | DCB / DES（与原有不同药物涂层） |
| 反复 ISR | 血管内放射治疗（VBT） / CABG |

---

## 六、结构性心脏病介入

### 6.1 TAVR/TAVI 适应证速查

| 外科风险 | AS 严重度 | 推荐 |
|----------|----------|------|
| 极高/禁忌（STS>8%或虚弱） | 重度 | TAVR → I |
| 高危（STS>4-8%） | 重度 | TAVR 或 SAVR → 心脏团队讨论 |
| 中危（STS>3-4%） | 重度 | TAVR = SAVR（I类），年轻选SAVR |
| 低危（STS<3%） | 重度 | SAVR 或 TAVR，<65岁偏SAVR，>80偏TAVR |

**术前评估**：CT主动脉根部（瓣环大小+冠脉开口高度+入路）、冠脉造影、超声、虚弱评估

### 6.2 MitraClip / TEER（经导管二尖瓣缘对缘修复术）

| 情况 | 推荐 |
|------|------|
| 原发性重度 MR + 外科高危 | I → MitraClip |
| 继发性重度 MR（FMR）+ GDMT 优化后仍有症状 + COAPT标准 | IIa → MitraClip |
| **COAPT 入选标准**：FMR EROA≥0.30 + LVEF 20-50% + LVESD≤70mm + GDMT≥3月 |

### 6.3 左心耳封堵（LAAO）

**适应证**：非瓣膜性房颤 + CHA₂DS₂-VASc ≥2 (男) / ≥3 (女) + 抗凝禁忌/高出血风险

| 装置 | 说明 |
|------|------|
| Watchman™ FLX | 最常用 |
| Amplatzer™ Amulet | 双盘结构 |

**术后抗栓**：Watchman → 抗凝 45天→DAPT→单抗 / 高出血替代方案→DAPT

### 6.4 PFO 封堵

**适应证**：
- 年龄 <60 岁 PFO + 原因不明卒中（CS）+ PFO 为中-大分流 / 房间隔瘤
- 排除其他卒中原因后 → PFO 封堵（I A，RoPE>6分）

---

## 七、起搏器 / CRT / ICD 适应证

### 7.1 永久起搏器

| 适应证 | 推荐等级 |
|--------|---------|
| 症状性 SSS（病态窦房结综合征） | I |
| 二度II型 / 高度 / 三度 AVB | I |
| 双束支阻滞 + 不明原因晕厥 | IIa |
| 交替性束支传导阻滞 | I |
| TAVR 术后高度 AVB | I |
| 神经介导性晕厥 + 心脏抑制型（>3秒停搏） | IIa |

### 7.2 CRT（心脏再同步化治疗）

**适应证**（窦性心律）：
- LBBB + QRS ≥150ms + LVEF≤35%
- LBBB + QRS 130-149ms + LVEF≤35%（IIa）
- non-LBBB + QRS ≥150ms + LVEF≤35%（IIa）
- non-LBBB + QRS 130-149ms + LVEF≤35%（IIb）

**CRT-D vs CRT-P**：预期生存>1年 + 状态好 → CRT-D

### 7.3 ICD（植入型心律转复除颤器）

**一级预防**：LVEF≤35%（优化药物≥3月）+ NYHA II-III + 预期生存>1年
- 缺血性心肌病 → I A
- 非缺血性心肌病 → I A（DANISH后仍推荐，尤其较年轻患者）

**二级预防**：VF/血流动力学不稳定 VT 存活（排除可逆原因）→ I A

---

## 八、择期 PCI 围术期抗凝管理

### 8.1 华法林患者

| 情况 | 处理 |
|------|------|
| 低血栓风险 | 停药 3-5天，INR<1.5 即可 |
| 高血栓风险（机械瓣/近期PE） | 停药+低分子肝素桥接 |

### 8.2 NOAC 患者

| 药物 | 术前停药 |
|------|---------|
| 达比加群（CrCl≥80） | 24h |
| 达比加群（CrCl 50-79） | 36h |
| 达比加群（CrCl 30-49） | 48h |
| 利伐沙班/阿哌沙班/依度沙班（CrCl≥30） | 24h |
| 同上（CrCl 15-29） | 36h |

**一般不需桥接**（NOAC 起效快、半衰期短）

---

## 输出规范

```
╔══════════════════════════════════╗
║  🩻 介入诊疗建议                  ║
╠══════════════════════════════════╣
║ 临床情况：[STEMI/NSTEMI/CCS...]  ║
║ 冠脉解剖：[描述]                 ║
║ SYNTAX 评分（如适用）：X 分      ║
╠══════════════════════════════════╣
║ 📋 策略推荐：                    ║
║  [PCI / CABG / 药物治疗]         ║
╠══════════════════════════════════╣
║ 🎯 操作要点：                    ║
║  1. 入路：[桡/股]               ║
║  2. 支架策略：...               ║
║  3. DAPT 方案：... 时长：...    ║
║  4. IVUS/OCT 指导：推荐/可选     ║
╠══════════════════════════════════╣
║ ⚠️ CIN 预防：[...水化方案...]    ║
║ 🚫 注意事项：...                  ║
╚══════════════════════════════════╝
```
