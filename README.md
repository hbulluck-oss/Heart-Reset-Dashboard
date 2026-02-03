# Heart Reset Dashboard - Quick Assessment

A cardiovascular risk assessment tool designed to help individuals understand their cardiovascular health profile through evidence-based screening questions. **No lab results or measurements required.**

## Overview

The Heart Reset Dashboard is a quick, accessible cardiovascular risk screener that requires no lab work or physical measurements. It runs entirely in the browser with **zero data collection** - all processing happens locally on the user's device.

Perfect for:
- General public health screening
- Initial cardiovascular risk awareness
- People without recent lab results
- Quick self-assessment before medical consultation

## Features

- 🔒 **Privacy-First**: No data storage, transmission, or tracking
- 📊 **Evidence-Based Scoring**: Calibrated risk assessment based on cardiovascular research
- ⚡ **Quick Assessment**: Only 14 questions, 3-5 minutes to complete
- 🎨 **Professional Design**: Clean, accessible interface with traffic light visualization
- 📱 **Fully Responsive**: Works on desktop, tablet, and mobile devices
- 💻 **No Dependencies**: Pure HTML/CSS/JavaScript - no frameworks required
- 🚫 **No Measurements Needed**: Based on health status awareness, not lab values

## Assessment Details

**Total Questions: 14**
**Estimated Time: 3-5 minutes**
**Prerequisites: None** (assumes no previous cardiovascular disease)

### Question Sections

#### 1. Personal & Family History (4 questions)
- Age
- Gender
- Ethnicity
- Family history of heart disease

#### 2. Metabolic Health (3 questions)
- Have you ever been told your blood pressure is high or borderline?
- Have you been told you have pre-diabetes or diabetes?
- Would you consider yourself overweight, borderline, or normal weight?

#### 3. Lifestyle (7 questions)
- Smoking status
- Weekly exercise (moderate activity)
- Daily fruit and vegetable servings
- Weekly oily fish intake
- Weekly alcohol consumption
- Stress level
- Nightly sleep duration

## Risk Categories

The assessment provides one of four results:

### 🟢 Green (Low Risk) - <20%
Your cardiovascular baseline load is low. This reflects a low level of strain on your cardiovascular system. Focus on maintaining healthy habits and regular monitoring to lock in these gains for decades to come.

**Typical Actions:**
- Continue current healthy lifestyle patterns
- Annual health check-ups
- Consider optimization strategies

### 🟡 Amber (Moderate Risk) - 20-40%
Your cardiovascular system is accumulating strain. You're at a critical juncture where changes may be beneficial before they become more significant. Many of these factors may be modifiable with the right approach.

**Typical Actions:**
- Consider comprehensive cardiovascular health check within 2-4 weeks
- Begin addressing modifiable risk factors systematically
- Explore working with a preventive cardiology specialist

### 🔴 Red (High Risk) - ≥40%
Your cardiovascular system is carrying high baseline load. This is not meant to alarm you, but to emphasize that seeking medical guidance may be important. Many of these risk factors can potentially be managed effectively with professional medical evaluation and treatment.

**Typical Actions:**
- Recommended: Book GP appointment within 7 days for comprehensive evaluation
- Document all symptoms, medications, and family history
- Consider structured cardiovascular risk management program

### ⚪ Grey (Indeterminate)
Key health parameters are unknown (blood pressure, diabetes status, or weight status marked as "Do not know"). A basic health check is needed before an accurate cardiovascular risk assessment can be provided.

**Typical Actions:**
- Schedule basic health check with GP
- Get blood pressure checked (free at most pharmacies)
- Ask about diabetes screening
- Discuss healthy weight targets with healthcare provider
- Retake assessment once you have this information

## Scoring System

### Maximum Points: 183

The assessment uses a calibrated point system across multiple categories:

**Non-Modifiable Factors:**
- **Age** (0-15 points): ≥65: 15, 55-64: 10, 45-54: 6, 35-44: 3
- **Ethnicity** (0-8 points): South Asian/Middle Eastern: 8, African/Afro-Caribbean: 6
- **Family History** (0-18 points): Both parents: 18, One parent: 10, Sibling(s): 15, Multiple: 22

**Modifiable Factors:**
- **Blood Pressure Status** (0-24 points): High: 24, Borderline: 12
- **Diabetes Status** (0-24 points): Diabetes: 24, Pre-diabetes: 12
- **Weight Status** (0-16 points): Overweight: 16, Borderline: 8
- **Lifestyle Factors** (0-60 points, capped): Combined score from smoking, exercise, diet, oily fish, alcohol, stress, and sleep

**Final Score Calculation:**
```
Percentage = (Total Points / 183) × 100
```

**Risk Thresholds:**
- Green: <20% (< 37 points)
- Amber: 20-40% (37-73 points)
- Red: ≥40% (≥ 73 points)
- Grey: Key data unknown

## Key Design Principles

### 1. Accessibility Over Precision
Designed for people who don't have recent lab results or access to measurements. Uses health status awareness rather than numerical values.

### 2. Non-Modifiable vs Modifiable Risk Factors
The assessment clearly separates factors you cannot change (age, ethnicity, genetics) from those you can (lifestyle, metabolic health). Results display these separately to focus attention appropriately.

### 3. Calibrated Thresholds
- Non-modifiable factors alone should NOT trigger AMBER risk
- AMBER requires accumulation of both non-modifiable and modifiable factors
- RED requires multiple serious modifiable risk factors

### 4. Protective Indeterminate Category
Shows GREY (Indeterminate) when users don't know their basic health status, preventing false reassurance and encouraging baseline health awareness.

### 5. No Previous CVD Assumption
This assessment assumes the user does not have previous cardiovascular disease (heart attack, angina, heart failure, etc.). Those with existing CVD should be under medical supervision.

## Installation & Usage

### Quick Start

1. Download `heart-reset-assessment-v2.html`

2. Open the HTML file in any modern web browser (Chrome, Firefox, Safari, Edge)

3. Complete the 14-question assessment (3-5 minutes)

4. Review your results and recommended actions

### Deployment Options

This is a standalone HTML file that can be:
- Hosted on any web server
- Embedded in existing websites (iframe or direct integration)
- Distributed as a downloadable file
- Shared via email or cloud storage links
- Used completely offline

**No server-side processing or database required.**

## Technical Details

### Technology Stack
- Pure HTML5
- CSS3 (Flexbox, CSS Grid, custom properties)
- Vanilla JavaScript (ES6+)
- Zero external dependencies

### Browser Compatibility
- Chrome/Edge 90+
- Firefox 88+
- Safari 14+
- Mobile browsers (iOS Safari, Chrome Mobile)

### File Size
- Single file: ~45KB
- Zero external requests
- Instant loading

### Performance
- No network requests after initial load
- All calculations client-side
- Fully functional offline
- Mobile-optimized

## Privacy & Security

### Data Protection
- ✅ **Zero data collection**: No analytics, tracking, or telemetry
- ✅ **Local processing only**: All calculations happen in the browser
- ✅ **No external requests**: No API calls or third-party services
- ✅ **No cookies**: No persistent storage or session tracking
- ✅ **No form submission**: Results never leave the user's device

### User Privacy Notice
The assessment displays a prominent privacy notice:
> "🔒 Privacy Notice: Your responses are processed locally in your browser and are NOT stored, transmitted, or saved anywhere."

## Medical Disclaimer

### Important Notice

This assessment is for **educational and guidance purposes only**. It:

- ❌ Is NOT a substitute for professional medical advice
- ❌ Is NOT a diagnostic tool
- ❌ Is NOT a predictor of heart attack risk
- ❌ Should NOT be used for emergency medical situations

**Results should not be interpreted as medical diagnosis.**

This tool reflects current cardiovascular load relative to an ideal baseline - it is not a prediction of heart attack risk, but a signal of how much strain your cardiovascular system is carrying.

**Always consult your physician regarding cardiovascular health questions.**

**If experiencing chest pain, severe breathlessness, or other acute symptoms, seek immediate medical attention.**

## Clinical Background

### Developed By
**Dr. Heeraj Bulluck, MBBS, PhD**
- Consultant Interventional Cardiologist at Leeds Teaching Hospitals
- 120+ cardiovascular publications
- Creator of the Heart Reset Accelerator program
- Author of "Heart Reset 40: The Modern Guide to Preventing Heart Disease"

### Evidence Base
The scoring system is informed by:
- Cardiovascular risk assessment guidelines (ACC/AHA, ESC)
- Framingham Risk Score principles
- QRISK3 cardiovascular risk algorithm
- Evidence from randomized controlled trials on modifiable risk factors
- Clinical experience in preventive cardiology

### R.E.S.E.T. Framework
This assessment supports the R.E.S.E.T. framework for cardiovascular disease prevention:
- **R**outines - Establishing consistent healthy habits
- **E**ating - Evidence-based nutrition for heart health
- **S**leep - Optimizing sleep duration and quality
- **E**xercise - Regular physical activity
- **T**racking - Monitoring key cardiovascular metrics

## Use Cases

### For Individuals
- Quick cardiovascular health check
- Motivation for lifestyle changes
- Preparation for medical consultation
- Tracking improvement over time (retake after lifestyle changes)

### For Healthcare Providers
- Patient education tool
- Initial screening before detailed assessment
- Lifestyle counseling framework
- Engagement tool for preventive cardiology programs

### For Wellness Programs
- Corporate health screening
- Community health initiatives
- Health insurance wellness programs
- Fitness center health assessments

## Related Resources

### Heart Reset 40 Book
Comprehensive guide to preventing heart disease featuring the R.E.S.E.T. framework.
[Available on Amazon](https://amzn.eu/d/dfy7f2d)

### Free Strategy Call
Book a 1:1 consultation with Dr. Heeraj Bulluck to discuss your cardiovascular health.
[Book Appointment](https://stan.store/drheerajbulluck/p/book-a-11-heart-reset-call)

### Heart Reset Accelerator
Structured program for busy professionals (ages 35-65) focused on cardiovascular disease prevention.

## Frequently Asked Questions

### Why don't you ask for exact cholesterol numbers?
This is designed as a **quick screening tool** accessible to everyone, including those without recent lab work. For detailed metabolic assessment, consult your healthcare provider.

### How accurate is this assessment?
The scoring is calibrated based on established cardiovascular risk factors, but it provides a **general risk profile** rather than precise risk prediction. It should complement, not replace, professional medical evaluation.

### Can I retake the assessment?
Yes! Retaking after lifestyle changes can help track improvement. Each assessment is independent with no stored data.

### What if I get a Red (High Risk) result?
Don't panic. This indicates you should seek professional medical evaluation within the next week. Many risk factors are manageable with proper medical care and lifestyle changes.

### What if all my answers are "Do not know"?
The assessment will show Grey (Indeterminate) and recommend getting a basic health check. Knowing your blood pressure, diabetes status, and weight is essential for cardiovascular risk awareness.

### Is this a substitute for seeing a doctor?
**No.** This is an educational tool. Always consult healthcare professionals for medical advice, diagnosis, or treatment decisions.

## Version History

### V2.0 (February 2026)
- Quick assessment version released
- 14 questions, 3-5 minutes completion time
- Removed all lab measurement requirements
- Simplified metabolic health to status-based questions
- Added indeterminate category for unknown health status
- Redesigned welcome page (removed warning icon, added assumption note)
- Recalibrated scoring for 183-point system
- Implemented protective "Do not know" handling

## Technical Support

### Common Issues

**Assessment won't load:**
- Ensure JavaScript is enabled in your browser
- Try a different modern browser
- Check if pop-up blockers are interfering

**Results don't display:**
- Complete all required questions
- Check browser console for errors (F12)
- Ensure you're using a supported browser

**Mobile display issues:**
- Rotate device to portrait orientation
- Zoom out if elements are cut off
- Update mobile browser to latest version

## Contributing

This is proprietary software. For collaboration inquiries, please contact Dr. Heeraj Bulluck through the official channels listed above.

## License

© 2026 Dr. Heeraj Bulluck. All rights reserved.

This software is proprietary and developed for the Heart Reset Accelerator program. Unauthorized distribution, modification, or commercial use is prohibited.

## Acknowledgments

Special thanks to the cardiovascular research community for the decades of evidence that makes evidence-based risk assessment possible.

---

**For Medical Emergencies**: If you experience chest pain, severe breathlessness, arm/jaw pain, or other acute cardiovascular symptoms, **call emergency services immediately (999/911)**. Do not rely on this assessment tool for emergency situations.
