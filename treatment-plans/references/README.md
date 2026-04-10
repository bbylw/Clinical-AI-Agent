# Clinical AI Agent

## Overview

AI-driven skill for generating **concise, clinician-focused** medical treatment plans across all clinical specialties. Provides Markdown templates with SMART goal frameworks, evidence-based interventions, regulatory compliance, and validation knowledge for patient-centered care planning.

**Default to 1-page format** for most cases - think "quick reference card" not "comprehensive textbook".

**Pure AI-Driven**: No scripts or external tools required. The AI model directly generates treatment plans using the latest clinical guidelines and Markdown templates.

## What's Included

### 📋 Treatment Plan Types

1. **One-Page Treatment Plan** (PREFERRED) - Concise, quick-reference format for most clinical scenarios
2. **Standard Treatment Plan** - Comprehensive medical care planning for chronic diseases (diabetes, hypertension, heart failure, etc.)

### 📚 Reference Files (5 comprehensive guides)

- `treatment_plan_standards.md` - Professional standards, documentation requirements, legal considerations
- `goal_setting_frameworks.md` - SMART goals, patient-centered outcomes, shared decision-making
- `intervention_guidelines.md` - Evidence-based treatments, pharmacological and non-pharmacological
- `regulatory_compliance.md` - HIPAA compliance, billing documentation, quality measures
- `specialty_specific_guidelines.md` - Detailed guidelines for each treatment plan type

### 📄 Markdown Templates (2 professional templates)

- `one_page_treatment_plan.md` - **FIRST CHOICE** - Dense, scannable 1-page format (like precision oncology reports)
- `standard_treatment_plan.md` - Comprehensive medical care planning

### 🧠 System Prompt (AI Knowledge Base)

- `SYSTEM_PROMPT.md` - Contains the latest clinical guidelines across all specialties (NCCN 2026, ADA 2026, ACC/AHA 2025, ESC/EAS 2025, KDIGO 2024, ACOG 2024, AAP 2023-2024, etc.)

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

**No scripts or external tools required** - this is a pure AI-driven skill. The AI model uses the latest clinical guidelines directly when generating treatment plans.

## Standard Treatment Plan Components

All templates include these essential sections:

### 1. Patient Information (De-identified)
- Demographics and relevant medical background
- Active conditions and comorbidities
- Current medications and allergies
- Functional status baseline
- HIPAA-compliant de-identification

### 2. Diagnosis and Assessment Summary
- Primary diagnosis (ICD-10 coded)
- Secondary diagnoses
- Severity classification
- Functional limitations
- Risk stratification

### 3. Treatment Goals (SMART Format)

**Short-term goals** (1-3 months):
- Specific, measurable outcomes
- Realistic targets with defined timeframes
- Patient-centered priorities

**Long-term goals** (6-12 months):
- Disease control targets
- Functional improvement objectives
- Quality of life enhancement
- Complication prevention

### 4. Interventions

- **Pharmacological**: Medications with dosages, frequencies, monitoring
- **Non-pharmacological**: Lifestyle modifications, behavioral interventions, education
- **Procedural**: Planned procedures, specialist referrals, diagnostic testing

### 5. Timeline and Schedule
- Treatment phases with timeframes
- Appointment frequency
- Milestone assessments
- Expected treatment duration

### 6. Monitoring Parameters
- Clinical outcomes to track
- Assessment tools and scales
- Monitoring frequency
- Intervention thresholds

### 7. Expected Outcomes
- Primary outcome measures
- Success criteria
- Timeline for improvement
- Long-term prognosis

### 8. Follow-up Plan
- Scheduled appointments
- Communication protocols
- Emergency procedures
- Transition planning

### 9. Patient Education
- Condition understanding
- Self-management skills
- Warning signs
- Resources and support

### 10. Risk Mitigation
- Adverse effect management
- Safety monitoring
- Emergency action plans
- Fall/infection prevention

## Common Use Cases

### 1. Type 2 Diabetes Management

```
Goal: Create comprehensive treatment plan for newly diagnosed diabetes

Template: standard_treatment_plan.md

Key Components:
- SMART goals: HbA1c <7% in 3 months, weight loss 10 lbs in 6 months
- Medications: Metformin titration schedule
- Lifestyle: Diet, exercise, glucose monitoring
- Monitoring: HbA1c every 3 months, quarterly visits
- Education: Diabetes self-management education
```

### 2. Post-Stroke Rehabilitation

```
Goal: Develop rehab plan for stroke patient with hemiparesis

Template: standard_treatment_plan.md

Key Components:
- Functional assessment: FIM scores, ROM, strength testing
- PT goals: Ambulation 150 feet with cane in 12 weeks
- OT goals: Independent ADLs, upper extremity function
- Treatment schedule: PT/OT/SLP 3x week each
- Home exercise program
```

### 3. Major Depressive Disorder

```
Goal: Create integrated treatment plan for depression

Template: standard_treatment_plan.md

Key Components:
- Assessment: PHQ-9 score 16 (moderate depression)
- Goals: Reduce PHQ-9 to <5, return to work in 12 weeks
- Psychotherapy: CBT weekly sessions
- Medication: SSRI with titration schedule
- Safety planning: Crisis contacts, warning signs
```

### 4. Total Knee Replacement

```
Goal: Perioperative care plan for elective TKA

Template: standard_treatment_plan.md

Key Components:
- Preop optimization: Medical clearance, medication management
- ERAS protocol implementation
- Postop milestones: Ambulation POD 1, discharge POD 2-3
- Pain management: Multimodal analgesia
- Rehab plan: PT starting POD 0
```

### 5. Chronic Low Back Pain

```
Goal: Multimodal pain management plan

Template: standard_treatment_plan.md

Key Components:
- Pain assessment: Location, intensity, functional impact
- Goals: Reduce pain 7/10 to 3/10, return to work
- Medications: Non-opioid analgesics, adjuvants
- PT: Core strengthening, McKenzie exercises
- Behavioral: CBT for pain, mindfulness
- Interventional: Consider ESI if inadequate response
```

## SMART Goals Framework

All treatment plans use SMART criteria for goal-setting:

- **Specific**: Clear, well-defined outcome (not vague)
- **Measurable**: Quantifiable metrics or observable behaviors
- **Achievable**: Realistic given patient capabilities and resources
- **Relevant**: Aligned with patient priorities and values
- **Time-bound**: Specific timeframe for achievement

### Examples

**Good SMART Goals**:
- Reduce HbA1c from 8.5% to <7% within 3 months
- Walk independently 150 feet with assistive device by 8 weeks
- Decrease PHQ-9 depression score from 18 to <10 in 8 weeks
- Achieve knee flexion >90 degrees by postoperative day 14
- Reduce pain from 7/10 to ≤4/10 within 6 weeks

**Poor Goals** (not SMART):
- "Feel better" (not specific or measurable)
- "Improve diabetes" (not specific or time-bound)
- "Get stronger" (not measurable)
- "Return to normal" (vague, not specific)

## Workflow Examples

### Standard Treatment Plan Workflow

1. **Provide clinical notes** - Give the AI patient history, physical, diagnostic testing
2. **AI generates plan** - AI automatically selects appropriate template and generates treatment plan
3. **Review and customize** - Review AI-generated plan, customize as needed
4. **Set SMART goals** - AI generates measurable short and long-term goals based on guidelines
5. **Specify interventions** - AI recommends evidence-based pharmacological and non-pharmacological interventions
6. **Create timeline** - AI schedules appointments, milestones, reassessments
7. **Define monitoring** - AI specifies outcome measures and assessment frequency
8. **Review with patient** - Shared decision-making, confirm understanding
9. **Implement and document** - Execute plan, track progress in clinical notes
10. **Reassess and modify** - Adjust plan based on outcomes

### Multidisciplinary Care Plan Workflow

1. **Identify team members** - PCP, specialists, therapists, case manager
2. **Provide comprehensive notes** - Include all consultant recommendations
3. **AI generates integrated plan** - AI integrates input across disciplines
4. **Coordinate goals** - Ensure alignment across disciplines
5. **Define communication** - Team meeting schedule, documentation sharing
6. **Assign responsibilities** - Clarify who manages each intervention
7. **Create care timeline** - AI coordinates appointments across providers
8. **Share plan** - Distribute to all team members and patient
9. **Track collectively** - Shared monitoring and outcome tracking
10. **Regular team review** - Adjust plan collaboratively

## Best Practices

### Patient-Centered Care
✓ Involve patients in goal-setting and decision-making  
✓ Respect cultural beliefs and language preferences  
✓ Address health literacy with appropriate language  
✓ Align plan with patient values and life circumstances  
✓ Support patient activation and self-management  

### Evidence-Based Practice
✓ Follow current clinical practice guidelines  
✓ Use interventions with proven efficacy  
✓ Incorporate quality measures (HEDIS, CMS)  
✓ Avoid low-value or ineffective interventions  
✓ Update plans based on emerging evidence  

### Regulatory Compliance
✓ De-identify per HIPAA Safe Harbor method (18 identifiers)  
✓ Document medical necessity for billing support  
✓ Include informed consent documentation  
✓ Sign and date all treatment plans  
✓ Maintain professional documentation standards  

### Quality Documentation
✓ Complete all required sections  
✓ Use clear, professional medical language  
✓ Include specific, measurable goals  
✓ Specify exact medications (dose, route, frequency)  
✓ Define monitoring parameters and frequency  
✓ Address safety and risk mitigation  

### Care Coordination
✓ Communicate plan to entire care team  
✓ Define roles and responsibilities  
✓ Coordinate across care settings  
✓ Integrate specialist recommendations  
✓ Plan for care transitions  

## Integration with Other Skills

### Clinical Reports
- **SOAP Notes**: Document treatment plan implementation and progress
- **H&P Documents**: Initial assessment informs treatment planning
- **Discharge Summaries**: Summarize treatment plan execution
- **Progress Notes**: Track goal achievement and plan modifications

### Scientific Writing
- **Citation Management**: Reference clinical practice guidelines
- **Literature Review**: Understand evidence base for interventions
- **Research Lookup**: Find current treatment recommendations

### Research
- **Research Grants**: Treatment protocols for clinical trials
- **Clinical Trial Reports**: Document trial interventions

## Clinical Practice Guidelines

Treatment plans should align with evidence-based guidelines:

### General Medicine
- American Diabetes Association (ADA) Standards of Care
- ACC/AHA Cardiovascular Guidelines
- GOLD COPD Guidelines
- AHA/ACC 2025 Hypertension Guidelines
- KDIGO Chronic Kidney Disease Guidelines

### Rehabilitation
- APTA Physical Therapy Clinical Practice Guidelines
- AOTA Occupational Therapy Practice Guidelines
- AHA/AACVPR Cardiac Rehabilitation Guidelines
- Stroke Rehabilitation Best Practices

### Mental Health
- APA (American Psychiatric Association) Practice Guidelines
- VA/DoD Clinical Practice Guidelines for Mental Health
- NICE Guidelines (UK)
- Evidence-based psychotherapy protocols (CBT, DBT, ACT)

### Pain Management
- CDC Opioid Prescribing Guidelines
- AAPM (American Academy of Pain Medicine) Guidelines
- WHO Analgesic Ladder
- Multimodal Analgesia Best Practices

### Perioperative Care
- ERAS (Enhanced Recovery After Surgery) Society Guidelines
- ASA Perioperative Guidelines
- SCIP (Surgical Care Improvement Project) Measures

## Professional Standards

### Documentation Requirements
- Complete and accurate patient information
- Clear diagnosis with appropriate ICD-10 coding
- Evidence-based interventions
- Measurable goals and outcomes
- Defined monitoring and follow-up
- Provider signature, credentials, and date

### Medical Necessity
Treatment plans must demonstrate:
- Medical appropriateness of interventions
- Alignment with diagnosis and severity
- Evidence supporting treatment choices
- Expected outcomes and benefit
- Frequency and duration justification

### Legal Considerations
- Informed consent documentation
- Patient understanding and agreement
- Risk disclosure and mitigation
- Professional liability protection
- Compliance with state/federal regulations

## Support and Resources

### Getting Help

1. **Check reference files** - Comprehensive guidance in `references/` directory
2. **Review templates** - See example structures in `assets/` directory
3. **Run validation scripts** - Identify issues with automated tools
4. **Consult SKILL.md** - Detailed documentation and best practices
5. **Review quality checklist** - Ensure all quality criteria met

### External Resources

- Clinical practice guidelines from specialty societies
- UpToDate and DynaMed for treatment recommendations
- AHRQ Effective Health Care Program
- Cochrane Library for intervention evidence
- CMS Quality Measures and HEDIS specifications
- HEDIS (Healthcare Effectiveness Data and Information Set)

### Professional Organizations

- American Medical Association (AMA)
- American Academy of Family Physicians (AAFP)
- Specialty society guidelines (ADA, ACC, AHA, APA, etc.)
- Joint Commission standards
- Centers for Medicare & Medicaid Services (CMS)

## Frequently Asked Questions

### How do I choose the right template?

Match the template to your primary clinical focus:
- **Quick reference format** → one_page_treatment_plan.md (PREFERRED for most cases)
- **Comprehensive format** → standard_treatment_plan.md (for complex cases)

### What if my patient has multiple conditions?

Use the standard_treatment_plan.md template for complex multimorbidity. The AI will integrate all relevant conditions into a comprehensive plan.

### How often should treatment plans be updated?

- **Initial creation**: At diagnosis or treatment initiation
- **Regular updates**: Every 3-6 months for chronic conditions
- **Significant changes**: When goals are met or treatment is modified
- **Annual review**: Minimum for all chronic disease plans

### Can I modify the Markdown templates?

Yes! Templates are designed to be customized. Modify sections, add specialty-specific content, or adjust formatting to meet your needs.

### How do I ensure HIPAA compliance?

- Remove all 18 HIPAA identifiers (see Safe Harbor method)
- Use age ranges instead of exact ages (e.g., "60-65" not "63")
- Remove specific dates, use relative timelines
- Omit geographic identifiers smaller than state
- The AI model automatically detects and flags PHI for de-identification

### What if the AI-generated plan needs adjustments?

Review the specific areas that need modification, consult reference files for guidance, and provide feedback to the AI for regeneration. Common adjustments include:
- Missing required sections
- Goals not meeting SMART criteria
- Insufficient monitoring parameters
- Incomplete medication information
- Need for specialty-specific content

## License

Part of the Claude Scientific Writer project. See main LICENSE file.

---

For detailed documentation, see `SKILL.md`. For issues or questions, consult the comprehensive reference files in the `references/` directory.

