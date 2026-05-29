---
name: ecg-help
description: >
  ECG interpretation assistant. Covers STEMI localization, arrhythmia differential
  (AF/AFL/SVT/VT/conduction blocks), electrolyte patterns (K/Ca), pacemaker ECGs,
  QT interval analysis, and critical value recognition.
  Describe ECG findings → get interpretation and differential diagnosis.

  心电图解读辅助工具。涵盖STEMI定位、心律失常鉴别（房颤/房扑/室上速/室速/传导阻滞）、
  电解质异常（高钾/低钾）、起搏器心电图、QT间期分析、危急值识别。
  描述心电图特征即可获得判读意见和鉴别诊断。
triggers:
  - ECG: ECG/EKG/electrocardiogram/心电图/心电
  - STEMI: STEMI/ST elevation/MI localization/ST段抬高/心梗定位/导联
  - arrhythmia: arrhythmia/AF/atrial fibrillation/atrial flutter/SVT/VT/wide complex tachycardia/心律失常/房颤/房扑/室速/室上速
  - block: AV block/LBBB/RBBB/bundle branch block/heart block/传导阻滞/房室传导/左束支/右束支
  - QT: QT/QTc/long QT/short QT/TdP/长QT/短QT
  - electrolyte: hyperkalemia/hypokalemia/hypercalcemia/hypocalcemia ECG/高钾/低钾/高钙/低钙
  - pacemaker: pacemaker/paced rhythm/CRT/biventricular pacing/起搏器/起搏心电图
metadata:
  author: Cardiology Claude Skills
  version: "1.0"
  languages: [en, zh]
---

# ECG Interpretation · 心电图解读辅助

帮助判读心电图，提供定位诊断和鉴别诊断。用户提供 ECG 描述或参数，Claude 给出分析。

---

## 一、正常心电图参考值

| 参数 | 正常范围 |
|------|---------|
| 心率 | 60-100 bpm |
| PR 间期 | 120-200 ms（3-5 小格） |
| QRS 时限 | <110-120 ms（<3 小格） |
| QTc | 男 <450ms / 女 <460ms |
| 电轴 | -30° 到 +90° |
| P 波 | 肢导 <2.5mm / 胸导 <1.5mm 高、<120ms 宽 |
| R 波递增 | V1→V5 逐渐增高 |

---

## 二、STEMI 定位诊断

### 2.1 罪犯血管定位表

| ST 段抬高导联 | 镜像性 ST 压低 | 罪犯血管 | 心梗部位 |
|--------------|---------------|---------|---------|
| V1-V2 | — | LAD（间隔支） | 前间壁 |
| V1-V4 | II, III, aVF | LAD（中段） | 前壁 |
| V1-V6 | II, III, aVF | LAD（近段） | 广泛前壁 |
| I, aVL, V5-V6 | II, III, aVF | LCx（钝缘支） | 侧壁/高侧壁 |
| II, III, aVF | I, aVL | RCA（80%）或 LCx（20%） | 下壁 |
| II, III, aVF + V1 / V4R | I, aVL | RCA 近段 | 下壁+右室 |
| V7-V9（后壁） | V1-V3 ST↓+高R波 | RCA 或 LCx | 后壁 |
| aVR 抬高 >V1 | 广泛ST↓ | LM 或严重三支 | 左主干等危 |

### 2.2 STEMI 诊断标准

- **ST 段抬高**（V2-V3 以外）：J 点处 ≥1mm（肢体导联）/ ≥1mm（胸导联）
- **V2-V3**：男 <40岁 ≥2.5mm / 男 ≥40岁 ≥2mm / 女 ≥1.5mm
- **后壁心梗**：V1-V3 ST 段压低 + 高 R 波 + V7-V9 ST 抬高 ≥0.5mm
- **新发 LBBB** + 缺血症状 → 等同 STEMI（Sgarbossa 标准）

### 2.3 Sgarbossa 标准（LBBB 或起搏心律下诊断心梗）

| 标准 | 分值 |
|------|------|
| ST 段同向抬高 ≥1mm（与 QRS 主波同向） | 5 分 |
| V1-V3 ST 段压低 ≥1mm | 3 分 |
| ST 段反向抬高 ≥5mm（与 QRS 主波反向） | 2 分 |

≥3 分 → 90%+ 特异性诊断急性心梗

---

## 三、心律失常判读

### 3.1 窄 QRS 心动过速（QRS<120ms）→ 室上性

| 表现 | 诊断 | 关键特征 |
|------|------|---------|
| P 波消失 + RR 绝对不齐 | **房颤** | 细颤 f 波 |
| 锯齿状 F 波（250-350bpm）+ 固定房室传导 | **房扑** | II/III/aVF 负向 F 波（典型房扑） |
| RP 短（RP<PR），突发突止 | **AVNRT**（典型） | P 波藏在 QRS 末 |
| RP 短，旁路逆传 P'波 | **AVRT**（顺向型） | δ波（窦律时） |
| P 波在 ST 段，RP 长 | **AT**（房性心动过速） | 温醒/冷却现象 |
| 心率 150bpm ± | **房扑 2:1** | 别忘了找隐藏的 F 波！ |

### 3.2 宽 QRS 心动过速（QRS≥120ms）→ 室速 vs 室上速伴差传

**Brugada 四步法**：
1. V1-V6 有无 RS 波？→ 无 → **室速**
2. 任一胸导 RS 间期 >100ms？→ 有 → **室速**
3. 房室分离？→ 有 → **室速**
4. QRS 形态符合室速标准？→ 是 → **室速**

**Vereckei 四步法（aVR 导联法）**：
1. aVR 初始 R 波？→ 是 → **室速**
2. aVR 初始 r 或 q 波宽度 >40ms？→ 是 → **室速**
3. aVR 负向 QRS 降支切迹？→ 是 → **室速**
4. Vi/Vt ≤1？→ 是 → **室速**

> 80% 宽 QRS 心动过速 = 室速！不确定时按室速处理

### 3.3 房颤心电图特征
- RR 间期绝对不规则
- P 波消失，代以 f 波（>350/min）
- 伴差传 vs 室早：差传 → Ashman 现象（长-短周期后）+ rSR' 形态（V1）

---

## 四、传导阻滞

### 4.1 房室传导阻滞

| 类型 | PR | QRS-宽窄 | 特征 |
|------|-----|---------|------|
| 一度 AVB | PR >200ms 固定 | 窄 | 每个 P 后有 QRS |
| 二度 I 型（文氏） | PR 逐渐延长→P 未下传 | 窄 | PR 逐渐延长→脱落 |
| 二度 II 型（莫氏） | PR 固定 | 宽 | 突然脱落（无 PR 延长） |
| 2:1 AVB | — | 可宽可窄 | 无法区分 I/II 型 |
| 高度 AVB | — | 可宽可窄 | ≥2个连续 P 未下传 |
| 三度 AVB | — | 宽（室性逸搏） | P 与 QRS 完全分离 |

**二度 II 型 / 高度 AVB / 三度 AVB → 起搏器适应证**

### 4.2 束支传导阻滞

**LBBB 诊断标准**：
- QRS ≥120ms（完全性）/ 110-119ms（不完全性）
- V1：rS 或 QS（宽深 S 波）
- V5-V6：宽大 R 波（无 q 波），R 波顶峰切迹
- I, aVL 类似 V5-V6
- 继发性 ST-T 改变（与 QRS 主波反向）

**RBBB 诊断标准**：
- QRS ≥120ms
- V1：rsR'（兔耳征）
- V5-V6：宽深 S 波（qRS）
- 继发性 ST-T 改变

### 4.3 左前/左后分支阻滞

| 左前分支阻滞 | 左后分支阻滞 |
|-------------|-------------|
| 电轴左偏 ≤-45° | 电轴右偏 ≥+120° |
| I, aVL：qR | I：rS |
| II, III, aVF：rS | II, III, aVF：qR |
| QRS <120ms | QRS <120ms |
| 排除其他电轴左偏原因 | 排除右室肥厚、肺心病 |

---

## 五、电解质异常心电图

### 5.1 钾异常

| 状态 | K⁺范围 | ECG 表现（进行性） |
|------|--------|-------------------|
| 低钾 | <3.5（显著<3.0） | T 波低平/倒置 → U 波明显 → ST 压低 → TU 融合 → QT 假性延长 |
| 高钾 | >5.5 | T 波高尖对称（帐篷T）→ P 波低平消失 → QRS 增宽 → 正弦波 → 室颤/心脏停搏 |

**高钾 ECG 与血钾大致对应**：
- K⁺ 5.5-6.5：T 波高尖
- K⁺ 6.5-7.5：P 波消失
- K⁺ 7.5-8.5：QRS 显著增宽
- K⁺ >8.5：正弦波

### 5.2 钙异常

| 状态 | ECG 表现 |
|------|---------|
| 低钙 | **QTc 延长**（ST 段延长为主），T 波正常 |
| 高钙 | **QTc 缩短**（ST 段缩短），Osborn 波可见 |

---

## 六、QT 间期分析

### QTc 计算公式

- **Bazett**：QTc = QT / √RR（最常用，心率快时过度校正）
- **Fridericia**：QTc = QT / ∛RR（心率快时更准确）
- **Framingham**：QTc = QT + 154 × (1 - RR)

### QTc 延长

| 程度 | 男 | 女 |
|------|----|----|
| 正常 | ≤430ms | ≤450ms |
| 临界 | 431-450ms | 451-470ms |
| 延长 | >450ms | >470ms |
| 高危 | >500ms | >500ms |

**后天性长 QT 常见原因**：药物（Ia/III类抗心律失常、氟喹诺酮、大环内酯、抗真菌唑类、抗精神病药、止吐药）、电解质紊乱（低钾/低镁/低钙）、心肌缺血、严重心动过缓、甲减

---

## 七、起搏器心电图基础

### 起搏钉识别

| 模式 | 起搏钉位置 | 自身QRS |
|------|-----------|--------|
| AAI | P波前有钉→起搏P波 | 有自身R |
| VVI | QRS前有钉→起搏QRS（宽） | 有自身P |
| DDD | P前+QRS前均有钉 | 可能融合 |

### 起搏心电图心梗判断
- 起搏 QRS 通常 LBBB 形态（右室起搏）→ 应用 **Sgarbossa 标准**

---

## 八、危急值心电图（立即处理）

| 表现 | 处理 |
|------|------|
| 室速/室颤 | 电复律/除颤 |
| 三度 AVB + 缓慢室性逸搏 | 临时起搏 |
| 高钾正弦波 | 钙剂 IV |
| STEMI（尤其是广泛前壁/左主干） | 紧急再灌注 |
| TdP（尖端扭转型室速） | MgSO₄ 2g IV |
| 心脏停搏 | CPR |
| 预激+房颤（R-R 最短 <250ms） | 电复律（禁用 AVN 阻滞剂） |

---

## 输出规范

```
╔══════════════════════════════╗
║  📊 心电图判读               ║
╠══════════════════════════════╣
║ 心率：X bpm                 ║
║ 节律：[窦性/房颤/房扑/...]   ║
║ 电轴：[正常/左偏/右偏]       ║
║ PR 间期：X ms               ║
║ QRS 时限：X ms              ║
║ QTc：X ms（公式）           ║
╠══════════════════════════════╣
║ 🔍 主要发现：               ║
║  1. ST 段：...              ║
║  2. T 波：...               ║
║  3. Q 波：...               ║
╠══════════════════════════════╣
║ 🎯 判读结论：               ║
║  定位诊断：...              ║
║  鉴别诊断：...              ║
╠══════════════════════════════╣
║ 🚨 危急值：是/否             ║
║ 📋 建议：...                 ║
╚══════════════════════════════╝
```
