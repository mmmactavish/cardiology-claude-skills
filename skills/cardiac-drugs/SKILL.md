---
name: cardiac-drugs
description: >
  Cardiovascular drug quick reference.
  Covers antihypertensives (ACEI/ARB/ARNI/CCB/BB/diuretics), antiarrhythmics,
  HF GDMT, lipid-lowering (statins/PCSK9i/ezetimibe), vasoactives (pressors/inotropes),
  SGLT2i & GLP-1RA. Query by drug name or class → dosing, cautions, interactions.

  心血管药物速查手册。涵盖降压药、抗心律失常药、心衰GDMT、调脂药、
  血管活性药、SGLT2i/GLP-1RA。输入药名或类别即可获得用法用量与注意事项。
triggers:
  - antihypertensive: antihypertensive/ACEI/ARB/CCB/amlodipine/nifedipine/valsartan/降压药/高血压药物/氨氯地平/硝苯地平/缬沙坦
  - HF: heart failure/GDMT/ARNI/sacubitril/valsartan/carvedilol/metoprolol/spironolactone/心衰药物/沙库巴曲缬沙坦
  - antiarrhythmic: antiarrhythmic/amiodarone/propafenone/lidocaine/verapamil/adenosine/digoxin/抗心律失常/胺碘酮
  - lipid: statin/atorvastatin/rosuvastatin/ezetimibe/PCSK9/inclisiran/lipid-lowering/他汀/降脂/依折麦布
  - vasopressor: vasopressor/norepinephrine/dopamine/epinephrine/inotrope/dobutamine/milrinone/升压/强心/血管活性药
  - diuretic: furosemide/HCTZ/spironolactone/diuretic/利尿/呋塞米/氢氯噻嗪/螺内酯
  - betablocker: beta blocker/metoprolol/bisoprolol/carvedilol/美托洛尔/比索洛尔/卡维地洛
  - antianginal: nitrate/ivabradine/nicorandil/trimetazidine/硝酸甘油/曲美他嗪/尼可地尔
  - SGLT2: SGLT2/dapagliflozin/empagliflozin/达格列净/恩格列净
  - GLP1: GLP-1/semaglutide/liraglutide/司美格鲁肽/利拉鲁肽
metadata:
  author: Cardiology Claude Skills
  version: "1.0"
  languages: [en, zh]
---

# 心血管药物速查手册

根据用户输入查询药物信息，提供剂量、注意事项、相互作用等结构化信息。

---

## 一、抗高血压药物

### 1.1 ACEI（血管紧张素转化酶抑制剂）

| 药物 | 起始剂量 | 目标/最大剂量 | 频次 |
|------|---------|-------------|------|
| 贝那普利 | 5-10mg | 20-40mg | qd |
| 培哚普利 | 4mg | 8mg | qd |
| 雷米普利 | 2.5mg | 10mg | qd |
| 依那普利 | 5mg | 20mg | bid |
| 赖诺普利 | 5-10mg | 20-40mg | qd |

**注意**：Cr >3mg/dL 或 CrCl<30 时减量；妊娠禁用
**主要不良反应**：干咳（10-20%）、血管性水肿（罕见但危急）、高钾、Cr↑

### 1.2 ARB（血管紧张素Ⅱ受体拮抗剂）

| 药物 | 起始剂量 | 目标/最大剂量 | 频次 |
|------|---------|-------------|------|
| 缬沙坦 | 80mg | 160mg bid | qd-bid |
| 厄贝沙坦 | 150mg | 300mg | qd |
| 替米沙坦 | 40mg | 80mg | qd |
| 坎地沙坦 | 8mg | 32mg | qd |
| 氯沙坦 | 50mg | 100mg | qd |

**优势**：干咳发生率 <1%（ACEI 不耐受者替代）

### 1.3 ARNI（血管紧张素受体-脑啡肽酶抑制剂）

**沙库巴曲缬沙坦（Entresto®）**：
- 起始：24/26mg bid → 目标 97/103mg bid
- 洗脱期：ACEI 停药 ≥36h
- 适应证：HFrEF（EF≤40%）/ 高血压
- **禁忌**：妊娠、ACEI 合用、血管性水肿史

### 1.4 CCB（钙通道阻滞剂）

| 药物 | 起始剂量 | 最大剂量 | 频次 |
|------|---------|---------|------|
| 氨氯地平 | 2.5-5mg | 10mg | qd |
| 硝苯地平控释片 | 30mg | 90mg | qd |
| 非洛地平 | 5mg | 10mg | qd |
| 地尔硫䓬 | 90mg bid（缓释） | 360mg | qd-bid |
| 维拉帕米 | 120-240mg（缓释） | 480mg | qd |

**注意**：非二氢吡啶类（地尔硫䓬/维拉帕米）→ 负性肌力，HFrEF 禁用

### 1.5 β受体阻滞剂

| 药物 | 起始剂量 | 目标剂量 | 频次 |
|------|---------|---------|------|
| 美托洛尔（酒石酸） | 25mg | 100mg bid | bid |
| 美托洛尔（琥珀酸缓释） | 23.75-47.5mg | 190mg | qd |
| 比索洛尔 | 2.5mg | 10mg | qd |
| 卡维地洛 | 3.125mg | 25mg bid | bid |

### 1.6 利尿剂

| 药物 | 剂量 |
|------|------|
| 氢氯噻嗪 | 12.5-25mg qd |
| 吲达帕胺 | 1.5mg（缓释）/ 2.5mg（常释）qd |
| 呋塞米 | 20-40mg qd-bid（max 600mg/d） |
| 螺内酯 | 20-40mg qd |
| 阿米洛利 | 5-10mg qd |

---

## 二、抗心律失常药物（Vaughan-Williams 分类）

### I 类（钠通道阻滞剂）

| 亚类 | 药物 | 剂量 | 主要用途 |
|------|------|------|---------|
| Ia | 奎尼丁 | 200-400mg tid-qid | 房颤复律（少用） |
| Ia | 普鲁卡因胺 | 10-15mg/kg IV | 室性心律失常 |
| Ib | 利多卡因 | 1-1.5mg/kg IV bolus→1-4mg/min | 室速/室颤（AMI相关） |
| Ic | 普罗帕酮 | 150mg tid / 2mg/kg IV | 房颤复律（无结构性心脏病） |

**注意**：Ic 类禁用于冠心病/心衰/左室肥厚（CAST 研究教训）

### II 类（β受体阻滞剂）— 见降压药部分

### III 类（钾通道阻滞剂）

| 药物 | 剂量 | 用途 |
|------|------|------|
| 胺碘酮 | 负荷 800-1600mg/d×1-3周 → 200-400mg qd 维持 | 房颤/室性心律失常 |
| 胺碘酮 IV | 150mg/10min → 1mg/min×6h → 0.5mg/min 维持 | 紧急复律 |
| 决奈达隆 | 400mg bid | 房颤维持窦律（无HF） |
| 索他洛尔 | 80-160mg bid | 房颤/室性 |

**胺碘酮注意**：肺纤维化、甲功异常、肝毒性、角膜沉积、光敏 → 每6月查甲功/肝功能/胸片
**决奈达隆**：NYHA IV级 / 不稳定心衰 → 禁用

### IV 类（钙通道阻滞剂）

| 药物 | 剂量 | 用途 |
|------|------|------|
| 维拉帕米 | 5-10mg IV / 240mg qd PO | PSVT 急性终止 |
| 地尔硫䓬 | 0.25mg/kg IV / 180-360mg qd PO | 房颤/房扑 心率控制 |

### 其他

| 药物 | 剂量 | 用途 |
|------|------|------|
| 腺苷 | 6mg→12mg→12mg 快速 IV 推注 | PSVT 诊断+终止（首选） |
| 地高辛 | 0.125-0.25mg qd | 房颤心率控制 / HFrEF 辅助 |
| 伊伐布雷定 | 5-7.5mg bid | 窦律心率 >70bpm + HFrEF |

---

## 三、心衰 GDMT（指南指导的药物治疗）

### HFrEF（EF≤40%）四联疗法：

| 类别 | 代表药物 | 目标剂量 |
|------|---------|---------|
| ARNI / ACEI / ARB | 沙库巴曲缬沙坦 | 97/103mg bid |
| β阻滞剂 | 美托洛尔缓释/比索洛尔/卡维地洛 | 见上表 |
| MRA | 螺内酯 25-50mg qd / 依普利酮 50mg qd | |
| SGLT2i | 达格列净 10mg qd / 恩格列净 10mg qd | |

### HFpEF（EF≥50%）：
- SGLT2i（达格列净/恩格列净）→ I 类推荐
- 利尿剂控制容量
- ARNI/ARB/MRA → IIb 类

---

## 四、调脂药物

| 药物 | 常用剂量 | LDL-C 降幅 |
|------|---------|-----------|
| 阿托伐他汀 | 10-80mg qn | 37-55% |
| 瑞舒伐他汀 | 5-20mg qn | 39-55% |
| 匹伐他汀 | 2-4mg qn | 32-41% |
| 依折麦布 | 10mg qd | 18-25% |
| PCSK9i（依洛尤单抗） | 140mg q2w SC / 420mg qm | 50-60% |
| PCSK9i（阿利西尤单抗） | 75-150mg q2w SC | 45-60% |
| Inclisiran | 284mg SC（D1→D90→q6m） | 50% |
| 贝派地酸 | 180mg qd | 18-20% |

**他汀不耐受处理**：换药/减量/隔日给药 + 依折麦布 ± PCSK9i

---

## 五、血管活性药物

### 升压药（ICU 常用）

| 药物 | 常用剂量范围 | α | β | 首选场景 |
|------|-------------|----|----|---------|
| 去甲肾上腺素 | 0.05-1.0 μg/kg/min | +++ | + | 分布性休克（首选） |
| 多巴胺 | 2-20 μg/kg/min | 剂量依赖 | 剂量依赖 | 有心动过缓时 |
| 肾上腺素 | 0.01-0.5 μg/kg/min | ++ | +++ | 过敏性休克/CPA |
| 去氧肾上腺素 | 0.5-5 μg/kg/min | +++ | 0 | NO-induced LVOTO |
| 血管加压素 | 0.01-0.04 U/min | V1 | 0 | 辅助NA（顽固性休克） |

### 正性肌力药

| 药物 | 剂量 | 机制 | 场景 |
|------|------|------|------|
| 多巴酚丁胺 | 2-20 μg/kg/min | β1>>β2>α | 心源性休克/急性心衰 |
| 米力农 | 0.125-0.75 μg/kg/min | PDE3i | 慢性心衰急性失代偿 |
| 左西孟旦 | 0.05-0.2 μg/kg/min | Ca增敏剂 | 急性心衰（β阻滞剂下） |

---

## 六、SGLT2i / GLP-1RA（心血管获益）

### SGLT2i

| 药物 | 心衰获益 | CKD获益 | 剂量 |
|------|---------|---------|------|
| 达格列净 | ✅ DAPA-HF/DELIVER | ✅ DAPA-CKD | 10mg qd |
| 恩格列净 | ✅ EMPEROR-Reduced/Preserved | ✅ EMPA-Kidney | 10mg qd |

**适应证**：HFrEF / HFpEF（不论是否糖尿病）、CKD

### GLP-1RA

| 药物 | CVOT 结果 | 剂量 |
|------|----------|------|
| 司美格鲁肽（注射） | SUSTAIN-6：MACE ↓26% | 0.5-1.0mg qw SC |
| 司美格鲁肽（口服） | PIONEER-6：非劣效 | 7-14mg qd |
| 利拉鲁肽 | LEADER：MACE ↓13% | 1.8mg qd SC |
| 度拉糖肽 | REWIND：MACE ↓12% | 1.5mg qw SC |

---

## 输出规范

```
╔══════════════════════════════╗
║  💊 [药物名称]               ║
╠══════════════════════════════╣
║ 类别：[ACEI/ARB/CCB...]     ║
║ 适应证：[...]                ║
╠══════════════════════════════╣
║ 起始剂量：X mg               ║
║ 目标剂量：X mg               ║
║ 最大剂量：X mg               ║
║ 服用频次：qd/bid/tid         ║
╠══════════════════════════════╣
║ ⚠️ 主要不良反应：            ║
║ 🚫 禁忌证：                   ║
║ 🔄 药物相互作用：            ║
║ 🩺 监测指标：                 ║
╚══════════════════════════════╝
```
