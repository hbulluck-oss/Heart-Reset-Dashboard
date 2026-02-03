(https://github.com/user-attachments/files/25053131/heart-reset-dashboard.html)
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Heart Reset Dashboard | Dr. Heeraj Bulluck</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, sans-serif;
            line-height: 1.6;
            color: #333;
            background: linear-gradient(135deg, #FFF4E6 0%, #FFE4CC 100%);
            min-height: 100vh;
            padding: 20px;
        }

        .container {
            max-width: 900px;
            margin: 0 auto;
            padding: 2rem 0;
        }

        .card {
            background: white;
            border-radius: 16px;
            box-shadow: 0 10px 40px rgba(0,0,0,0.1);
            padding: 2rem;
            margin-bottom: 2rem;
        }

        /* Header */
        .header {
            text-align: center;
            margin-bottom: 2rem;
        }

        .header-icon {
            width: 64px;
            height: 64px;
            margin: 0 auto 1rem;
            background: #ee6b01;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 32px;
        }

        .header h1 {
            font-size: 2.5rem;
            color: #5C2E0D;
            margin-bottom: 0.5rem;
        }

        .header p {
            font-size: 1.2rem;
            color: #666;
        }

        /* Disclaimer */
        .disclaimer {
            background: white;
            border: 3px solid #ee6b01;
            border-radius: 16px;
            padding: 2rem;
        }

        .disclaimer-header {
            display: flex;
            align-items: flex-start;
            gap: 1rem;
            margin-bottom: 1.5rem;
        }

        .warning-icon {
            width: 48px;
            height: 48px;
            background: #ee6b01;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 24px;
            flex-shrink: 0;
        }

        .disclaimer h2 {
            color: #5C2E0D;
            font-size: 1.8rem;
            margin-bottom: 1rem;
        }

        .disclaimer p {
            margin-bottom: 1rem;
            color: #333;
            line-height: 1.8;
        }

        .privacy-notice {
            background: #E3F2FD;
            border: 2px solid #2196F3;
            border-radius: 12px;
            padding: 1.5rem;
            margin: 1.5rem 0;
            text-align: center;
        }

        .privacy-notice p {
            color: #0D47A1;
            font-weight: 600;
            margin: 0;
        }

        /* Progress Bar */
        .progress-container {
            margin-bottom: 2rem;
        }

        .progress-label {
            display: flex;
            justify-content: space-between;
            margin-bottom: 0.5rem;
            font-size: 0.9rem;
            color: #666;
        }

        .progress-bar {
            width: 100%;
            height: 12px;
            background: #E0E0E0;
            border-radius: 10px;
            overflow: hidden;
        }

        .progress-fill {
            height: 100%;
            background: linear-gradient(90deg, #ee6b01 0%, #ee6b01 100%);
            transition: width 0.3s ease;
            border-radius: 10px;
            box-shadow: 0 2px 8px rgba(255, 140, 0, 0.3);
        }

        /* Section Title */
        .section-title {
            font-size: 0.9rem;
            font-weight: 600;
            color: #ee6b01;
            margin-bottom: 0.5rem;
            text-transform: uppercase;
            letter-spacing: 0.5px;
        }

        /* Question */
        .question-title {
            font-size: 1.8rem;
            font-weight: 700;
            color: #5C2E0D;
            margin-bottom: 1.5rem;
        }

        /* Options */
        .options {
            display: flex;
            flex-direction: column;
            gap: 0.75rem;
        }

        .option-btn {
            width: 100%;
            padding: 1.25rem;
            text-align: left;
            background: white;
            border: 3px solid #E0E0E0;
            border-radius: 12px;
            font-size: 1rem;
            cursor: pointer;
            transition: all 0.2s;
            color: #333;
            font-weight: 500;
        }

        .option-btn:hover {
            border-color: #ee6b01;
            background: #FFF8F0;
        }

        .option-btn.selected {
            border-color: #ee6b01;
            background: #FFF4E6;
            font-weight: 600;
        }

        .option-btn.multiselect {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .checkmark {
            color: #ee6b01;
            font-size: 1.2rem;
        }

        /* Number Input */
        .number-input {
            width: 100%;
            padding: 1.25rem;
            border: 3px solid #E0E0E0;
            border-radius: 12px;
            font-size: 1.1rem;
            transition: border-color 0.2s;
        }

        .number-input:focus {
            outline: none;
            border-color: #ee6b01;
        }

        .input-hint {
            margin-top: 0.5rem;
            font-size: 0.9rem;
            color: #666;
        }

        /* Navigation Buttons */
        .nav-buttons {
            display: flex;
            gap: 1rem;
            margin-top: 2rem;
        }

        .btn {
            padding: 1rem 2rem;
            border: none;
            border-radius: 12px;
            font-size: 1rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.2s;
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
            justify-content: center;
        }

        .btn-primary {
            flex: 1;
            background: linear-gradient(135deg, #ee6b01 0%, #ee6b01 100%);
            color: white;
            box-shadow: 0 3px 10px rgba(255, 140, 0, 0.3);
        }

        .btn-primary:hover:not(:disabled) {
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(255, 140, 0, 0.4);
            background: linear-gradient(135deg, #d66001 0%, #d66001 100%);
        }

        .btn-primary:disabled {
            opacity: 0.5;
            cursor: not-allowed;
        }

        .btn-secondary {
            background: #F5F5F5;
            color: #666;
        }

        .btn-secondary:hover {
            background: #E0E0E0;
        }

        .btn-skip {
            flex: 1;
            background: #F5F5F5;
            color: #666;
        }

        .btn-restart {
            background: #424242;
            color: white;
            padding: 1rem 2rem;
        }

        .btn-restart:hover {
            background: #303030;
        }

        /* Results */
        .results {
            text-align: center;
        }

        .traffic-light {
            width: 150px;
            height: 150px;
            margin: 2rem auto;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 4rem;
            box-shadow: 0 10px 30px rgba(0,0,0,0.2);
        }

        .traffic-light.green {
            background: #4CAF50;
            color: white;
        }

        .traffic-light.amber {
            background: #FF9800;
            color: white;
        }

        .traffic-light.red {
            background: #F44336;
            color: white;
        }

        .traffic-light.grey {
            background: #9E9E9E;
            color: white;
        }

        .result-title {
            font-size: 2.5rem;
            font-weight: 700;
            color: #5C2E0D;
            margin: 1rem 0 0.5rem;
        }

        .result-subtitle {
            font-size: 1.5rem;
            color: #666;
            margin-bottom: 2rem;
        }

        .result-section {
            background: #F9F9F9;
            border-radius: 12px;
            padding: 2rem;
            margin: 1.5rem 0;
            text-align: left;
        }

        .result-section h3 {
            color: #5C2E0D;
            font-size: 1.5rem;
            margin-bottom: 1rem;
        }

        .result-section ul {
            list-style: none;
            padding: 0;
        }

        .result-section li {
            padding: 0.75rem 0;
            border-bottom: 1px solid #E0E0E0;
            display: flex;
            gap: 1rem;
        }

        .result-section li:last-child {
            border-bottom: none;
        }

        .risk-factors {
            background: #FFF4E6;
            border: 2px solid #ee6b01;
        }

        .risk-factors h3 {
            color: #D84315;
        }

        .risk-factors li {
            color: #D84315;
        }

        .actions {
            background: #E3F2FD;
            border: 2px solid #2196F3;
        }

        .actions h3 {
            color: #1565C0;
        }

        .actions li {
            color: #1976D2;
        }

        .actions .missing-data {
            color: #D32F2F;
            font-weight: 600;
        }

        .missing-params {
            background: #FFF3E0;
            border: 2px solid #FF9800;
        }

        .missing-params h3 {
            color: #E65100;
        }

        .missing-params li {
            color: #F57C00;
        }

        .projected-risk-section {
            background: #FFF9C4;
            border: 2px solid #FBC02D;
            border-radius: 12px;
            padding: 2rem;
            margin: 2rem 0;
            text-align: center;
        }

        .projected-risk-section h3 {
            color: #F57F17;
            margin-bottom: 1rem;
        }

        .projected-risk-section p {
            color: #827717;
            margin-bottom: 1.5rem;
            line-height: 1.6;
        }

        .caveat {
            background: #FFECB3;
            border-left: 4px solid #FFA000;
            padding: 1rem;
            margin: 1rem 0;
            font-size: 0.9rem;
            color: #E65100;
            font-weight: 600;
            text-align: left;
        }

        .reveal-btn {
            background: #ee6b01;
            color: white;
            padding: 1rem 2rem;
            border: none;
            border-radius: 12px;
            font-size: 1rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.2s;
        }

        .reveal-btn:hover {
            background: #d66001;
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(255, 140, 0, 0.3);
        }

        .projected-results {
            margin-top: 2rem;
            padding-top: 2rem;
            border-top: 2px solid #FFA000;
        }

        .timeline {
            background: #FFF9C4;
            border-left: 4px solid #ee6b01;
            padding: 1.5rem;
            border-radius: 8px;
            font-style: italic;
            margin: 1.5rem 0;
        }

        .cta-box {
            background: linear-gradient(135deg, #B71C1C 0%, #C62828 100%);
            color: white;
            border-radius: 12px;
            padding: 2.5rem;
            text-align: center;
            margin: 2rem 0;
            box-shadow: 0 4px 20px rgba(183, 28, 28, 0.3);
        }

        .cta-box h3 {
            font-size: 2rem;
            margin-bottom: 1rem;
            color: white;
            text-shadow: 0 2px 4px rgba(0,0,0,0.2);
        }

        .cta-box p {
            font-size: 1.1rem;
            margin-bottom: 1.5rem;
            color: rgba(255, 255, 255, 0.95);
        }

        .cta-btn {
            display: inline-block;
            background: white;
            color: #B71C1C;
            padding: 1rem 2rem;
            border-radius: 12px;
            font-weight: 700;
            font-size: 1.1rem;
            text-decoration: none;
            transition: all 0.2s;
            box-shadow: 0 4px 12px rgba(0,0,0,0.15);
        }

        .cta-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 6px 20px rgba(0,0,0,0.25);
            background: #FFF8F0;
        }

        .book-cta {
            background: linear-gradient(135deg, #FFF4E6 0%, #FFE4CC 100%);
            border: 3px solid #ee6b01;
            color: #5C2E0D;
            box-shadow: 0 4px 20px rgba(255, 140, 0, 0.2);
        }

        .book-cta h3 {
            color: #D84315;
            margin-bottom: 1rem;
            font-size: 1.5rem;
        }

        .book-cta p {
            margin-bottom: 1rem;
            color: #5C2E0D;
        }

        .book-cta .cta-btn {
            background: linear-gradient(135deg, #ee6b01 0%, #ee6b01 100%);
            color: white;
            box-shadow: 0 4px 12px rgba(255, 140, 0, 0.3);
        }

        .book-cta .cta-btn:hover {
            background: linear-gradient(135deg, #d66001 0%, #d66001 100%);
        }

        .footer-text {
            text-align: center;
            color: #666;
            font-size: 0.9rem;
            margin-top: 1.5rem;
        }

        .hidden {
            display: none;
        }

        @media (max-width: 600px) {
            .header h1 {
                font-size: 1.8rem;
            }

            .question-title {
                font-size: 1.4rem;
            }

            .nav-buttons {
                flex-direction: column;
            }
        }
    </style>
</head>
<body>
    <div class="container" id="app">
        <!-- Content will be rendered here by JavaScript -->
    </div>

    <script>
        // State management
        let state = {
            showDisclaimer: true,
            currentSection: 0,
            currentQuestion: 0,
            answers: {},
            showResults: false
        };

        // Assessment data
        const sections = [
            {
                title: "Personal and Family History",
                questions: [
                    { id: 'age', text: 'What is your age?', type: 'number' },
                    { id: 'gender', text: 'What is your gender?', type: 'select', options: ['Male', 'Female'] },
                    { id: 'ethnicity', text: 'What is your ethnicity?', type: 'select', options: ['White European', 'South Asian', 'East Asian', 'Middle Eastern', 'African/Afro-Caribbean', 'Hispanic/Latino', 'Other'] },
                    { id: 'familyHistory', text: 'Family history of heart disease before age 60?', type: 'select', options: ['No', 'Yes - one parent', 'Yes - both parents', 'Yes - sibling(s)', 'Multiple family members'] }
                ]
            },
            {
                title: "Metabolic Health",
                questions: [
                    { id: 'knowWaist', text: 'Do you know your waist circumference?', type: 'select', options: ['Yes', 'No'] },
                    { id: 'waistUnit', text: 'Choose your preferred unit for waist measurement', type: 'select', options: ['cm', 'inches'], conditional: (a) => a.knowWaist === 'Yes' },
                    { id: 'waist', text: 'Enter your waist circumference', type: 'number', conditional: (a) => a.knowWaist === 'Yes' },
                    { id: 'knowCholesterol', text: 'Do you know your cholesterol levels?', type: 'select', options: ['Yes', 'No'] },
                    { id: 'cholesterolUnit', text: 'Choose unit for cholesterol', type: 'select', options: ['mmol/L', 'mg/dL'], conditional: (a) => a.knowCholesterol === 'Yes' },
                    { id: 'totalCholesterol', text: 'Total cholesterol', type: 'number', conditional: (a) => a.knowCholesterol === 'Yes', skip: true },
                    { id: 'ldl', text: 'LDL cholesterol', type: 'number', conditional: (a) => a.knowCholesterol === 'Yes', skip: true },
                    { id: 'hdl', text: 'HDL cholesterol', type: 'number', conditional: (a) => a.knowCholesterol === 'Yes', skip: true },
                    { id: 'triglycerides', text: 'Triglycerides', type: 'number', conditional: (a) => a.knowCholesterol === 'Yes', skip: true },
                    { id: 'knowHbA1c', text: 'Do you know your HbA1c level?', type: 'select', options: ['Yes', 'No'] },
                    { id: 'hba1cUnit', text: 'Choose unit for HbA1c', type: 'select', options: ['mmol/mol', '%'], conditional: (a) => a.knowHbA1c === 'Yes' },
                    { id: 'hba1c', text: 'HbA1c level', type: 'number', conditional: (a) => a.knowHbA1c === 'Yes', skip: true },
                    { id: 'bloodPressure', text: 'What is your typical blood pressure?', type: 'select', options: ['Less than 120/80', '120-129/80-84', '130-139/85-89', '140-159/90-99', '160+/100+', 'Do not know'] }
                ]
            },
            {
                title: "Lifestyle",
                questions: [
                    { id: 'smoking', text: 'Smoking status?', type: 'select', options: ['Never', 'Ex-smoker 5+ years', 'Ex-smoker recent', 'Current light', 'Current heavy'] },
                    { id: 'exercise', text: 'Moderate exercise per week? (brisk walking, cycling, swimming, dancing)', type: 'select', options: ['Under 30 min', '30-75 min', '75-150 min', '150-300 min', 'Over 300 min'] },
                    { id: 'diet', text: 'How many servings of vegetables and fruits do you eat daily?', type: 'select', options: ['0-1 servings', '2-3 servings', '4-5 servings', '6-7 servings', '8+ servings'] },
                    { id: 'oilyFish', text: 'How many portions of oily fish (salmon, mackerel, sardines) do you eat per week?', type: 'select', options: ['None', '1 portion', '2 portions', '3+ portions'] },
                    { id: 'alcohol', text: 'How many units of alcohol do you consume per week? (1 pint beer = 2 units, 175ml wine = 2 units, single spirit = 1 unit)', type: 'select', options: ['None', '1-7 units', '8-14 units', '15-21 units', '22+ units'] },
                    { id: 'stress', text: 'Stress level?', type: 'select', options: ['Low', 'Moderate', 'High', 'Very high', 'Overwhelming'] },
                    { id: 'sleep', text: 'Hours of sleep?', type: 'select', options: ['Under 5', '5-6', '6-7', '7-8', 'Over 8'] }
                ]
            },
            {
                title: "Medical History",
                questions: [
                    { id: 'heartCondition', text: 'Heart condition?', type: 'select', options: ['No', 'Arrhythmia', 'Heart attack', 'Angina', 'Heart failure', 'Other'] },
                    { id: 'medications', text: 'Medications?', type: 'multiselect', options: ['None', 'BP med', 'Statin', 'Diabetes med', 'Blood thinner', 'Other cardiac'] },
                    { id: 'otherConditions', text: 'Other conditions?', type: 'multiselect', options: ['None', 'Kidney', 'Liver', 'Autoimmune', 'Sleep apnea', 'PCOS', 'ED'] }
                ]
            }
        ];

        // Calculate risk score
        function calculateScore() {
            let t = 0, m = 0;
            const r = []; // High-risk factors (flagged)
            const suboptimal = []; // All parameters that scored points
            const missing = [];
            const age = parseInt(state.answers.age) || 0;
            
            // AGE SCORING
            if (age >= 65) { t += 15; r.push('Age 65+'); } 
            else if (age >= 55) { t += 10; r.push('Age 55-64'); } 
            else if (age >= 45) { t += 6; suboptimal.push('Age 45-54'); } 
            else if (age >= 35) { t += 3; suboptimal.push('Age 35-44'); }
            m += 15;
            
            // GENDER (used as modifier)
            const male = state.answers.gender === 'Male';
            m += 2;
            
            // ETHNICITY SCORING - Reduced weight
            if (['South Asian', 'Middle Eastern'].includes(state.answers.ethnicity)) { 
                t += 8; r.push('High-risk ethnicity'); 
            } else if (state.answers.ethnicity === 'African/Afro-Caribbean') { 
                t += 6; r.push('Ethnic risk'); 
            }
            m += 12;
            
            // FAMILY HISTORY SCORING - Reduced weight
            const fm = { 'No': 0, 'Yes - one parent': 10, 'Yes - both parents': 18, 'Yes - sibling(s)': 15, 'Multiple family members': 22 };
            const fs = fm[state.answers.familyHistory] || 0;
            t += fs; 
            if (fs >= 10) r.push('Family history');
            m += 30;
            
            // WAIST CIRCUMFERENCE SCORING
            let w = 0;
            if (state.answers.knowWaist === 'No' || !state.answers.knowWaist) {
                missing.push('Measure your waist circumference');
                m += 15;
            } else if (state.answers.knowWaist === 'Yes' && state.answers.waist) {
                w = parseFloat(state.answers.waist) || 0;
                if (w > 0 && state.answers.waistUnit === 'inches') w *= 2.54;
                if (w > 0) { 
                    if ((male && w >= 102) || (!male && w >= 88)) { 
                        t += 15; r.push('High waist circumference'); 
                    } else if ((male && w >= 94) || (!male && w >= 80)) { 
                        t += 8; suboptimal.push('Elevated waist circumference'); 
                    } 
                }
                m += 15;
            }
            
            // CHOLESTEROL SCORING WITH LIPID CAP
            let lipidPoints = 0;
            if (state.answers.knowCholesterol === 'No') {
                missing.push('Get your cholesterol levels checked');
                m += 60; // Capped maximum for lipids
            } else if (state.answers.knowCholesterol === 'Yes') {
                let tc = parseFloat(state.answers.totalCholesterol) || 0;
                let ldl = parseFloat(state.answers.ldl) || 0;
                let hdl = parseFloat(state.answers.hdl) || 0;
                let tg = parseFloat(state.answers.triglycerides) || 0;
                
                if (state.answers.cholesterolUnit === 'mg/dL') { 
                    tc /= 38.67; 
                    ldl /= 38.67; 
                    hdl /= 38.67; 
                    tg /= 88.57; 
                }
                
                // LDL scoring (max 15)
                if (ldl >= 4.9) { lipidPoints += 15; r.push('Very high LDL cholesterol'); } 
                else if (ldl >= 4.1) { lipidPoints += 10; r.push('High LDL cholesterol'); } 
                else if (ldl >= 3.4) { lipidPoints += 5; suboptimal.push('Borderline LDL cholesterol'); }
                
                // HDL scoring - PENALTY ONLY (max 18)
                if (hdl > 0) { 
                    if (male) { 
                        if (hdl < 0.9) { lipidPoints += 18; r.push('Very low HDL cholesterol'); } 
                        else if (hdl < 1.0) { lipidPoints += 10; suboptimal.push('Low HDL cholesterol'); }
                    } else { 
                        if (hdl < 1.1) { lipidPoints += 18; r.push('Very low HDL cholesterol'); } 
                        else if (hdl < 1.3) { lipidPoints += 10; suboptimal.push('Low HDL cholesterol'); }
                    } 
                }
                
                // Triglycerides scoring (max 15)
                if (tg >= 5.6) { lipidPoints += 15; r.push('Very high triglycerides'); } 
                else if (tg >= 2.3) { lipidPoints += 10; r.push('High triglycerides'); } 
                else if (tg >= 1.7) { lipidPoints += 5; suboptimal.push('Borderline triglycerides'); }
                
                // TC/HDL ratio scoring (max 12)
                const ratio = hdl > 0 ? tc / hdl : 0;
                if (ratio >= 6) { lipidPoints += 12; r.push('Poor cholesterol ratio'); } 
                else if (ratio >= 5) { lipidPoints += 8; r.push('Elevated cholesterol ratio'); } 
                else if (ratio >= 4) { lipidPoints += 4; suboptimal.push('Borderline cholesterol ratio'); }
                
                // CAP TOTAL LIPID CONTRIBUTION AT 60 POINTS
                lipidPoints = Math.min(60, lipidPoints);
                t += lipidPoints;
                m += 60;
            }
            
            // HbA1c SCORING
            if (state.answers.knowHbA1c === 'No') {
                missing.push('Get your HbA1c tested');
                m += 18;
            } else if (state.answers.knowHbA1c === 'Yes' && state.answers.hba1c) {
                let hba = parseFloat(state.answers.hba1c) || 0;
                if (state.answers.hba1cUnit === '%' && hba > 0 && hba < 20) hba = (hba - 2.15) * 10.929;
                if (hba >= 48) { t += 18; r.push('Diabetes range HbA1c'); } 
                else if (hba >= 42) { t += 12; r.push('Pre-diabetes range HbA1c'); } 
                else if (hba >= 39) { t += 6; suboptimal.push('Borderline HbA1c'); }
                m += 18;
            }
            
            // BLOOD PRESSURE SCORING
            const bpMap = { 
                'Less than 120/80': 0, 
                '120-129/80-84': 6, 
                '130-139/85-89': 12, 
                '140-159/90-99': 20, 
                '160+/100+': 28 
            };
            const bps = bpMap[state.answers.bloodPressure] || 0;
            
            if (state.answers.bloodPressure === 'Do not know') {
                missing.push('Check your blood pressure');
                m += 28;
            } else {
                if (bps >= 20) r.push('High blood pressure'); 
                else if (bps >= 12) suboptimal.push('Elevated blood pressure');
                else if (bps >= 6) suboptimal.push('Borderline blood pressure');
                t += bps; 
                m += 28;
            }
            
            // LIFESTYLE FACTORS WITH SOFT CAP
            let lifestylePoints = 0;
            
            // Smoking
            const sm = { 
                'Never': 0, 
                'Ex-smoker 5+ years': 4, 
                'Ex-smoker recent': 10, 
                'Current light': 20, 
                'Current heavy': 28 
            };
            const sms = sm[state.answers.smoking] || 0;
            if (sms >= 20) r.push('Current smoker'); 
            else if (sms >= 10) suboptimal.push('Recent ex-smoker');
            else if (sms >= 4) suboptimal.push('Ex-smoker (5+ years)');
            lifestylePoints += sms;
            
            // Exercise
            const ex = { 
                'Under 30 min': 12, 
                '30-75 min': 8, 
                '75-150 min': 4, 
                '150-300 min': 0, 
                'Over 300 min': 0 
            };
            const exs = ex[state.answers.exercise] || 0;
            if (exs >= 12) r.push('Very low physical activity'); 
            else if (exs >= 8) suboptimal.push('Low physical activity');
            else if (exs >= 4) suboptimal.push('Below recommended physical activity');
            lifestylePoints += exs;
            
            // Diet
            const dt = { 
                '0-1 servings': 10, 
                '2-3 servings': 6, 
                '4-5 servings': 2, 
                '6-7 servings': 0, 
                '8+ servings': 0 
            };
            const dts = dt[state.answers.diet] || 0;
            if (dts >= 10) r.push('Very low fruit/vegetable intake');
            else if (dts >= 6) suboptimal.push('Low fruit/vegetable intake');
            else if (dts >= 2) suboptimal.push('Below optimal fruit/vegetable intake');
            lifestylePoints += dts;
            
            // Oily Fish
            const fish = { 
                'None': 8, 
                '1 portion': 4, 
                '2 portions': 0, 
                '3+ portions': -2 
            };
            const fishScore = fish[state.answers.oilyFish] || 0;
            if (fishScore >= 8) r.push('No omega-3 rich fish intake');
            else if (fishScore >= 4) suboptimal.push('Low omega-3 rich fish intake');
            lifestylePoints += fishScore;
            
            // Alcohol
            const alc = { 
                'None': 0, 
                '1-7 units': 0, 
                '8-14 units': 4, 
                '15-21 units': 8, 
                '22+ units': 12 
            };
            const alcScore = alc[state.answers.alcohol] || 0;
            if (alcScore >= 12) r.push('Very high alcohol intake');
            else if (alcScore >= 8) r.push('High alcohol intake');
            else if (alcScore >= 4) suboptimal.push('Moderate alcohol intake');
            lifestylePoints += alcScore;
            
            // Stress
            const st = { 
                'Low': 0, 
                'Moderate': 4, 
                'High': 8, 
                'Very high': 12, 
                'Overwhelming': 16 
            };
            const sts = st[state.answers.stress] || 0;
            if (sts >= 12) r.push('Very high stress levels'); 
            else if (sts >= 8) suboptimal.push('High stress levels');
            else if (sts >= 4) suboptimal.push('Moderate stress levels');
            lifestylePoints += sts;
            
            // Sleep
            const sl = { 
                'Under 5': 10, 
                '5-6': 6, 
                '6-7': 2, 
                '7-8': 0, 
                'Over 8': 4 
            };
            const sls = sl[state.answers.sleep] || 0;
            if (sls >= 10) r.push('Severely inadequate sleep');
            else if (sls >= 6) suboptimal.push('Inadequate sleep duration');
            else if (sls >= 4) suboptimal.push('Excessive sleep duration');
            else if (sls >= 2) suboptimal.push('Slightly suboptimal sleep');
            lifestylePoints += sls;
            
            // CAP LIFESTYLE CONTRIBUTION AT 60 POINTS
            lifestylePoints = Math.min(60, lifestylePoints);
            t += lifestylePoints;
            m += 60;
            
            // HEART CONDITION SCORING (DYNAMIC DENOMINATOR)
            const hc = { 
                'No': 0, 
                'Arrhythmia': 15, 
                'Heart attack': 35, 
                'Angina': 25, 
                'Heart failure': 35, 
                'Other': 20 
            };
            const hcs = hc[state.answers.heartCondition] || 0;
            if (hcs >= 15) r.push(state.answers.heartCondition); 
            t += hcs;
            // Only add to denominator if condition exists
            if (state.answers.heartCondition && state.answers.heartCondition !== 'No') {
                m += 35;
            }
            
            // MEDICATIONS (DYNAMIC DENOMINATOR)
            if (state.answers.medications && Array.isArray(state.answers.medications)) {
                const medCount = state.answers.medications.filter(x => x !== 'None').length;
                if (medCount > 0) {
                    t += medCount * 4;
                    m += 20; // Only add if on medications
                    suboptimal.push(`On ${medCount} cardiovascular medication(s)`);
                }
            }
            
            // OTHER CONDITIONS (DYNAMIC DENOMINATOR)
            if (state.answers.otherConditions && Array.isArray(state.answers.otherConditions)) {
                const hr = ['Kidney', 'Sleep apnea', 'PCOS', 'ED'];
                const hasHighRisk = state.answers.otherConditions.some(c => hr.includes(c));
                if (hasHighRisk) { 
                    t += 10; 
                    r.push('Metabolic risk condition');
                    m += 10; // Only add if condition exists
                }
            }
            
            const p = m > 0 ? (t / m) * 100 : 0;
            let level, color, msg, actions;
            
            // Separate modifiable and non-modifiable risk factors
            const nonModifiable = [];
            const modifiable = [];
            
            // Categorize risk factors
            r.forEach(factor => {
                const nonModifiableFactors = ['Age 65+', 'Age 55-64', 'High-risk ethnicity', 'Ethnic risk', 'Family history'];
                if (nonModifiableFactors.includes(factor)) {
                    nonModifiable.push(factor);
                } else {
                    modifiable.push(factor);
                }
            });
            
            // Check if critical data is missing
            const criticalDataMissing = missing.length > 0;
            
            if (criticalDataMissing) {
                level = 'INDETERMINATE';
                color = 'grey';
                msg = 'Your assessment is incomplete. Several key cardiovascular risk markers are missing, which prevents us from providing an accurate risk assessment. This score reflects your current cardiovascular load relative to an ideal baseline – it is not a prediction of heart attack risk, but a signal of how much strain your system is carrying.';
                actions = [
                    'Schedule a comprehensive health check with your GP to measure missing parameters',
                    'Get your waist circumference measured (or measure it yourself)',
                    'Request a full lipid panel (total cholesterol, LDL, HDL, triglycerides)',
                    'Have your HbA1c tested to assess glucose metabolism',
                    'Check your blood pressure (home monitor or pharmacy)',
                    'Once you have these values, retake this assessment for an accurate risk profile'
                ];
            } else if (p < 20) {
                level = 'LOW RISK';
                color = 'green';
                msg = 'Your cardiovascular risk assessment suggests you\'re in the low-risk category. This reflects a low baseline cardiovascular load – your system is not carrying significant strain. While this is encouraging, it doesn\'t mean you can be complacent. This is the optimal time to strengthen your heart health and maintain these gains for decades to come.';
                actions = [
                    'Continue your current exercise routine and aim to gradually increase intensity',
                    'Maintain healthy eating patterns with focus on whole foods',
                    'Keep stress levels manageable through regular relaxation practices',
                    'Schedule annual health check-ups to monitor key metrics',
                    'Consider advanced optimization strategies to maximize longevity'
                ];
            } else if (p < 40) {
                level = 'MODERATE RISK';
                color = 'amber';
                msg = 'Your assessment suggests moderate cardiovascular risk factors that may require attention. You\'re at a critical juncture – your system appears to be accumulating cardiovascular strain. These patterns suggest that changes may be beneficial before they become more significant. The encouraging news is that many of these factors may be modifiable with the right approach.';
                actions = [
                    'Consider scheduling a comprehensive cardiovascular health check with your GP within 2-4 weeks',
                    'Explore implementing the R.E.S.E.T. framework - focus on one pillar at a time',
                    'Consider tracking key metrics (blood pressure, weight, activity) regularly',
                    'You may benefit from working with a preventive cardiology specialist for personalized guidance',
                    'Address potentially modifiable risk factors systematically over the next 3-6 months'
                ];
            } else {
                level = 'HIGH RISK';
                color = 'red';
                msg = 'Your assessment suggests significant cardiovascular risk factors that likely require professional medical evaluation. Your system appears to be carrying a high baseline cardiovascular load. This is not meant to alarm you, but to emphasize that seeking medical guidance may be important. Many of these risk factors can potentially be managed effectively with professional medical evaluation and treatment.';
                actions = [
                    'RECOMMENDED: Book an appointment with your GP within the next 7 days for comprehensive evaluation',
                    'If experiencing chest pain, severe breathlessness, or other acute symptoms, seek immediate medical care',
                    'Prepare for your appointment by documenting all symptoms, medications, and family history',
                    'Early intervention may significantly improve outcomes',
                    'Once medically cleared, consider beginning a structured cardiovascular rehabilitation program'
                ];
            }
            
            // Don't add missing data to actions if already indeterminate
            if (!criticalDataMissing && missing.length > 0) {
                actions = [...missing, ...actions];
            }
            
            // Combine high-risk and suboptimal factors for comprehensive display
            const allFactors = [...r, ...suboptimal];
            
            // Calculate projected risk assuming missing values are normal
            let projectedRisk = null;
            if (criticalDataMissing) {
                const projectedTotal = t;
                const projectedMax = m;
                const projectedPercent = projectedMax > 0 ? (projectedTotal / projectedMax) * 100 : 0;
                
                let projLevel, projColor, projMsg;
                if (projectedPercent < 20) {
                    projLevel = 'LOW RISK';
                    projColor = 'green';
                    projMsg = 'If your missing parameters are within normal ranges, your cardiovascular baseline load would likely be low. However, this is speculative and cannot replace actual measurements.';
                } else if (projectedPercent < 40) {
                    projLevel = 'MODERATE RISK';
                    projColor = 'amber';
                    projMsg = 'If your missing parameters are within normal ranges, your cardiovascular system would likely be carrying moderate strain. However, this is speculative and cannot replace actual measurements.';
                } else {
                    projLevel = 'HIGH RISK';
                    projColor = 'red';
                    projMsg = 'Even assuming your missing parameters are normal, your cardiovascular system would likely be carrying high baseline load due to other identified risk factors. Professional medical evaluation is strongly recommended.';
                }
                
                projectedRisk = {
                    level: projLevel,
                    color: projColor,
                    message: projMsg,
                    percentage: projectedPercent.toFixed(1)
                };
            }
            
            return { level, color, message: msg, riskFactors: allFactors, highRiskFactors: r, suboptimalFactors: suboptimal, actions, missingData: missing, projectedRisk };
        }
        function getCurrentQuestions() {
            return sections[state.currentSection].questions.filter(q => 
                !q.conditional || q.conditional(state.answers)
            );
        }

        // Render functions
        function renderDisclaimer() {
            return `
                <div class="header">
                    <div class="header-icon">❤️</div>
                    <h1>Heart Reset Dashboard</h1>
                </div>
                <div class="card disclaimer">
                    <div class="disclaimer-header">
                        <div class="warning-icon">⚠️</div>
                        <div>
                            <h2>Important Notice</h2>
                        </div>
                    </div>
                    <p><strong>This assessment is for educational and guidance purposes only.</strong> Not a substitute for professional medical advice.</p>
                    <p>Results are based on general principles and should not be interpreted as medical diagnosis.</p>
                    <p><strong>Always consult your physician</strong> regarding cardiovascular health questions.</p>
                    <p>If experiencing chest pain or concerning symptoms, seek immediate medical attention.</p>
                    
                    <div class="privacy-notice">
                        <p>🔒 Privacy Notice: Your responses are processed locally in your browser and are NOT stored, transmitted, or saved anywhere.</p>
                    </div>
                    
                    <div style="text-align: center;">
                        <button class="btn btn-primary" onclick="continueFromDisclaimer()">
                            I Understand - Continue →
                        </button>
                    </div>
                    <p class="footer-text">Dr. Heeraj Bulluck, Consultant Interventional Cardiologist</p>
                </div>
            `;
        }

        function renderQuestion() {
            const questions = getCurrentQuestions();
            const question = questions[state.currentQuestion];
            const answer = state.answers[question.id];
            
            const totalQuestions = sections.reduce((sum, section) => 
                sum + section.questions.filter(q => !q.conditional || q.conditional(state.answers)).length, 0
            );
            const completedQuestions = sections.slice(0, state.currentSection).reduce((sum, section) => 
                sum + section.questions.filter(q => !q.conditional || q.conditional(state.answers)).length, 0
            ) + state.currentQuestion;
            const progress = (completedQuestions / totalQuestions) * 100;
            
            let questionHTML = '';
            
            if (question.type === 'select') {
                questionHTML = `
                    <div class="options">
                        ${question.options.map(option => `
                            <button class="option-btn ${answer === option ? 'selected' : ''}" 
                                    onclick="selectOption('${question.id}', '${option}')">
                                ${option}
                            </button>
                        `).join('')}
                    </div>
                `;
            } else if (question.type === 'multiselect') {
                const selected = answer || [];
                questionHTML = `
                    <div class="options">
                        ${question.options.map(option => `
                            <button class="option-btn multiselect ${selected.includes(option) ? 'selected' : ''}" 
                                    onclick="toggleMultiselect('${question.id}', '${option}')">
                                <span>${option}</span>
                                ${selected.includes(option) ? '<span class="checkmark">✓</span>' : ''}
                            </button>
                        `).join('')}
                    </div>
                `;
            } else if (question.type === 'number') {
                let hint = '';
                if (question.id === 'waist' && state.answers.waistUnit) {
                    hint = `<div class="input-hint">Unit: ${state.answers.waistUnit}</div>`;
                } else if (['totalCholesterol', 'ldl', 'hdl', 'triglycerides'].includes(question.id) && state.answers.cholesterolUnit) {
                    hint = `<div class="input-hint">Unit: ${state.answers.cholesterolUnit}</div>`;
                } else if (question.id === 'hba1c' && state.answers.hba1cUnit) {
                    hint = `<div class="input-hint">Unit: ${state.answers.hba1cUnit}</div>`;
                }
                
                questionHTML = `
                    <input type="text" 
                           class="number-input" 
                           id="numberInput"
                           value="${answer || ''}" 
                           placeholder="Enter value"
                           oninput="handleNumberInput('${question.id}', this.value)"
                           inputmode="decimal">
                    ${hint}
                `;
            }
            
            const isLastQuestion = state.currentSection === sections.length - 1 && 
                                  state.currentQuestion === questions.length - 1;
            const canGoBack = state.currentSection > 0 || state.currentQuestion > 0;
            
            return `
                <div class="header">
                    <div class="header-icon">❤️</div>
                    <h1>Heart Reset Dashboard</h1>
                    <p>Discover your cardiovascular risk profile</p>
                </div>
                <div class="card">
                    <div class="progress-container">
                        <div class="progress-label">
                            <span>Progress</span>
                            <span>${completedQuestions} of ${totalQuestions}</span>
                        </div>
                        <div class="progress-bar">
                            <div class="progress-fill" style="width: ${progress}%"></div>
                        </div>
                    </div>
                    
                    <div class="section-title">
                        Section ${state.currentSection + 1} of ${sections.length}: ${sections[state.currentSection].title}
                    </div>
                    
                    <h2 class="question-title">${question.text}</h2>
                    
                    ${questionHTML}
                    
                    <div class="nav-buttons">
                        ${canGoBack ? '<button class="btn btn-secondary" onclick="goBack()">← Back</button>' : ''}
                        ${question.skip ? '<button class="btn btn-skip" onclick="skipQuestion()">Skip</button>' : ''}
                        <button class="btn btn-primary" 
                                onclick="goNext()" 
                                id="nextBtn"
                                ${!answer && !question.skip ? 'disabled' : ''}>
                            ${isLastQuestion ? 'Complete' : 'Next'} →
                        </button>
                    </div>
                </div>
                <p class="footer-text">Dr. Heeraj Bulluck, Consultant Interventional Cardiologist</p>
            `;
        }

        function renderResults() {
            const result = calculateScore();
            const icon = result.color === 'green' ? '✓' : result.color === 'amber' ? '⚠' : result.color === 'grey' ? '?' : '⚠';
            
            // Missing parameters section (only if indeterminate)
            const missingParamsSection = result.missingData && result.missingData.length > 0 && result.color === 'grey' ? `
                <div class="result-section missing-params">
                    <h3>Missing Parameters That Need Attention:</h3>
                    <ul>
                        ${result.missingData.map(param => `<li><span>⚠</span><span>${param}</span></li>`).join('')}
                    </ul>
                </div>
            ` : '';
            
            // Projected risk section (only if indeterminate and has projected risk)
            const projectedRiskSection = result.projectedRisk ? `
                <div class="projected-risk-section">
                    <h3>Want to See Your Projected Risk?</h3>
                    <p>While we cannot provide an accurate assessment without complete data, we can show you what your risk profile might look like if your missing parameters were within normal ranges.</p>
                    <div class="caveat">
                        <strong>⚠ Important Caveat:</strong> This projection assumes your missing values are normal, which may not be the case. This is NOT a substitute for actual measurements and should only be used as a rough estimate to understand the importance of the parameters you do have.
                    </div>
                    <button class="reveal-btn" onclick="revealProjectedRisk()">
                        Show Projected Risk Assessment
                    </button>
                    <div id="projectedResults" class="projected-results hidden">
                        <div class="traffic-light ${result.projectedRisk.color}">${result.projectedRisk.color === 'green' ? '✓' : result.projectedRisk.color === 'amber' ? '⚠' : '⚠'}</div>
                        <h2 class="result-title">PROJECTED: ${result.projectedRisk.level}</h2>
                        <div class="result-subtitle">(Assuming Missing Values Are Normal)</div>
                        <div class="result-section">
                            <p>${result.projectedRisk.message}</p>
                            <p style="margin-top: 1rem;"><strong>Remember:</strong> This is speculation based on incomplete data. Get your missing parameters measured to know your true risk profile.</p>
                        </div>
                        
                        <div class="cta-box">
                            <h3>Want More Insight and See How I Can Help You?</h3>
                            <p>Book your free 1:1 strategy call with Dr. Heeraj Bulluck</p>
                            <a href="https://stan.store/drheerajbulluck/p/book-a-11-heart-reset-call" 
                               target="_blank" 
                               class="cta-btn">
                                Book Your Free Strategy Call
                            </a>
                        </div>
                        
                        <div class="result-section book-cta">
                            <h3 style="text-align: center;">Learn More About Cardiovascular Health Optimization</h3>
                            <p style="text-align: center;">Discover evidence-based strategies to prevent heart disease</p>
                            <div style="text-align: center;">
                                <a href="https://amzn.eu/d/dfy7f2d" 
                                   target="_blank" 
                                   class="cta-btn">
                                    Check Out Heart Reset 40 Book on Amazon
                                </a>
                            </div>
                        </div>
                    </div>
                </div>
            ` : '';
            
            // Only show CTA boxes for complete assessments (not indeterminate)
            const ctaBoxes = result.color !== 'grey' ? `
                <div class="cta-box">
                    <h3>Want More Insight and See How I Can Help You?</h3>
                    <p>Book your free 1:1 strategy call with Dr. Heeraj Bulluck</p>
                    <a href="https://stan.store/drheerajbulluck/p/book-a-11-heart-reset-call" 
                       target="_blank" 
                       class="cta-btn">
                        Book Your Free Strategy Call
                    </a>
                </div>
                
                ${result.color === 'green' ? `
                    <div class="result-section book-cta">
                        <h3 style="text-align: center;">Learn More About Cardiovascular Health Optimization</h3>
                        <p style="text-align: center;">Discover evidence-based strategies to prevent heart disease</p>
                        <div style="text-align: center;">
                            <a href="https://amzn.eu/d/dfy7f2d" 
                               target="_blank" 
                               class="cta-btn">
                                Check Out Heart Reset 40 Book on Amazon
                            </a>
                        </div>
                    </div>
                ` : ''}
            ` : '';
            
            return `
                <div class="card results">
                    <div class="traffic-light ${result.color}">${icon}</div>
                    <h1 class="result-title">${result.level}</h1>
                    <div class="result-subtitle">Your Cardiovascular Risk Assessment</div>
                    
                    <div class="result-section">
                        <p>${result.message}</p>
                    </div>
                    
                    ${(() => {
                        const nonModifiableFactors = ['Age 65+', 'Age 55-64', 'Age 45-54', 'Age 35-44', 'High-risk ethnicity', 'Ethnic risk', 'Family history'];
                        
                        // Separate into categories
                        const highRisk = result.highRiskFactors || [];
                        const suboptimal = result.suboptimalFactors || [];
                        
                        const highRiskMod = highRisk.filter(f => !nonModifiableFactors.includes(f));
                        const highRiskNonMod = highRisk.filter(f => nonModifiableFactors.includes(f));
                        const suboptimalMod = suboptimal.filter(f => !nonModifiableFactors.includes(f));
                        const suboptimalNonMod = suboptimal.filter(f => nonModifiableFactors.includes(f));
                        
                        const hasAnyFactors = highRisk.length > 0 || suboptimal.length > 0;
                        if (!hasAnyFactors) return '';
                        
                        let html = '<div class="result-section risk-factors"><h3>Key Risk Factors Identified:</h3>';
                        
                        // Non-Modifiable Section
                        if (highRiskNonMod.length > 0 || suboptimalNonMod.length > 0) {
                            html += '<p style="font-size: 0.9em; color: #D84315; margin-bottom: 0.5rem; font-weight: 600;">Non-Modifiable Factors:</p>';
                            html += '<ul>';
                            if (highRiskNonMod.length > 0) {
                                html += highRiskNonMod.map(f => `<li><span>•</span><span>${f}</span></li>`).join('');
                            }
                            if (suboptimalNonMod.length > 0) {
                                html += suboptimalNonMod.map(f => `<li style="opacity: 0.8;"><span>•</span><span>${f}</span></li>`).join('');
                            }
                            html += '</ul>';
                        }
                        
                        // Modifiable Section
                        if (highRiskMod.length > 0 || suboptimalMod.length > 0) {
                            if (highRiskNonMod.length > 0 || suboptimalNonMod.length > 0) {
                                html += '<p style="font-size: 0.9em; color: #D84315; margin: 1.5rem 0 0.5rem; font-weight: 600;">Modifiable Factors:</p>';
                            }
                            html += '<ul>';
                            if (highRiskMod.length > 0) {
                                html += highRiskMod.map(f => `<li><span>•</span><span>${f}</span></li>`).join('');
                            }
                            if (suboptimalMod.length > 0) {
                                html += suboptimalMod.map(f => `<li style="opacity: 0.8;"><span>•</span><span>${f}</span></li>`).join('');
                            }
                            html += '</ul>';
                        }
                        
                        html += '</div>';
                        return html;
                    })()}
                    
                    ${missingParamsSection}
                    
                    ${result.color === 'grey' || result.color === 'green' ? `
                        <div class="result-section actions">
                            <h3>Recommended Actions:</h3>
                            <ul>
                                ${result.actions.map((action, i) => {
                                    const isMissing = result.missingData && result.missingData.includes(action);
                                    return `<li class="${isMissing ? 'missing-data' : ''}"><span>${i+1}.</span><span>${action}</span></li>`;
                                }).join('')}
                            </ul>
                        </div>
                    ` : ''}
                    
                    ${projectedRiskSection}
                    
                    ${ctaBoxes}
                    
                    <div class="result-section" style="background: #f5f5f5; font-size: 0.9rem; color: #666;">
                        <p style="font-weight: 600; margin-bottom: 0.5rem;">Disclaimer:</p>
                        <p>For educational and guidance purposes only. Not medical advice. Consult your physician.</p>
                        <p style="margin-top: 1rem;"><strong>Dr. Heeraj Bulluck, MBBS, PhD</strong><br>Consultant Interventional Cardiologist<br>Author of Heart Reset 40</p>
                    </div>
                    
                    <button class="btn btn-restart" onclick="restartAssessment()" style="margin: 2rem auto; display: block;">
                        Take Assessment Again
                    </button>
                </div>
            `;
        }

        // Event handlers
        function continueFromDisclaimer() {
            state.showDisclaimer = false;
            render();
        }

        function selectOption(questionId, value) {
            state.answers[questionId] = value;
            render();
        }

        function toggleMultiselect(questionId, value) {
            const current = state.answers[questionId] || [];
            
            if (value === 'None') {
                state.answers[questionId] = ['None'];
            } else {
                const filtered = current.filter(x => x !== 'None');
                if (current.includes(value)) {
                    state.answers[questionId] = filtered.filter(x => x !== value);
                } else {
                    state.answers[questionId] = [...filtered, value];
                }
            }
            render();
        }

        function updateNumberInput(questionId, value) {
            state.answers[questionId] = value;
            // Don't call render() - just update state silently to keep focus
        }

        function handleNumberInput(questionId, value) {
            state.answers[questionId] = value;
            // Enable/disable next button without re-rendering
            const nextBtn = document.getElementById('nextBtn');
            if (nextBtn) {
                const questions = getCurrentQuestions();
                const question = questions[state.currentQuestion];
                if (value || question.skip) {
                    nextBtn.disabled = false;
                } else {
                    nextBtn.disabled = true;
                }
            }
        }

        function goBack() {
            const questions = getCurrentQuestions();
            if (state.currentQuestion > 0) {
                state.currentQuestion--;
            } else if (state.currentSection > 0) {
                state.currentSection--;
                const prevQuestions = sections[state.currentSection].questions.filter(q => 
                    !q.conditional || q.conditional(state.answers)
                );
                state.currentQuestion = prevQuestions.length - 1;
            }
            render();
        }

        function skipQuestion() {
            goNext();
        }

        function goNext() {
            const questions = getCurrentQuestions();
            if (state.currentQuestion < questions.length - 1) {
                state.currentQuestion++;
            } else if (state.currentSection < sections.length - 1) {
                state.currentSection++;
                state.currentQuestion = 0;
            } else {
                state.showResults = true;
            }
            render();
            window.scrollTo(0, 0);
        }

        function restartAssessment() {
            state = {
                showDisclaimer: false,
                currentSection: 0,
                currentQuestion: 0,
                answers: {},
                showResults: false
            };
            render();
            window.scrollTo(0, 0);
        }

        function revealProjectedRisk() {
            const projectedResults = document.getElementById('projectedResults');
            if (projectedResults) {
                projectedResults.classList.remove('hidden');
                // Scroll to the revealed section
                projectedResults.scrollIntoView({ behavior: 'smooth', block: 'nearest' });
            }
        }

        // Main render
        function render() {
            const app = document.getElementById('app');
            
            if (state.showDisclaimer) {
                app.innerHTML = renderDisclaimer();
            } else if (state.showResults) {
                app.innerHTML = renderResults();
            } else {
                app.innerHTML = renderQuestion();
            }
        }

        // Initialize
        render();
    </script>
</body>
</html>
