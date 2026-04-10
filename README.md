# Treatment Plans Skill

AI-driven medical treatment plan generation skill for generating evidence-based, guideline-concordant treatment plans across all clinical specialties.

## Overview

This skill enables AI-powered generation of professional medical treatment plans using the latest clinical guidelines (NCCN 2026, ADA 2026, ACC/AHA 2024, ESC 2023, etc.). It provides structured Markdown templates, comprehensive medication databases, drug interaction checking, and automated PHI de-identification for patient-centered care planning.

**Key Features:**
- 🧠 **AI-Driven Generation**: Direct treatment plan generation from clinical notes or case descriptions
- 📚 **Latest Guidelines**: Incorporates the most current evidence-based guidelines across 12+ medical specialties
- 🔍 **Dynamic Updates**: Uses search tools to retrieve the latest FDA/NCCN/EMA/ESMO recommendations for rapidly evolving fields
- 📝 **Professional Templates**: Structured Markdown templates (one-page and standard formats)
- 💊 **Medication Database**: Comprehensive drug information with dose ranges, interactions, and contraindications
- 🔐 **Privacy Protection**: Built-in PHI detection and de-identification for HIPAA compliance

## Installation

This skill is installed as a standard AI skill package. No additional dependencies required.

**Required Tools:**
- Read
- Write
- Edit
- Bash
- Search
- WebBrowsing

## Quick Start

### Generate a Treatment Plan

Simply provide clinical notes or a case description to the AI. The AI will automatically:

1. Analyze the clinical context
2. Identify diagnoses with ICD-10 codes
3. Generate SMART goals based on patient characteristics and latest guidelines
4. Recommend evidence-based interventions using current standards
5. Check for drug interactions and contraindications
6. Create a structured monitoring and follow-up plan
7. Output a complete, ready-to-use treatment plan in Markdown format

### Example Usage

```
User: 58岁男性，2型糖尿病3年，HbA1c 8.5%，高血压，血压138/88，BMI 28.7，目前服用二甲双胍500mg BID，赖诺普利10mg QD

AI (with treatment-plans skill loaded): [Generates complete treatment plan using ADA 2026 guidelines, recommending SGLT2 inhibitor addition, individualized HbA1c target, appropriate monitoring schedule]
```

## File Structure

```
treatment-plans/
├── SKILL.md                          # Skill documentation and capabilities
├── SYSTEM_PROMPT.md                  # AI knowledge base with clinical guidelines
├── README.md                         # This file
├── assets/                           # Markdown templates
│   ├── one_page_treatment_plan.md    # One-page quick-reference template (PREFERRED)
│   └── standard_treatment_plan.md    # Standard comprehensive template
└── references/                       # Reference materials
    ├── treatment_plan_standards.md   # Professional standards and best practices
    ├── goal_setting_frameworks.md    # SMART goals and patient-centered outcomes
    ├── intervention_guidelines.md    # Evidence-based interventions
    ├── regulatory_compliance.md      # HIPAA compliance and regulatory requirements
    ├── specialty_specific_guidelines.md # Specialty-specific guidelines
    └── README.md                     # Reference documentation
```

## Templates

### 1. One-Page Treatment Plan (PREFERRED)

**When to use:** Straightforward clinical scenarios, standard protocols, busy clinical settings

**Format:** Single page containing all essential treatment information in scannable sections

**Features:**
- Dense, scannable layout
- Similar to precision oncology reports
- All essential information on one page
- Quick-reference format for busy clinicians

### 2. Standard Treatment Plan

**When to use:** Moderate complexity, need for patient education materials, multidisciplinary coordination

**Format:** 3-4 pages with executive summary and detailed sections

**Features:**
- First-page executive summary (Foundation Medicine model)
- Comprehensive documentation
- Detailed monitoring and follow-up plans
- Patient education sections

## Clinical Guidelines Covered

The skill incorporates the latest evidence-based guidelines across 12+ medical specialties:

### Diabetes Management (ADA 2026)
- First-line: Metformin unless contraindicated
- CVD patients: GLP-1 RAs preferred (Class I)
- CKD patients: SGLT2 inhibitors preferred (Class I)
- Individualized HbA1c targets

### Hypertension Management (AHA/ACC 2025)
- ACE inhibitors or ARBs preferred for CAD/CKD
- Target BP: <130/80 mmHg (general adults, encouraged to achieve <120/80 mmHg if tolerated), <140/90 (elderly 80+, institutional care, limited life expectancy, pregnancy)
- Elderly 65-79: <130/80 mmHg if tolerated; consider <140/90 mmHg for frail patients or high fall risk
- Individualize targets based on clinical judgment, tolerance, frailty, and life expectancy
- Single-pill combination for stage 2 hypertension

### Lipid Management (ACC/AHA 2026, ESC/EAS 2025)
- Both ACC/AHA 2026 and ESC/EAS 2025 are authoritative evidence-based guidelines
- **ACC/AHA 2026**: Clinical ASCVD very high risk <55 mg/dL, not at very high risk <70 mg/dL; Primary prevention based on PREVENT-ASCVD risk
- **ESC/EAS 2025**: High risk <70 mg/dL, very high risk <55 mg/dL, extreme risk <40 mg/dL; Strong combination therapy endorsement
- Common targets: <55 mg/dL for very high risk, <70 mg/dL for high risk
- Sources: National Lipid Association (ACC/AHA), Family Heart Foundation (ESC/EAS), verified 2026-04-11
- Stepwise approach: Statin → Ezetimibe → PCSK9 inhibitors; Bempedoic acid for statin-intolerant
- Individualize based on patient risk, tolerance, and comorbidities

### Oncology Guidelines (NCCN 2026)
- Breast, Lung, Prostate, Lymphoma, Ovarian, Melanoma
- Gastric, Pancreatic, Liver, Kidney cancers
- Colon cancer with detailed molecular testing and immunotherapy
- Targeted therapies and immunotherapy recommendations

### Cardiology Guidelines (ACC/AHA 2024-2025)
- Heart Failure: ARNI preferred, SGLT2 inhibitors for HFrEF
- Atrial Fibrillation: DOACs preferred, left atrial appendage occlusion
- Acute Coronary Syndrome: DAPT duration, high-intensity statins
- Valvular Disease: TAVR, transcatheter edge-to-edge repair

### Respiratory Guidelines (GOLD 2025, ATS 2024)
- COPD: Smoking cessation, bronchodilators (LAMA/LABA)
- Asthma: ICS-containing controller preferred over SABA alone
- Pulmonary Embolism: Risk-stratified management, outpatient treatment

### Rheumatology Guidelines (ACR 2019-2021)
- Rheumatoid Arthritis: Treat-to-target, methotrexate first-line
- Osteoarthritis: Topical NSAIDs first, opioids avoided
- Osteoporosis: FRAX assessment, bisphosphonates first-line
- Gout: Treat-to-target uric acid <6 mg/dL

### Neurology Guidelines (AAN 2023-2024)
- Stroke: DAPT for minor stroke/TIA, endovascular thrombectomy for LVO
- Epilepsy: First-line AEDs, avoid enzyme inducers in women of childbearing age
- Multiple Sclerosis: DMTs based on disease activity, early treatment
- Parkinson's Disease: Levodopa most effective, DBS for advanced

### Infectious Disease Guidelines (IDSA 2023-2024)
- Pneumonia: Local resistance patterns guide empiric therapy
- Urinary Tract Infection: Nitrofurantoin first-line for cystitis
- Sepsis: 1-hour bundle, broad-spectrum antibiotics within 3 hours
- HIV: ART for all, integrase inhibitors preferred

### Psychiatry Guidelines (APA 2022-2024)
- Depression: SSRIs first-line, psychotherapy for mild-moderate
- Anxiety: SSRIs/SNRIs first-line, benzodiazepines short-term only
- Bipolar Disorder: Mood stabilizers, quetiapine for depression
- Schizophrenia: Second-generation antipsychotics, clozapine for treatment-resistant

### Geriatrics Guidelines (AGS Beers 2023)
- Avoid: Anticholinergics, benzodiazepines, meperidine, sliding scale insulin
- Deprescribing: Review medications annually
- Falls prevention: Multifactorial intervention, vitamin D, exercise

## Dynamic Guideline Updates

### The Static Prompt Paradox Solution

To address the challenge of static guidelines becoming outdated, this skill includes:

**Search Tool Integration:**
- For rapidly evolving fields (oncology targeted therapies, newly approved medications, emerging clinical evidence, drug safety alerts), the AI is instructed to use search tools to retrieve current FDA/NCCN/EMA/ESMO recommendations
- Guidelines provided in SYSTEM_PROMPT.md serve as a foundation, but web-retrieved information is used for verification
- Search date and source are documented when using web-retrieved information

**Critical Directive:**
```
For rapidly evolving medical fields, you MUST use search tools to retrieve the most current information. Do NOT rely solely on static guidelines embedded in this prompt.
```

## Self-Verification Mechanism

Before finalizing any treatment plan, the AI performs a self-verification check:

1. **Risk Stratification**: Verify patient risk level is correctly assessed
2. **Target Alignment**: Ensure treatment targets match patient risk level
3. **Stepwise Approach**: Verify stepwise treatment approach is considered
4. **Baseline Consideration**: Anticipate need for combination therapy based on baseline values
5. **Guideline Version**: Explicitly state guideline version used
6. **Comorbidities**: Verify all comorbidities are addressed

## Quality Assurance

### Documentation Standards

- **Completeness**: All required sections present
- **SMART Goals**: Goals meet specific, measurable, achievable, relevant, time-bound criteria
- **Evidence-Based**: Interventions based on current clinical practice guidelines
- **Patient-Centered**: Plans align with patient preferences and clinical context
- **Privacy-Compliant**: Automatic PHI detection and de-identification

### Regulatory Compliance

- **HIPAA**: De-identification per Safe Harbor method
- **Informed Consent**: Document patient understanding and agreement
- **Medical Necessity**: Documentation supports billing requirements
- **Quality Reporting**: Enable extraction of quality metrics

## Disclaimer

**IMPORTANT: This skill generates AI-assisted treatment plans based on current guideline recommendations.**

- Final clinical decisions, dose adjustments, and prescribing authority must be approved by the attending physician based on individual patient circumstances (such as real-time liver and kidney function indicators)
- AI-generated treatment plans are for reference only and do not replace physician clinical judgment and decision-making
- Physicians should consider patient-specific factors, real-time laboratory indicators, drug interactions, allergy history, and other factors when making final decisions
- Always verify guideline versions and consult current sources, especially for rapidly evolving fields

## License

MIT License

## Author

bbylw

## Version

Guideline Version: ADA 2026, ACC/AHA 2024, ESC 2023, NCCN 2026
Last Updated: April 2026

## Support

For issues or questions, please refer to the skill documentation in SKILL.md and reference materials in the references/ directory.

---

# 治疗方案技能

AI驱动的医疗治疗方案生成技能，用于生成基于循证医学、符合指南的临床治疗方案，涵盖所有临床专科。

## 概述

本技能利用最新的临床指南（NCCN 2026、ADA 2026、ACC/AHA 2024、ESC 2023等）实现AI驱动的专业医疗治疗方案生成。提供结构化Markdown模板、全面的药物数据库、药物相互作用检查和自动PHI去识别功能，支持以患者为中心的护理计划制定。

**核心特性:**
- 🧠 **AI驱动生成**: 直接从临床记录或病例描述生成治疗方案
- 📚 **最新指南**: 整合12+医学专科的最新循证指南
- 🔍 **动态更新**: 使用搜索工具检索快速演进领域的最新FDA/NCCN/EMA/ESMO推荐
- 📝 **专业模板**: 结构化Markdown模板（单页和标准格式）
- 💊 **药物数据库**: 全面的药物信息，包括剂量范围、相互作用和禁忌症
- 🔐 **隐私保护**: 内置PHI检测和去识别功能，符合HIPAA合规要求

## 安装

本技能作为标准AI技能包安装。无需额外依赖。

**所需工具:**
- Read / 读取
- Write / 写入
- Edit / 编辑
- Bash / 命令行
- Search / 搜索
- WebBrowsing / 网页浏览

## 快速开始

### 生成治疗方案

只需向AI提供临床记录或病例描述。AI将自动：

1. 分析临床背景
2. 识别诊断并标注ICD-10代码
3. 根据患者特征和最新指南生成SMART目标
4. 基于当前标准推荐循证干预措施
5. 检查药物相互作用和禁忌症
6. 创建结构化监测和随访计划
7. 输出完整的、可直接使用的Markdown格式治疗方案

### 使用示例

```
User: 58岁男性，2型糖尿病3年，HbA1c 8.5%，高血压，血压138/88，BMI 28.7，目前服用二甲双胍500mg BID，赖诺普利10mg QD

AI (with treatment-plans skill loaded): [Generates complete treatment plan using ADA 2026 guidelines, recommending SGLT2 inhibitor addition, individualized HbA1c target, appropriate monitoring schedule]

AI（加载treatment-plans技能后）：[使用ADA 2026指南生成完整治疗方案，推荐添加SGLT2抑制剂、个体化HbA1c目标、适当的监测计划]
```

## 文件结构

```
treatment-plans/
├── SKILL.md                          # 技能文档和功能
├── SYSTEM_PROMPT.md                  # AI知识库（含临床指南）
├── README.md                         # 本文件
├── assets/                           # Markdown模板
│   ├── one_page_treatment_plan.md    # 单页快速参考模板（首选）
│   └── standard_treatment_plan.md    # 标准综合模板
└── references/                       # 参考资料
    ├── treatment_plan_standards.md   # 专业标准和最佳实践
    ├── goal_setting_frameworks.md    # SMART目标和以患者为中心的结局
    ├── intervention_guidelines.md    # 循证干预措施
    ├── regulatory_compliance.md      # HIPAA合规和法规要求
    ├── specialty_specific_guidelines.md # 专科特定指南
    └── README.md                     # 参考文档
```

## 模板

### 1. 单页治疗方案 (首选)

**适用场景:** 简单临床场景、标准方案、繁忙的临床环境

**格式:** 单页包含所有基本治疗信息的可扫描章节

**特性:**
- 密集、可扫描的布局
- 类似精准肿瘤学报告
- 所有基本信息在一页
- 为繁忙的临床医生提供的快速参考格式

### 2. 标准治疗方案

**适用场景:** 中等复杂度、需要患者教育材料、多学科协调

**格式:** 3-4页，包含执行摘要和详细章节

**特性:**
- 首页执行摘要（Foundation Medicine模型）
- 全面的文档
- 详细的监测和随访计划
- 患者教育章节

## 涵盖的临床指南

本技能整合12+医学专科的最新循证指南：

### 糖尿病管理 (ADA 2026)
- 一线：二甲双胍，除非有禁忌症
- CVD患者：GLP-1受体激动剂优先（I类推荐）
- CKD患者：SGLT2抑制剂优先（I类推荐）
- 个体化HbA1c目标

### 高血压管理 (AHA/ACC 2025)
- CAD/CKD患者首选ACE抑制剂或ARB
- 目标血压：<130/80 mmHg（一般成年人，鼓励达到<120/80 mmHg如耐受），<140/90（80岁以上老年人、机构护理、预期寿命有限、孕妇）
- 65-79岁老年人：<130/80 mmHg如耐受；虚弱或高跌倒风险患者考虑<140/90 mmHg
- 根据临床判断、耐受性、虚弱程度和预期寿命个体化目标
- 2期高血压使用单片联合制剂

### 血脂管理 (ACC/AHA 2026, ESC/EAS 2025)
- ACC/AHA 2026和ESC/EAS 2025均为权威循证指南
- **ACC/AHA 2026**：临床ASCVD极高危<55 mg/dL，非极高危<70 mg/dL；一级预防基于PREVENT-ASCVD风险
- **ESC/EAS 2025**：高危<70 mg/dL，极高危<55 mg/dL，极高风险<40 mg/dL；强烈推荐联合治疗
- 共同目标：极高危<55 mg/dL，高危<70 mg/dL
- 来源：National Lipid Association (ACC/AHA)，Family Heart Foundation (ESC/EAS)，验证于2026-04-11
- 阶梯式方法：他汀→依折麦布→PCSK9抑制剂；他汀不耐受者使用Bempedoic acid
- 根据患者风险、耐受性和合并症个体化

### 肿瘤学指南 (NCCN 2026)
- 乳腺癌、肺癌、前列腺癌、淋巴瘤、卵巢癌、黑色素瘤
- 胃癌、胰腺癌、肝癌、肾癌
- 结肠癌：详细分子检测和免疫治疗
- 靶向治疗和免疫治疗推荐

### 心脏病学指南 (ACC/AHA 2024-2025)
- 心力衰竭：ARNI优先，HFrEF使用SGLT2抑制剂
- 心房颤动：DOAC优先，左心耳封堵
- 急性冠脉综合征：DAPT持续时间，高强度他汀
- 瓣膜性心脏病：TAVR，经导管缘对缘修复

### 呼吸系统指南 (GOLD 2025, ATS 2024)
- COPD：戒烟，支气管扩张剂（LAMA/LABA）
- 哮喘：含ICS的控制器优于单独SABA
- 肺栓塞：风险分层管理，门诊治疗

### 风湿病学指南 (ACR 2019-2021)
- 类风湿关节炎：达标治疗，甲氨蝶呍一线
- 骨关节炎：外用NSAIDs首选，避免阿片类药物
- 骨质疏松：FRAX评估，双膦酸盐一线
- 痛风：达标治疗尿酸<6 mg/dL

### 神经病学指南 (AAN 2023-2024)
- 卒中：轻型卒中/TIA使用DAPT，大血管闭塞取栓
- 癫痫：一线AEDs，育龄女性避免酶诱导剂
- 多发性硬化症：根据疾病活动选择DMTs，早期治疗
- 帕金森病：左旋多巴最有效，晚期DBS

### 感染性疾病指南 (IDSA 2023-2024)
- 肺炎：根据当地耐药模式指导经验性治疗
- 尿路感染：硝基呋喃妥因一线治疗膀胱炎
- 脓毒症：1小时集束化，3小时内广谱抗生素
- HIV：所有患者ART，整合酶抑制剂优先

### 精神病学指南 (APA 2022-2024)
- 抑郁症：SSRIs一线，轻中度心理治疗
- 焦虑症：SSRIs/SNRIs一线，苯二氮卓仅短期使用
- 双相情感障碍：情绪稳定剂，抑郁期喹硫平
- 精神分裂症：第二代抗精神病药，难治性氯氮平

### 老年病学指南 (AGS Beers 2023)
- 避免：抗胆碱能药、苯二氮卓类、哌替啶、滑动胰岛素
- 处方精简：每年审查药物
- 跌倒预防：多因素干预，维生素D，运动

## 动态指南更新

### 静态提示词悖论解决方案

为解决静态指南过时的挑战，本技能包含：

**搜索工具集成:**
- 对于快速演进领域（肿瘤靶向治疗、新获批药物、新兴临床证据、药物安全警报），AI被指示使用搜索工具检索当前FDA/NCCN/EMA/ESMO推荐
- SYSTEM_PROMPT.md中提供的指南作为基础，但使用网络检索信息进行验证
- 使用网络检索信息时记录搜索日期和来源

**关键指令:**
```
对于快速演进的医学领域，您必须使用搜索工具检索最新信息。不得仅依赖本提示词中嵌入的静态指南。
```

## 自我验证机制

在最终确定任何治疗方案之前，AI执行自我验证检查：

1. **风险分层**: 验证患者风险级别评估正确
2. **目标对齐**: 确保治疗目标与患者风险级别匹配
3. **阶梯式方法**: 验证考虑了阶梯式治疗方法
4. **基线考虑**: 根据基线值预期联合治疗需求
5. **指南版本**: 明确说明使用的指南版本
6. **合并症**: 验证所有合并症均已处理

## 质量保证

### 文档标准

- **完整性**: 所有必需章节均存在
- **SMART目标**: 目标符合具体、可衡量、可实现、相关、有时限标准
- **循证**: 干预措施基于当前临床实践指南
- **以患者为中心**: 计划与患者偏好和临床背景一致
- **隐私合规**: 自动PHI检测和去识别

### 法规合规

- **HIPAA**: 按Safe Harbor方法去识别
- **知情同意**: 记录患者理解和同意
- **医疗必要性**: 文档支持计费要求
- **质量报告**: 支持质量指标提取

## 免责声明

**重要提示：本技能基于当前指南推荐生成AI辅助治疗方案。**

- 最终临床决策、剂量调整和处方权必须由主治医师根据患者个体化情况（如实时肝肾功能指标）核准
- AI生成的治疗方案仅供参考，不替代医生的临床判断和决策
- 医生在做出最终决策时应考虑患者特异性因素、实时实验室指标、药物相互作用、过敏史等因素
- 始终验证指南版本并咨询当前来源，特别是对于快速演进领域

## 许可证

MIT License

## 作者

bbylw

## 版本

指南版本: ADA 2026, ACC/AHA 2024, ESC 2023, NCCN 2026
最后更新: 2026年4月

## 支持

如有问题或疑问，请参阅SKILL.md中的技能文档和references/目录中的参考资料。
