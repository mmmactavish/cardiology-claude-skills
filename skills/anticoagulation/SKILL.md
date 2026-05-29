---
name: anticoagulation
description: >
  Anticoagulation & antiplatelet management reference.
  Covers NOAC/DOAC dosing, warfarin INR management, heparin/LMWH protocols,
  perioperative bridging, DAPT duration, bleeding reversal strategies.
  Provide patient data (age/weight/renal function/indication) → get specific regimen.

  抗凝与抗血小板药物管理助手。涵盖NOAC/DOAC剂量、华法林INR管理、
  肝素方案、围术期桥接、DAPT时长、出血逆转。提供患者情况即可获得具体用药方案。
triggers:
  - anticoag: anticoag/anticoagulation/NOAC/DOAC/warfarin/heparin/bridging/DAPT/antiplatelet/抗凝/抗凝药/抗血小板
  - NOAC: NOAC/DOAC/dabigatran/rivaroxaban/apixaban/edoxaban/新型口服抗凝药/达比加群/利伐沙班/阿哌沙班/依度沙班
  - warfarin: warfarin/INR/coumadin/华法林/华法令
  - heparin: heparin/LMWH/enoxaparin/fondaparinux/UFH/肝素/低分子肝素/依诺肝素
  - bridging: bridging/perioperative/periprocedural anticoagulation/桥接/围术期抗凝/术前停药
  - DAPT: DAPT/dual antiplatelet/aspirin/clopidogrel/ticagrelor/prasugrel/双抗/双联抗血小板/阿司匹林/氯吡格雷/替格瑞洛
  - bleeding: bleeding reversal/anticoagulant reversal/INR high/PCC/idarucizumab/andexanet/抗凝出血/INR过高/抗凝逆转
metadata:
  author: Cardiology Claude Skills
  version: "1.0"
  languages: [en, zh]
---

# Anticoagulation & Antiplatelet · 抗凝与抗血小板管理

当用户提供患者信息后，根据适应证、肾功能、体重等给出具体用药方案。

---

## 一、NOAC/DOAC 标准剂量

### 1.1 达比加群（Dabigatran，Pradaxa®）

| 适应证 | 标准剂量 | 减量标准 |
|--------|---------|---------|
| 房颤卒中预防 | 150mg bid | 110mg bid（≥80岁 / 合用维拉帕米 / 高出血风险） |
| DVT/PE 急性期 | 150mg bid（肝素先行≥5天） | 110mg bid |

**CrCl 调整**：
- CrCl ≥30 mL/min → 150mg bid
- CrCl 15-29 → 110mg bid（欧洲）/ 75mg bid（美国）
- CrCl <15 / 透析 → 禁用（欧洲）/ 75mg bid（美国透析患者）

### 1.2 利伐沙班（Rivaroxaban，Xarelto®）

| 适应证 | 剂量 |
|--------|------|
| 房颤（CrCl >50） | 20mg qd 晚餐时服 |
| 房颤（CrCl 15-49） | 15mg qd |
| DVT/PE 急性期 | 15mg bid ×21天 → 20mg qd |
| 二级预防 | 10mg qd（>6个月后） |

**CrCl 调整**：CrCl <15 / 透析 → 禁用

### 1.3 阿哌沙班（Apixaban，Eliquis®）

| 适应证 | 标准剂量 | 减量标准（满足≥2项） |
|--------|---------|---------------------|
| 房颤 | 5mg bid | 2.5mg bid（年龄≥80 / 体重≤60kg / Cr≥1.5mg/dL） |
| DVT/PE | 10mg bid ×7天 → 5mg bid | — |

**CrCl 调整**：
- CrCl ≥25 → 标准剂量
- CrCl 15-24 → 谨慎使用（数据有限）
- CrCl <15 / 透析 → 5mg bid（美国）/ 谨慎（欧洲）

### 1.4 依度沙班（Edoxaban，Lixiana®）

| 适应证 | 标准剂量 | 减量标准 |
|--------|---------|---------|
| 房颤 | 60mg qd | 30mg qd（CrCl 15-50 / 体重≤60kg / 合用强效 P-gp 抑制剂） |
| DVT/PE | 60mg qd（肝素先行≥5天） | 30mg qd |

**CrCl <15 / 透析 → 禁用**

---

## 二、NOAC 适应证速查

| 适应证 | 达比加群 | 利伐沙班 | 阿哌沙班 | 依度沙班 |
|--------|---------|---------|---------|---------|
| 非瓣膜性房颤 | ✅ | ✅ | ✅ | ✅ |
| DVT/PE 急性 | ✅ | ✅ | ✅ | ✅ |
| 骨科术后 VTE 预防 | ✅ | ✅ | ✅ | — |
| 机械瓣膜 | ❌ | ❌ | ❌ | ❌ |
| 中重度二狭 | ❌ | ❌ | ❌ | ❌ |
| APS（抗磷脂综合征） | ❌ | ❌ | ❌ | ❌ |
| 妊娠/哺乳 | ❌ | ❌ | ❌ | ❌ |

> **注意**：机械瓣、中重度二尖瓣狭窄、抗磷脂综合征 → 只能用华法林！

---

## 三、华法林管理

### 3.1 目标 INR

| 适应证 | 目标 INR |
|--------|----------|
| 房颤 / DVT / PE | 2.0-3.0 |
| 机械瓣（主动脉瓣双叶） | 2.0-3.0 |
| 机械瓣（二尖瓣/三尖瓣/球笼瓣） | 2.5-3.5 |
| APS（抗磷脂综合征） | 2.5（静脉）/ 2.5-3.0（动脉） |

### 3.2 初始给药方案

**住院患者**（快速达标）：首日 5-10mg，后续根据 INR 调整
**门诊患者**（缓慢达标）：2.5-5mg/日起始，3-7天后查 INR

> 起始同时需重叠肝素/低分子肝素 ≥5 天，直至 INR 连续 2 天达标

### 3.3 INR 过高处理

| INR | 处理 |
|-----|------|
| >3.0-4.5（无出血） | 减量或跳过一次，每周监测 |
| >4.5-10（无出血） | 停 1-2 次 / 口服 VitK 1-2.5mg |
| >10（无出血） | 停华法林 / 口服 VitK 2.5-5mg |
| 任何 INR + 大出血 | 停华法林 / VitK 10mg IV / PCC（4因子） |

### 3.4 华法林围术期桥接

| 情况 | 方案 |
|------|------|
| **低血栓风险**（房颤 CHA₂DS₂-VASc ≤4，VTE>3月） | 单纯停药，无需桥接 |
| **中血栓风险**（房颤 CHA₂DS₂-VASc 5-6，VTE 3-12月） | 停药 + 低分子肝素桥接（个体化） |
| **高血栓风险**（机械瓣、房颤 CHA₂DS₂-VASc ≥7、VTE<3月、近期卒中） | 停药 + 低分子肝素桥接 |

**NOAC 术前停药时间**：

| 药物 | 低出血风险手术 | 高出血风险手术 |
|------|---------------|---------------|
| 达比加群（CrCl≥80/CrCl 50-79/CrCl 30-49） | 24h/36h/48h | 48h/72h/96h |
| 利伐沙班/阿哌沙班/依度沙班 (CrCl≥30) | 24h | 48h |
| 利伐沙班/阿哌沙班/依度沙班 (CrCl 15-29) | 36h | 72h |

---

## 四、肝素/低分子肝素

### 4.1 普通肝素（UFH）

**AMI 溶栓辅助**：60 U/kg 推注（max 4000U）→ 12 U/kg/h 维持（max 1000U/h）
**ACS PCI**：70-100 U/kg 推注（GP IIb/IIIa 合用时 50-70 U/kg）
**治疗性抗凝目标**：aPTT 为对照 1.5-2.5 倍

### 4.2 依诺肝素（Enoxaparin）

| 适应证 | 剂量 |
|--------|------|
| ACS（UA/NSTEMI） | 1mg/kg q12h SC |
| STEMI（保守/溶栓） | 30mg IV 推注 → 1mg/kg q12h SC |
| DVT/PE 治疗 | 1mg/kg q12h SC 或 1.5mg/kg qd SC |
| 外科 VTE 预防 | 40mg qd SC |

**CrCl <30**：治疗剂量减为 1mg/kg qd / 预防 30mg qd

### 4.3 磺达肝癸钠（Fondaparinux）

| 适应证 | 剂量 |
|--------|------|
| UA/NSTEMI（保守治疗） | 2.5mg qd SC |
| DVT/PE | 5mg（<50kg）/ 7.5mg（50-100kg）/ 10mg（>100kg）qd |
| 外科预防 | 2.5mg qd |

**CrCl <20**：禁用

---

## 五、抗血小板治疗

### 5.1 常用药物

| 药物 | 负荷量 | 维持量 |
|------|--------|--------|
| 阿司匹林 | 150-300mg | 75-100mg qd |
| 氯吡格雷 | 300-600mg | 75mg qd |
| 替格瑞洛 | 180mg | 90mg bid |
| 普拉格雷 | 60mg | 10mg qd |

### 5.2 DAPT 时长（2024 更新）

| 临床场景 | DAPT 时长 | 备注 |
|----------|----------|------|
| CCS PCI | 1-3 月 | 高缺血/低出血→延长；反之→缩短 |
| ACS PCI | 6-12 月 | 首选替格瑞洛+阿司匹林 |
| ACS 药物治疗 | ≥12 月 | |
| 高出血风险（PRECISE-DAPT≥25） | 1-3 月 | |
| PCI + 房颤需抗凝 | 1周-1月 | 之后单用抗凝（优选NOAC） |

### 5.3 PRECISE-DAPT 评分

| 因素 | 分值 |
|------|------|
| 年龄 | 每岁+1（起始50岁） |
| CrCl | -1/每5mL/min（起始100） |
| 血红蛋白 | -1/每1g/L（起始12g/dL） |
| WBC | +1/每1×10⁹/L（起始5） |
| 既往自发出血 | +15 |

≥25分 → 高出血风险，推荐缩短 DAPT

---

## 六、出血处理与逆转

| 抗凝药 | 逆转/止血策略 |
|--------|-------------|
| 华法林 | VitK 10mg IV缓慢 + PCC（4因子）25-50 U/kg |
| 达比加群 | Idarucizumab 5g IV |
| 利伐沙班/阿哌沙班 | Andexanet alfa（低剂量400mg bolus+480mg/2h；高剂量800mg bolus+960mg/2h） |
| 依度沙班 | Andexanet alfa |
| 肝素 | 鱼精蛋白 1mg/100U 肝素 |
| 依诺肝素 | 鱼精蛋白 1mg/1mg（8h内）/ 0.5mg/1mg（8-12h） |
| 无逆转剂时 | PCC 25-50 U/kg / 氨甲环酸 1g IV |

---

## 输出规范

提供用药建议时，格式如下：
```
╔══════════════════════════════╗
║  💊 抗凝/抗血小板用药方案     ║
╠══════════════════════════════╣
║ 诊断：[房颤/DVT/PE/ACS...]    ║
║ CrCl：X mL/min              ║
║ 体重：X kg                  ║
╠══════════════════════════════╣
║ 📋 推荐方案：                 ║
║  首选：[药物名] [剂量]       ║
║  备选：[药物名] [剂量]       ║
╠══════════════════════════════╣
║ ⚠️ 注意事项：                 ║
║  1. ...                     ║
║  2. ...                     ║
╚══════════════════════════════╝
```

需询问的信息：年龄、体重、Cr/CrCl、肝功能、合并用药（尤其是 P-gp 抑制剂 / CYP3A4 相互作用）、是否有机械瓣/中重度二狭/APS。
