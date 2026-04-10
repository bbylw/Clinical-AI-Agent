---
name: treatment-plans
description: AI-driven medical treatment plan generation skill. Automatically generates evidence-based, guideline-concordant treatment plans using the latest clinical guidelines (ADA 2026, ACC/AHA, ESC, etc.). Supports all clinical specialties with comprehensive medication databases, drug interaction checking, and automated PHI de-identification. Outputs structured Markdown for EHR integration. This is a fully AI-driven skill - the AI model directly generates high-quality treatment plans based on clinical context and current evidence.
allowed-tools: Read Write Edit Bash Search WebBrowsing
license: MIT license
metadata:
    skill-author: K-Dense Inc.
    ai-driven: true
    guideline-version: ADA 2026, ACC/AHA 2024, ESC 2023
---

# AI-Driven Treatment Plan Generation

## Overview

This is a fully AI-driven medical treatment plan generation skill. When loaded, the AI model directly generates evidence-based, guideline-concordant treatment plans using the latest clinical guidelines and medication databases.

**Core Capabilities:**
- **Automatic generation**: AI generates complete treatment plans from clinical notes or case descriptions
- **Latest guidelines**: Incorporates the most current evidence-based guidelines across all specialties (NCCN, ADA, ACC/AHA, ESC, AHA, ACR, AAN, IDSA, APA, AGS, etc.)
- **Guideline verification**: AI model is instructed to verify guideline versions and use the most recent evidence available
- **Medication database**: Comprehensive drug information with dose ranges, interactions, and contraindications
- **Drug interaction checking**: Automated detection of potential drug-drug interactions
- **PHI de-identification**: Built-in privacy protection with context-aware PHI detection
- **EHR integration**: Structured Markdown output compatible with electronic health records

**Critical Principles:**
1. **Latest Evidence-Based**: ALL recommendations MUST be based on the most current evidence-based guidelines available. The AI model is instructed to always use the latest guidelines from authoritative organizations (NCCN, ADA, ACC/AHA, ESC, AHA, ACR, etc.) and to verify guideline versions when uncertain
2. **Patient-Centered**: Plans align with patient preferences, comorbidities, and clinical context
3. **Guideline-Concordant**: Treatment recommendations align with the latest guidelines across all specialties (diabetes, hypertension, cardiology, oncology, respiratory, rheumatology, neurology, infectious disease, psychiatry, geriatrics)
4. **Actionable**: Specific, measurable interventions with clear timelines and monitoring
5. **Privacy-Compliant**: Automatic PHI detection and de-identification for HIPAA compliance

**How to Use:**
Simply provide clinical notes or a case description to the AI. The AI will automatically:
1. Analyze the clinical context
2. Identify diagnoses with ICD-10 codes
3. Generate SMART goals based on patient characteristics and latest guidelines
4. Recommend evidence-based interventions using current standards (ADA 2026, ACC/AHA 2024, ESC 2019)
5. Check for drug interactions and contraindications
6. Create a structured monitoring and follow-up plan
7. Output a complete, ready-to-use treatment plan in Markdown format

**No scripts or external tools required** - this is a pure AI-driven skill. The AI model uses the latest clinical guidelines directly when generating treatment plans.

## When to Use This Skill

This skill should be used when:
- Creating individualized treatment plans for patient care
- Documenting therapeutic interventions for chronic disease management
- Developing rehabilitation programs (physical therapy, occupational therapy, cardiac rehab)
- Writing mental health and psychiatric treatment plans
- Planning perioperative and surgical care pathways
- Establishing pain management protocols
- Setting patient-centered goals using SMART criteria
- Coordinating multidisciplinary care across specialties
- Ensuring regulatory compliance in treatment documentation
- Generating professional treatment plans for medical records

## How This Skill Works

This is a pure AI-driven skill. When loaded, the AI model has access to:

1. **SYSTEM_PROMPT.md**: Contains comprehensive clinical guidelines across all specialties (diabetes, hypertension, cardiology, oncology, respiratory, rheumatology, neurology, infectious disease, psychiatry, geriatrics) with emphasis on the latest evidence-based recommendations (NCCN 2026, ADA 2026, ACC/AHA 2024, ESC 2023, etc.)
2. **Treatment Templates**: Structured Markdown templates in `assets/` directory (one_page_treatment_plan.md, standard_treatment_plan.md)
3. **Reference Materials**: Clinical guidelines and evidence in `references/` directory

**The AI model directly generates treatment plans** by:
- Applying the latest guidelines from SYSTEM_PROMPT.md across all relevant specialties
- Verifying guideline versions and using the most current evidence available
- Using the appropriate template from `assets/`
- Incorporating evidence-based recommendations for the specific clinical scenario
- Ensuring all recommendations align with the latest authoritative guidelines

**No external scripts or tools are required**. The AI model's knowledge combined with the skill's comprehensive guidelines and templates enables direct generation of high-quality, guideline-concordant treatment plans across all medical specialties.

**Commitment to Latest Evidence**: The skill is designed to prioritize the most current evidence-based guidelines. When generating treatment plans, the AI model is instructed to:
- Always use the latest available guidelines from authoritative organizations
- Verify guideline versions when uncertain
- Recommend verification with current sources if there is ambiguity
- Prioritize the most recent evidence when there are conflicting recommendations

**Self-Verification Mechanism**: Before finalizing any treatment plan, the AI model performs a self-verification check to ensure guideline compliance:
- Risk stratification verification
- Target alignment with patient risk level
- Stepwise treatment approach consideration
- Baseline value consideration for combination therapy
- Explicit guideline version documentation
- Comorbidity coverage verification

**Example:**
```
User: 58岁男性，2型糖尿病3年，HbA1c 8.5%，高血压，血压138/88，BMI 28.7，目前服用二甲双胍500mg BID，赖诺普利10mg QD

AI (with treatment-plans skill loaded): [Generates complete treatment plan using ADA 2026 guidelines, recommending SGLT2 inhibitor addition, individualized HbA1c target, appropriate monitoring schedule]
```

## Visual Enhancement (Optional)

**Visual diagrams can enhance treatment plans but are not mandatory.** Consider adding figures for:

- Treatment pathway flowcharts
- Care coordination diagrams
- Therapy progression timelines
- Clinical decision algorithm diagrams
- Any complex concept that benefits from visualization

**How to add diagrams:**
- Embed images using Markdown syntax: `![Description](path/to/image.png)`
- Can use external tools like scientific-schematics skill if available
- Simple ASCII diagrams in Markdown code blocks also work well

---

## Document Format and Best Practices

### Document Length Options

Treatment plans come in three format options based on clinical complexity and use case:

#### Option 1: One-Page Treatment Plan (PREFERRED for most cases)

**When to use**: Straightforward clinical scenarios, standard protocols, busy clinical settings

**Format**: Single page containing all essential treatment information in scannable sections
- No table of contents needed
- No extensive narratives
- Focused on actionable items only
- Similar to precision oncology reports or treatment recommendation cards

**Required sections** (all on one page):
1. **Header Box**: Patient info, diagnosis, date, molecular/risk profile if applicable
2. **Treatment Regimen**: Numbered list of specific interventions
3. **Supportive Care**: Brief bullet points
4. **Rationale**: 1-2 sentence justification (optional for standard protocols)
5. **Monitoring**: Key parameters and frequency
6. **Evidence Level**: Guideline reference or evidence grade (e.g., "Level 1, FDA approved")
7. **Expected Outcome**: Timeline and success metrics

**Design principles**:
- Use small boxes/tables for organization (like the clinical treatment recommendation card format)
- Eliminate all non-essential text
- Use abbreviations familiar to clinicians
- Dense information layout - maximize information per square inch
- Think "quick reference card" not "comprehensive documentation"

**Example structure**:
```markdown
[Patient ID/Diagnosis Box at top]

TARGET PATIENT POPULATION
  Number of patients, demographics, key features

PRIMARY TREATMENT REGIMEN
  • Medication 1: dose, frequency, duration
  • Procedure: specific details
  • Monitoring: what and when

SUPPORTIVE CARE
  • Key supportive medications

RATIONALE
  Brief clinical justification

MOLECULAR TARGETS / RISK FACTORS
  Relevant biomarkers or risk stratification

EVIDENCE LEVEL
  Guideline reference, trial data

MONITORING REQUIREMENTS
  Key labs/vitals, frequency

EXPECTED CLINICAL BENEFIT
  Primary endpoint, timeline
```

#### Option 2: Standard 3-4 Page Format

**When to use**: Moderate complexity, need for patient education materials, multidisciplinary coordination

Uses the Foundation Medicine first-page summary model with 2-3 additional pages of details.

#### Option 3: Extended 5-6 Page Format

**When to use**: Complex comorbidities, research protocols, extensive safety monitoring required

### First Page Summary (Foundation Medicine Model)

**CRITICAL REQUIREMENT: All treatment plans MUST have a complete executive summary on the first page ONLY, before any table of contents or detailed sections.**

Following the Foundation Medicine model for precision medicine reporting and clinical summary documents, treatment plans begin with a one-page executive summary that provides immediate access to key actionable information. This entire summary must fit on the first page.

**Required First Page Structure (in order):**

1. **Title and Subtitle**
   - Main title: Treatment plan type (e.g., "Comprehensive Treatment Plan")
   - Subtitle: Specific condition or focus (e.g., "Type 2 Diabetes Mellitus - Young Adult Patient")

2. **Report Information Box**
   - Report type/document purpose
   - Date of plan creation
   - Patient demographics (age, sex, de-identified)
   - Primary diagnosis with ICD-10 code
   - Report author/clinic (if applicable)
   - Analysis approach or framework used

3. **Key Findings or Treatment Highlights** (2-4 colored boxes using Markdown tables or blockquotes)
   - **Primary Treatment Goals**
     - 2-3 SMART goals in bullet format
   - **Main Interventions**
     - 2-3 key interventions (pharmacological, non-pharmacological, monitoring)
   - **Critical Decision Points** (using warning blockquotes if urgent)
     - Important monitoring thresholds or safety considerations
   - **Timeline Overview**
     - Brief treatment duration/phases
     - Key milestone dates

**Visual Format Requirements:**
- Use Markdown formatting for visual organization
- All content should be concise and scannable
- Use tables, blockquotes, and headers for visual hierarchy
- Boxes should be visually prominent and easy to scan
- Use concise, bullet-point format
- Table of contents (if included) follows the executive summary
- Detailed sections start on page 3

**Example First Page Structure:**
```markdown
# Comprehensive Treatment Plan
# Type 2 Diabetes Mellitus - Young Adult Patient

## Report Information
- Report Type: Treatment Plan
- Date: [Date]
- Patient: [De-identified demographics]
- Diagnosis: Type 2 Diabetes (E11.9)

## Treatment Highlights

### Primary Treatment Goals
- HbA1c <7.0% within 3 months
- Blood pressure <130/80 mmHg
- Weight loss of 5-10%

### Main Interventions
- Metformin 1000mg BID
- ACE inhibitor 10mg daily
- Lifestyle modifications

### Critical Decision Points
- Monitor for hypoglycemia
- Adjust medications based on renal function

### Timeline Overview
- Phase 1: Intensive initiation (4 weeks)
- Phase 2: Adjustment (8 weeks)
- Phase 3: Maintenance (ongoing)

---

[Detailed sections continue on page 2]
```

### Concise Documentation

**CRITICAL: Treatment plans MUST prioritize brevity and clinical relevance. Default to 3-4 pages maximum unless clinical complexity absolutely demands more detail.**

Treatment plans should prioritize **clarity and actionability** over exhaustive detail:

- **Focused**: Include only clinically essential information that impacts care decisions
- **Actionable**: Emphasize what needs to be done, when, and why
- **Efficient**: Facilitate quick decision-making without sacrificing clinical quality
- **Target length options**:
  - **1-page format** (preferred for straightforward cases): Quick-reference card with all essential information
  - **3-4 pages standard**: Standard format with first-page summary + supporting details
  - **5-6 pages** (rare): Only for highly complex cases with multiple comorbidities or multidisciplinary interventions

**Streamlining Guidelines:**
- **First Page Summary**: Use individual colored boxes to consolidate key information (goals, interventions, decision points) - this alone can often convey the essential treatment plan
- **Eliminate Redundancy**: If information is in the first-page summary, don't repeat it verbatim in detailed sections
- **Patient Education section**: 3-5 key bullet points on critical topics and warning signs only
- **Risk Mitigation section**: Highlight only critical medication safety concerns and emergency actions (not exhaustive lists)
- **Expected Outcomes section**: 2-3 concise statements on anticipated responses and timelines
- **Interventions**: Focus on primary interventions; secondary/supportive measures in brief bullet format
- **Use tables and bullet points** extensively for efficient presentation
- **Avoid narrative prose** where structured lists suffice
- **Combine related sections** when appropriate to reduce page count

### Quality Over Quantity

The goal is professional, clinically complete documentation that respects clinicians' time while ensuring comprehensive patient care. Every section should add value; remove or condense sections that don't directly inform treatment decisions.

### Citations and Evidence Support

**Use minimal, targeted citations to support clinical recommendations:**

- **Text Citations Preferred**: Use brief in-text citations (Author Year) or simple references rather than extensive bibliographies unless specifically requested
- **When to Cite**:
  - Clinical practice guideline recommendations (e.g., "per ADA 2024 guidelines")
  - Specific medication dosing or protocols (e.g., "ACC/AHA recommendations")
  - Novel or controversial interventions requiring evidence support
  - Risk stratification tools or validated assessment scales
- **When NOT to Cite**:
  - Standard-of-care interventions widely accepted in the field
  - Basic medical facts and routine clinical practices
  - General patient education content
- **Citation Format**: 
  - Inline: "Initiate metformin as first-line therapy (ADA Standards of Care 2024)"
  - Minimal: "Treatment follows ACC/AHA heart failure guidelines"
  - Avoid formal numbered references and extensive bibliography sections unless document is for academic/research purposes
- **Keep it Brief**: A 3-4 page treatment plan should have 0-3 citations maximum, only where essential for clinical credibility or novel recommendations

## Core Capabilities

### 1. General Medical Treatment Plans

General medical treatment plans address common chronic conditions and acute medical issues requiring structured therapeutic interventions.

#### Standard Components

**Patient Information (De-identified)**
- Demographics (age, sex, relevant medical background)
- Active medical conditions and comorbidities
- Current medications and allergies
- Relevant social and family history
- Functional status and baseline assessments
- **HIPAA Compliance**: Remove all 18 identifiers per Safe Harbor method

**Diagnosis and Assessment Summary**
- Primary diagnosis with ICD-10 code
- Secondary diagnoses and comorbidities
- Severity classification and staging
- Functional limitations and quality of life impact
- Risk stratification (e.g., cardiovascular risk, fall risk)
- Prognostic indicators

**Treatment Goals (SMART Format)**

Short-term goals (1-3 months):
- **Specific**: Clearly defined outcome (e.g., "Reduce HbA1c to <7%")
- **Measurable**: Quantifiable metrics (e.g., "Decrease systolic BP by 10 mmHg")
- **Achievable**: Realistic given patient capabilities
- **Relevant**: Aligned with patient priorities and values
- **Time-bound**: Specific timeframe (e.g., "within 8 weeks")

Long-term goals (6-12 months):
- Disease control or remission targets
- Functional improvement objectives
- Quality of life enhancement
- Prevention of complications
- Maintenance of independence

**Interventions**

*Pharmacological*:
- Medications with specific dosages, routes, frequencies
- Titration schedules and target doses
- Drug-drug interaction considerations
- Monitoring for adverse effects
- Medication reconciliation

*Non-pharmacological*:
- Lifestyle modifications (diet, exercise, smoking cessation)
- Behavioral interventions
- Patient education and self-management
- Monitoring and self-tracking (glucose, blood pressure, weight)
- Assistive devices or adaptive equipment

*Procedural*:
- Planned procedures or interventions
- Referrals to specialists
- Diagnostic testing schedule
- Preventive care (vaccinations, screenings)

**Timeline and Schedule**
- Treatment phases with specific timeframes
- Appointment frequency (weekly, monthly, quarterly)
- Milestone assessments and goal evaluations
- Medication adjustments schedule
- Expected duration of treatment

**Monitoring Parameters**
- Clinical outcomes to track (vital signs, lab values, symptoms)
- Assessment tools and scales (e.g., PHQ-9, pain scales)
- Frequency of monitoring
- Thresholds for intervention or escalation
- Patient-reported outcomes

**Expected Outcomes**
- Primary outcome measures
- Success criteria and benchmarks
- Expected timeline for improvement
- Criteria for treatment modification
- Long-term prognosis

**Follow-up Plan**
- Scheduled appointments and reassessments
- Communication plan (phone calls, secure messaging)
- Emergency contact procedures
- Criteria for urgent evaluation
- Transition or discharge planning

**Patient Education**
- Understanding of condition and treatment rationale
- Self-management skills training
- Medication administration and adherence
- Warning signs and when to seek help
- Resources and support services

**Risk Mitigation**
- Potential adverse effects and management
- Drug interactions and contraindications
- Fall prevention, infection prevention
- Emergency action plans
- Safety monitoring

#### Common Applications

- Diabetes mellitus management
- Hypertension control
- Heart failure treatment
- COPD management
- Asthma care plans
- Hyperlipidemia treatment
- Osteoarthritis management
- Chronic kidney disease

### 2. Rehabilitation Treatment Plans

Rehabilitation plans focus on restoring function, improving mobility, and enhancing quality of life through structured therapeutic programs.

#### Core Components

**Functional Assessment**
- Baseline functional status (ADLs, IADLs)
- Range of motion, strength, balance, endurance
- Gait analysis and mobility assessment
- Standardized measures (FIM, Barthel Index, Berg Balance Scale)
- Environmental assessment (home safety, accessibility)

**Rehabilitation Goals**

*Impairment-level goals*:
- Improve shoulder flexion to 140 degrees
- Increase quadriceps strength by 2/5 MMT grades
- Enhance balance (Berg Score >45/56)

*Activity-level goals*:
- Independent ambulation 150 feet with assistive device
- Climb 12 stairs with handrail supervision
- Transfer bed-to-chair independently

*Participation-level goals*:
- Return to work with modifications
- Resume recreational activities
- Independent community mobility

**Therapeutic Interventions**

*Physical Therapy*:
- Therapeutic exercises (strengthening, stretching, endurance)
- Manual therapy techniques
- Gait training and balance activities
- Modalities (heat, ice, electrical stimulation, ultrasound)
- Assistive device training

*Occupational Therapy*:
- ADL training (bathing, dressing, grooming, feeding)
- Upper extremity strengthening and coordination
- Adaptive equipment and modifications
- Energy conservation techniques
- Cognitive rehabilitation

*Speech-Language Pathology*:
- Swallowing therapy and dysphagia management
- Communication strategies and augmentative devices
- Cognitive-linguistic therapy
- Voice therapy

*Other Services*:
- Recreational therapy
- Aquatic therapy
- Cardiac rehabilitation
- Pulmonary rehabilitation
- Vestibular rehabilitation

**Treatment Schedule**
- Frequency: 3x/week PT, 2x/week OT (example)
- Session duration: 45-60 minutes
- Treatment phase durations (acute, subacute, maintenance)
- Expected total duration: 8-12 weeks
- Reassessment intervals

**Progress Monitoring**
- Weekly functional assessments
- Standardized outcome measures
- Goal attainment scaling
- Pain and symptom tracking
- Patient satisfaction

**Home Exercise Program**
- Specific exercises with repetitions/sets/frequency
- Precautions and safety instructions
- Progression criteria
- Self-monitoring strategies

#### Specialty Rehabilitation

- Post-stroke rehabilitation
- Orthopedic rehabilitation (joint replacement, fracture)
- Cardiac rehabilitation (post-MI, post-surgery)
- Pulmonary rehabilitation
- Vestibular rehabilitation
- Neurological rehabilitation
- Sports injury rehabilitation

### 3. Mental Health Treatment Plans

Mental health treatment plans address psychiatric conditions through integrated psychotherapeutic, pharmacological, and psychosocial interventions.

#### Essential Components

**Psychiatric Assessment**
- Primary psychiatric diagnosis (DSM-5 criteria)
- Symptom severity and functional impairment
- Co-occurring mental health conditions
- Substance use assessment
- Suicide/homicide risk assessment
- Trauma history and PTSD screening
- Social determinants of mental health

**Treatment Goals**

*Symptom reduction*:
- Decrease depression severity (PHQ-9 score from 18 to <10)
- Reduce anxiety symptoms (GAD-7 score <5)
- Improve sleep quality (Pittsburgh Sleep Quality Index)
- Stabilize mood (reduced mood episodes)

*Functional improvement*:
- Return to work or school
- Improve social relationships and support
- Enhance coping skills and emotional regulation
- Increase engagement in meaningful activities

*Recovery-oriented goals*:
- Build resilience and self-efficacy
- Develop crisis management skills
- Establish sustainable wellness routines
- Achieve personal recovery goals

**Therapeutic Interventions**

*Psychotherapy*:
- Evidence-based modality (CBT, DBT, ACT, psychodynamic, IPT)
- Session frequency (weekly, biweekly)
- Treatment duration (12-16 weeks, ongoing)
- Specific techniques and targets
- Group therapy participation

*Psychopharmacology*:
- Medication class and rationale
- Starting dose and titration schedule
- Target symptoms
- Expected response timeline (2-4 weeks for antidepressants)
- Side effect monitoring
- Combination therapy considerations

*Psychosocial Interventions*:
- Case management services
- Peer support programs
- Family therapy or psychoeducation
- Vocational rehabilitation
- Supported housing or community integration
- Substance abuse treatment

**Safety Planning**
- Crisis contacts and emergency services
- Warning signs and triggers
- Coping strategies and self-soothing techniques
- Safe environment modifications
- Means restriction (firearms, medications)
- Support system activation

**Monitoring and Assessment**
- Symptom rating scales (weekly or biweekly)
- Medication adherence and side effects
- Suicidal ideation screening
- Functional status assessments
- Treatment engagement and therapeutic alliance

**Patient and Family Education**
- Psychoeducation about diagnosis
- Treatment rationale and expectations
- Medication information
- Relapse prevention strategies
- Community resources

#### Mental Health Conditions

- Major depressive disorder
- Anxiety disorders (GAD, panic, social anxiety)
- Bipolar disorder
- Schizophrenia and psychotic disorders
- PTSD and trauma-related disorders
- Eating disorders
- Substance use disorders
- Personality disorders

### 4. Chronic Disease Management Plans

Comprehensive long-term care plans for chronic conditions requiring ongoing monitoring, treatment adjustments, and multidisciplinary coordination.

#### Key Features

**Disease-Specific Targets**
- Evidence-based treatment goals per guidelines
- Stage-appropriate interventions
- Complication prevention strategies
- Disease progression monitoring

**Self-Management Support**
- Patient activation and engagement
- Shared decision-making
- Action plans for symptom changes
- Technology-enabled monitoring (apps, remote monitoring)

**Care Coordination**
- Primary care physician oversight
- Specialist consultations and co-management
- Care transitions (hospital to home)
- Medication management across providers
- Communication protocols

**Population Health Integration**
- Registry tracking and outreach
- Preventive care and screening schedules
- Quality measure reporting
- Care gaps identification

#### Applicable Conditions

- Type 1 and Type 2 diabetes
- Cardiovascular disease (CHF, CAD)
- Chronic respiratory diseases (COPD, asthma)
- Chronic kidney disease
- Inflammatory bowel disease
- Rheumatoid arthritis and autoimmune conditions
- HIV/AIDS
- Cancer survivorship care

### 5. Perioperative Care Plans

Structured plans for surgical and procedural patients covering preoperative preparation, intraoperative management, and postoperative recovery.

#### Components

**Preoperative Assessment**
- Surgical indication and planned procedure
- Preoperative risk stratification (ASA class, cardiac risk)
- Optimization of medical conditions
- Medication management (continuation, discontinuation)
- Preoperative testing and clearances
- Informed consent and patient education

**Perioperative Interventions**
- Enhanced recovery after surgery (ERAS) protocols
- Venous thromboembolism prophylaxis
- Antibiotic prophylaxis
- Glycemic control strategies
- Pain management plan (multimodal analgesia)

**Postoperative Care**
- Immediate recovery goals (24-48 hours)
- Early mobilization protocols
- Diet advancement
- Wound care and drain management
- Pain control regimen
- Complication monitoring

**Discharge Planning**
- Activity restrictions and progression
- Medication reconciliation
- Follow-up appointments
- Home health or rehabilitation services
- Return-to-work timeline

### 6. Pain Management Plans

Multimodal approaches to acute and chronic pain using evidence-based interventions and opioid-sparing strategies.

#### Comprehensive Components

**Pain Assessment**
- Pain location, quality, intensity (0-10 scale)
- Temporal pattern (constant, intermittent, breakthrough)
- Aggravating and alleviating factors
- Functional impact (sleep, activities, mood)
- Previous treatments and responses
- Psychosocial contributors

**Multimodal Interventions**

*Pharmacological*:
- Non-opioid analgesics (acetaminophen, NSAIDs)
- Adjuvant medications (antidepressants, anticonvulsants, muscle relaxants)
- Topical agents (lidocaine, capsaicin, diclofenac)
- Opioid therapy (when appropriate, with risk mitigation)
- Titration and rotation strategies

*Interventional Procedures*:
- Nerve blocks and injections
- Radiofrequency ablation
- Spinal cord stimulation
- Intrathecal drug delivery

*Non-pharmacological*:
- Physical therapy and exercise
- Cognitive-behavioral therapy for pain
- Mindfulness and relaxation techniques
- Acupuncture
- TENS units

**Opioid Safety (when prescribed)**
- Indication and planned duration
- Prescription drug monitoring program (PDMP) check
- Opioid risk assessment tools
- Naloxone prescription
- Treatment agreements
- Random urine drug screening
- Frequent follow-up and reassessment

**Functional Goals**
- Specific activity improvements
- Sleep quality enhancement
- Reduced pain interference
- Improved quality of life
- Return to work or meaningful activities

## Best Practices

### Brevity and Focus (HIGHEST PRIORITY)

**Treatment plans MUST be concise and focused on actionable clinical information:**

- **1-page format is PREFERRED**: For most clinical scenarios, a single-page treatment plan (like precision oncology reports) provides all necessary information
- **Default to shortest format possible**: Start with 1-page; only expand if clinical complexity genuinely requires it
- **Every sentence must add value**: If a section doesn't change clinical decision-making, omit it entirely
- **Think "quick reference card" not "comprehensive textbook"**: Busy clinicians need scannable, dense information
- **Avoid academic verbosity**: This is clinical documentation, not a literature review or teaching document
- **Maximum lengths by complexity**:
  - Simple/standard cases: 1 page
  - Moderate complexity: 3-4 pages (first-page summary + details)
  - High complexity (rare): 5-6 pages maximum

### First Page Summary (Most Important)

**ALWAYS create a one-page executive summary as the first page:**
- The first page must contain ONLY: Title, Report Info Box, and Key Findings boxes
- This provides an at-a-glance overview similar to precision medicine reports
- Table of contents and detailed sections start on page 2 or later
- Think of it as a "clinical highlights" page that a busy clinician can scan in 30 seconds
- Use 2-4 colored boxes for different key findings (goals, interventions, decision points)
- **A strong first page can often stand alone** - subsequent pages are for details, not repetition

### SMART Goal Setting

All treatment goals should meet SMART criteria:

- **Specific**: "Improve HbA1c to <7%" not "Better diabetes control"
- **Measurable**: Use quantifiable metrics, validated scales, objective measures
- **Achievable**: Consider patient capabilities, resources, social support
- **Relevant**: Align with patient values, priorities, and life circumstances
- **Time-bound**: Define clear timeframes for goal achievement and reassessment

### Patient-Centered Care

✓ **Shared Decision-Making**: Involve patients in goal-setting and treatment choices  
✓ **Cultural Competence**: Respect cultural beliefs, language preferences, health literacy  
✓ **Patient Preferences**: Honor treatment preferences and personal values  
✓ **Individualization**: Tailor plans to patient's unique circumstances  
✓ **Empowerment**: Support patient activation and self-management  

### Evidence-Based Practice

✓ **Clinical Guidelines**: Follow current specialty society recommendations  
✓ **Quality Measures**: Incorporate HEDIS, CMS quality measures  
✓ **Comparative Effectiveness**: Use treatments with proven efficacy  
✓ **Avoid Low-Value Care**: Eliminate unnecessary tests and interventions  
✓ **Stay Current**: Update plans based on emerging evidence  

### Documentation Standards

✓ **Completeness**: Include all required elements  
✓ **Clarity**: Use clear, professional medical language  
✓ **Accuracy**: Ensure factual correctness and current information  
✓ **Timeliness**: Document plans promptly  
✓ **Legibility**: Professional formatting and organization  
✓ **Signature and Date**: Authenticate all treatment plans  

### Regulatory Compliance

✓ **HIPAA Privacy**: De-identify all protected health information  
✓ **Informed Consent**: Document patient understanding and agreement  
✓ **Billing Support**: Include documentation to support medical necessity  
✓ **Quality Reporting**: Enable extraction of quality metrics  
✓ **Legal Protection**: Maintain defensible clinical documentation  

### Multidisciplinary Coordination

✓ **Team Communication**: Share plans across care team  
✓ **Role Clarity**: Define responsibilities for each team member  
✓ **Care Transitions**: Ensure continuity across settings  
✓ **Specialist Integration**: Coordinate with subspecialty care  
✓ **Patient-Centered Medical Home**: Align with PCMH principles  

## Markdown Template Usage

### Template Selection

Choose the appropriate template based on clinical context and desired length:

#### Concise Templates (PREFERRED)

1. **one_page_treatment_plan.md** - **FIRST CHOICE** for most cases
   - All clinical specialties
   - Standard protocols and straightforward cases
   - Quick-reference format similar to precision oncology reports
   - Dense, scannable, clinician-focused
   - Use this unless complexity demands more detail

#### Standard Templates (3-4 pages)

Use only when one-page format is insufficient due to complexity:

2. **standard_treatment_plan.md** - Primary care, chronic disease, general medicine
   - Comprehensive 11-section structure
   - Suitable for complex cases requiring detailed documentation

**Note**: Even when using standard templates, adapt them to be concise (3-4 pages max) by removing non-essential sections.

### Template Structure

All Markdown templates include:
- Clean, readable formatting with headers and tables
- Structured sections for all required components
- Tables for medications, interventions, timelines
- Goal-tracking sections with SMART criteria
- Space for provider signatures and dates
- HIPAA-compliant de-identification guidance
- Inline comments and instructions

### Converting to Other Formats

**To PDF:**
```bash
# Using Pandoc (recommended)
pandoc treatment_plan.md -o treatment_plan.pdf

# Using Markdown editors
# - Typora: File > Export > PDF
# - VS Code: Markdown PDF extension
# - Online: Dillinger, StackEdit
```

**To HTML:**
```bash
pandoc treatment_plan.md -o treatment_plan.html
```

**For EHR Integration:**
- Copy Markdown content directly into EHR text fields
- Convert to plain text for systems that don't support formatting
- Export tables as CSV if needed for structured data entry

## Validation and Quality Assurance

### Completeness Checking

Use validation scripts to ensure all required sections are present:

```bash
python scripts/check_completeness_md.py my_treatment_plan.md
```

The script checks for:
- Patient information section
- Diagnosis and assessment
- SMART goals (short-term and long-term)
- Interventions (pharmacological, non-pharmacological)
- Timeline and schedule
- Monitoring parameters
- Expected outcomes
- Follow-up plan
- Patient education
- Risk mitigation
- HIPAA de-identification notice
- Provider signature section
- Uncustomized placeholders

### Treatment Plan Validation

**Standard validation** - Basic completeness and quality checks:

```bash
python scripts/validate_treatment_plan_md.py my_treatment_plan.md
```

Validation includes:
- SMART goal criteria assessment
- Evidence-based intervention verification
- Timeline feasibility check
- Monitoring parameter adequacy
- Safety and risk mitigation review
- Regulatory compliance check
- ICD-10 coding verification
- Quantitative metrics assessment

**Enhanced validation** - Semantic understanding with local rules (no external APIs):

```bash
python scripts/validate_enhanced_md.py my_treatment_plan.md
```

Enhanced validation adds:
- **Medication dose合理性检查**: Validates doses against common medication ranges (e.g., metformin 500-2550mg, lisinopril 2.5-80mg)
- **SMART goal语义验证**: Checks if goals are semantically reasonable (has targets, has timeframes, not unrealistic)
- **Clinical target validation**: Compares targets against typical ranges (e.g., HbA1c 6.5-8.0%, BP 120-140/70-90 mmHg)
- **Internal consistency检查**: Ensures diagnosis matches interventions, goals match interventions
- **Unrealistic goal detection**: Flags goals like "HbA1c <5.5%" or "weight loss >10 lbs/week"

**⚠️ Important Scope Limitation**:
The local medication dose validation includes a lightweight knowledge base covering common chronic disease medications (diabetes, hypertension, common antibiotics, pain medications). This is suitable for:
- Primary care and chronic disease management
- Basic medication safety checks
- Demo and small-scale use

**For complex medications, the AI model should perform semantic validation when generating treatment plans**:
- Chemotherapy agents
- Targeted therapies
- Immunotherapy drugs
- Specialized psychiatric medications
- Complex polypharmacy with drug interactions

The local validator cannot scale to thousands of medications and does not include comprehensive drug interaction databases. When the AI model generates treatment plans, it should automatically perform comprehensive validation including drug interaction checking and guideline compliance verification.

### Quality Checklist

Review treatment plans against the quality checklist (`quality_checklist.md`):

**Clinical Quality**
- [ ] Diagnosis is accurate and properly coded (ICD-10)
- [ ] Goals are SMART and patient-centered
- [ ] Interventions are evidence-based and guideline-concordant
- [ ] Timeline is realistic and clearly defined
- [ ] Monitoring plan is comprehensive
- [ ] Safety considerations are addressed

**Patient-Centered Care**
- [ ] Patient preferences and values incorporated
- [ ] Shared decision-making documented
- [ ] Health literacy appropriate language
- [ ] Cultural considerations addressed
- [ ] Patient education plan included

**Regulatory Compliance**
- [ ] HIPAA-compliant de-identification
- [ ] Medical necessity documented
- [ ] Informed consent noted
- [ ] Provider signature and credentials
- [ ] Date of plan creation/revision

**Coordination and Communication**
- [ ] Specialist referrals documented
- [ ] Care team roles defined
- [ ] Follow-up schedule clear
- [ ] Emergency contacts provided
- [ ] Transition planning addressed

## Integration with Other Skills

### Clinical Reports Integration

Treatment plans often accompany other clinical documentation:

- **SOAP Notes** (`clinical-reports` skill): Document ongoing implementation
- **H&P** (`clinical-reports` skill): Initial assessment informs treatment plan
- **Discharge Summaries** (`clinical-reports` skill): Summarize treatment plan execution
- **Progress Notes**: Track goal achievement and plan modifications

### Scientific Writing Integration

Evidence-based treatment planning requires literature support:

- **Citation Management** (`citation-management` skill): Reference clinical guidelines
- **Literature Review** (`literature-review` skill): Understand treatment evidence base
- **Research Lookup** (`research-lookup` skill): Find current best practices

### Research Integration

Treatment plans may be developed for clinical trials or research studies:

- **Research Grants** (`research-grants` skill): Treatment protocols for funded studies
- **Clinical Trial Reports** (`clinical-reports` skill): Intervention documentation

## Common Use Cases

### Example 1: Type 2 Diabetes Management

**Scenario**: 58-year-old patient with newly diagnosed Type 2 diabetes, HbA1c 8.5%, BMI 32

**Template**: `general_medical_treatment_plan.tex`

**Goals**:
- Short-term: Reduce HbA1c to <7.5% in 3 months
- Long-term: Achieve HbA1c <7%, lose 15 pounds in 6 months

**Interventions**:
- Pharmacological: Metformin 500mg BID, titrate to 1000mg BID
- Lifestyle: Mediterranean diet, 150 min/week moderate exercise
- Education: Diabetes self-management education, glucose monitoring

### Example 2: Post-Stroke Rehabilitation

**Scenario**: 70-year-old patient s/p left MCA stroke with right hemiparesis

**Template**: `rehabilitation_treatment_plan.tex`

**Goals**:
- Short-term: Improve right arm strength 2/5 to 3/5 in 4 weeks
- Long-term: Independent ambulation 150 feet with cane in 12 weeks

**Interventions**:
- PT 3x/week: Gait training, balance, strengthening
- OT 3x/week: ADL training, upper extremity function
- SLP 2x/week: Dysphagia therapy

### Example 3: Major Depressive Disorder

**Scenario**: 35-year-old with moderate depression, PHQ-9 score 16

**Template**: `mental_health_treatment_plan.tex`

**Goals**:
- Short-term: Reduce PHQ-9 to <10 in 8 weeks
- Long-term: Achieve remission (PHQ-9 <5), return to work

**Interventions**:
- Psychotherapy: CBT weekly sessions
- Medication: Sertraline 50mg daily, titrate to 100mg
- Lifestyle: Sleep hygiene, exercise 30 min 5x/week

### Example 4: Total Knee Arthroplasty

**Scenario**: 68-year-old scheduled for right TKA for osteoarthritis

**Template**: `perioperative_care_plan.tex`

**Preoperative Goals**:
- Optimize diabetes control (glucose <180)
- Discontinue anticoagulation per protocol
- Complete medical clearance

**Postoperative Goals**:
- Ambulate 50 feet by POD 1
- 90-degree knee flexion by POD 3
- Discharge home with PT services by POD 2-3

### Example 5: Chronic Low Back Pain

**Scenario**: 45-year-old with chronic non-specific low back pain, pain 7/10

**Template**: `pain_management_plan.tex`

**Goals**:
- Short-term: Reduce pain to 4/10 in 6 weeks
- Long-term: Return to work full-time, pain 2-3/10

**Interventions**:
- Pharmacological: Gabapentin 300mg TID, duloxetine 60mg daily
- PT: Core strengthening, McKenzie exercises 2x/week x 8 weeks
- Behavioral: CBT for pain, mindfulness meditation
- Interventional: Consider lumbar ESI if inadequate response

## Professional Standards and Guidelines

Treatment plans should align with:

### General Medicine
- American Diabetes Association (ADA) Standards of Care
- ACC/AHA Cardiovascular Guidelines
- GOLD COPD Guidelines
- JNC-8 Hypertension Guidelines
- KDIGO Chronic Kidney Disease Guidelines

### Rehabilitation
- APTA Clinical Practice Guidelines
- AOTA Practice Guidelines
- Cardiac Rehabilitation Guidelines (AHA/AACVPR)
- Stroke Rehabilitation Guidelines

### Mental Health
- APA Practice Guidelines
- VA/DoD Clinical Practice Guidelines
- NICE Guidelines (National Institute for Health and Care Excellence)
- Cochrane Reviews for psychiatric interventions

### Pain Management
- CDC Opioid Prescribing Guidelines
- AAPM/APS Chronic Pain Guidelines
- WHO Pain Ladder
- Multimodal Analgesia Best Practices

## Timeline Generation

Use the timeline generator script to create visual treatment timelines:

```bash
python timeline_generator.py --plan my_treatment_plan.tex --output timeline.pdf
```

Generates:
- Gantt chart of treatment phases
- Milestone markers for goal assessments
- Medication titration schedules
- Follow-up appointment calendar
- Intervention intensity over time

## Support and Resources

### Template Generation

Interactive template selection:

### Additional Resources

- Clinical practice guidelines from specialty societies
- AHRQ Effective Health Care Program
- Cochrane Library for intervention evidence
- UpToDate and DynaMed for treatment recommendations
- CMS Quality Measures and HEDIS specifications

## Markdown Formatting for Treatment Plans

This skill uses Markdown for treatment plan generation. The AI model directly applies the latest clinical guidelines (ADA 2026, ACC/AHA 2024, ESC 2019) when generating treatment plans in Markdown format.

### Markdown Structure

Treatment plans use standard Markdown formatting:
- **Headers**: `#`, `##`, `###` for hierarchy
- **Tables**: For medication lists, monitoring parameters, timelines
- **Blockquotes**: `>` for critical information, warnings, decision points
- **Lists**: `-` or `*` for bullet points
- **Bold**: `**text**` for emphasis

### Information Boxes

Use Markdown blockquotes with context for organizing clinical information:

#### Info Block (For general information)

```markdown
> **Key Information:**
> - Clinical assessment details
> - Testing schedules
> - General guidance
```

#### Warning Block (For critical information)

```markdown
> **⚠️ Important Safety Information:**
> - Critical drug interactions
> - Safety monitoring requirements
> - Red flag symptoms requiring immediate action
```

#### Goal Block (For treatment goals)

```markdown
> **🎯 Treatment Goals**
> - Reduce HbA1c to <7.0% within 3 months
> - Achieve 5-7% weight loss in 12 weeks
> - Complete diabetes education program
```

### Tables

Use Markdown tables for structured data:

```markdown
| Medication | Dose | Frequency | Purpose |
|------------|------|-----------|---------|
| Metformin | 500mg | BID | Diabetes management |
| Lisinopril | 10mg | QD | Blood pressure control |
| Atorvastatin | 20mg | QN | Lipid management |
```

### Key Points Block

For executive summaries, key takeaways, and important recommendations:

```markdown
> **💡 Key Highlights**
> - Main therapeutic approach
> - Critical patient instructions
> - Priority interventions
```

**Use cases**: Plan overview, plate method instructions, important dietary guidelines

#### Emergency Block

For emergency contacts and urgent protocols:

```markdown
> **🚨 Emergency Contacts**
> - **Emergency Services**: 911
> - **Endocrinology Office**: [Phone] (business hours)
> - **After-Hours Hotline**: [Phone] (nights/weekends)
> - **Pharmacy**: [Phone and location]
```

**Use cases**: Emergency contacts, critical hotlines, urgent resource information

#### Patient Info Block

For patient demographics and baseline information:

```markdown
| **Patient Information** | |
|---|---|
| **Age** | 23 years |
| **Sex** | Male |
| **Diagnosis** | Type 2 Diabetes Mellitus |
| **Plan Start Date** | [Date] |
```

**Use cases**: Patient information sections, demographic data

### Professional Table Formatting

Enhanced table environment with medical styling:

```markdown
| Column 1 | Column 2 | Column 3 |
|----------|----------|----------|
| Data row 1 content | Value 1 | Details 1 |
| Data row 2 content | Value 2 | Details 2 |
| Data row 3 content | Value 3 | Details 3 |

*Table caption*
```

**Features:**
- Clear column headers

4. **Treatment Goals** (SMART format)
   - Short-term goals (1-3 months)
   - Long-term goals (6-12 months)
   - Patient-centered goals

5. **Interventions**
   - Pharmacological interventions with evidence-based rationale
   - Non-pharmacological interventions
   - Monitoring parameters
   - Safety considerations

6. **Timeline and Schedule**
   - Treatment phases
   - Appointment schedule
   - Milestone assessments

7. **Expected Outcomes**
   - Anticipated benefits
   - Success criteria
   - Timeline for improvement

8. **Follow-up Plan**
   - Next appointment
   - Communication plan
   - Emergency protocols

9. **Patient Education**
   - Key educational topics
   - Warning signs
   - Self-management instructions

10. **Provider Signature**
    - Provider information
    - Date
    - Patient acknowledgment (optional)

## Evidence-Based Guidelines

This skill incorporates the latest clinical guidelines:

### Diabetes Management (ADA 2026)
- GLP-1 RAs (semaglutide, liraglutide, tirzepatide) are PREFERRED for patients with established CVD
- SGLT2 inhibitors (empagliflozin, dapagliflozin) are PREFERRED for patients with CKD
- For patients with both CVD and CKD, both GLP-1 RA and SGLT2i can be used together
- Individualized HbA1c targets: <7.0% for general adults, <8.0% for elderly/frail patients

### Hypertension Management (ACC/AHA 2024)
- ACE inhibitors or ARBs are PREFERRED for patients with CAD or CKD
- For 2nd stage hypertension or high-risk factors, INITIAL therapy should consider SINGLE-PILL COMBINATION
- Target BP: <130/80 mmHg (general), <140/90 mmHg (elderly 65-75), <150/90 mmHg (elderly 80+)

### Lipid Management (ACC/AHA 2018/ESC 2019)
- LDL-C target for very high risk (CAD + diabetes): <55 mg/dL (1.4 mmol/L)
- High-intensity statins for very high risk patients

## Skill Architecture

This is a pure AI-driven skill with the following structure:

- **SKILL.md**: Documentation and usage instructions
- **SYSTEM_PROMPT.md**: System prompt containing latest clinical guidelines
- **assets/**: Markdown templates (one_page_treatment_plan.md, standard_treatment_plan.md)
- **references/**: Reference materials and clinical guidelines

The AI model uses the SYSTEM_PROMPT.md and templates to directly generate evidence-based treatment plans without requiring any external scripts or tools.

