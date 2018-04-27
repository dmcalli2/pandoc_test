
Defining comorbidities/covariates
=================================

Having reviewed the baseline data from a set of clinical trials from the YODA repository, the following data have been found to be available.

| Information type           | Number of trials |
|----------------------------|------------------|
| Age and sex                | 37               |
| Height and weight (or BMI) | 32               |
| Blood pressure             | 27               |
| Concomitant medication     | 37               |
| Medical history            | 22               |
| Laboratory results         | 34               |

Based on an examination of these covariate data (without having examined outcome or treatment allocation data) we will adopt the comorbidity/covariate definitions for all trials across the YODA, NIH BioLINCC and CSDR repositories, and any subsequent repositories.

Age
===

Age in years will be standardised to the mean and standard deviation for age from the US National Health and Nutrition Survey (NHANES), 2015-16. Data and documentation at *<https://wwwn.cdc.gov/nchs/nhanes/continuousnhanes/default.aspx?BeginYear=2015>.* For both the main effect and interaction with treatment, age will be modelled as a continuous variable. Details of the approach for modelling continuous variables are given at the end of this document.

Sex
===

Sex will be coded as 1 for female and 0 for male. This has been chosen as historically there has been greater interest in whether treatments tested in predominantly male populations are equally effective in women.

Race/Ethnicity
==============

We did not previously apply for race or ethnicity variables, but will do so in subsequent applications to trial repositories. In the main analysis we will examine race.Ethnicity will be included only in a secondary analysis.

In the absence of an international consensus, we will collapse race categories to correspond to the US Office of Management and Budget (OMB) definitions (American Indian or Alaska Native, Asian, Black or African American, Native Hawaiian or Other Pacific Islander and White) as described in the FDA guidelines for race/ethnicity in clinical trials.(1) We will map other terms to these categories using the “roll-up” scheme shown in Figure 3.3 of the 2009 Institute of Medicine (IOM) report on “Race, Ethnicity, and Language Data: Standardization for Health Care Quality Improvement”. The roll-up given in the FDA recommendation is a subset of that in the IOM report, containing fewer terms. Terms not found in this list will be classified as “Other”.

In the IOM report, the use of OMB categories are described as reasonable “when an analyst needs a consistent set of minimum categories to make comparisons across systems”.(2) As such, their use seems appropriate for our analysis.

We acknowledge that the OMB categories, and the mappings, were designed for a US context, and may be less appropriate in other settings. Nonetheless, we have opted to use these because FDA policy is influential internationally as regards trial design and conduct. Moreover, we been unable to find guidance on this topic from equivalent organisations in other countries or federations.

Of the 2172 trials selected for this research and registered on the PROSPERO systematic review register website, 350 reported baseline counts according to race on clinicaltrials.gov. We collapsed these according to the IOM rollup to OMB categories. Figure 1 shows the percentage of participants within each OMB category for each trial. Where a trial reported counts aggregated across 2 or more OMB categories (eg “White or Asian - 103 participants”) we counted both. As such, the proportion of participants in each category is known to be an overestimate.

Figure 1 OMB Race categories in selected trials. Boxplots indicate distribution across the trials for the percentage of participants in that category in each trial
-------------------------------------------------------------------------------------------------------------------------------------------------------------------

On the basis of this observed distribution, we will use “White” as the reference category, as this is the commonest grouping, with indicator variables for “Asian”, “Black or African American”. We will also use a single indicator variable of “Other” for the remaining categories as these are uncommon.

Socio-economic status
=====================

So far, no measure of socio-economic status (eg income, educational level, deprivation scores) has been recorded in any of the commercial trials examined.

Reported medical history
========================

We will not use the reported medical history to **define** comorbidities.

This is because of incomplete reporting and the fact that the medical history data varies considerably between trials in terms of collection (for example, there are frequently specific questions for diseases closely related to the main outcome and only broad screening questions for unrelated diseases) and recording. An additional difficulty is that some sponsors redact the condition data to preserve privacy. Consequently, this data will only be used as a check on the definitions described in the following sections.

Concomitant medications based definitions
=========================================

It is also likely that trials will differ in the accuracy and completeness of concomitant medicine data recording. For example, compared to other trials, respiratory trials may be more likely to identify inhaled therapies.

Nevertheless, obtaining a yes/no drug history is intrinsically less complex than taking a past medical history. Moreover, concomitant medications are assigned to World Health Organisation Anatomic Therapeutic Chemical (WHO-ATC) codes in a consistent manner across trials. The WHO ATC system is organised around indications, and for some drug classes it is reasonable to infer that a trial participant has one or more of a narrow set of diseases (eg reporting use of thyroid drugs indicates the presence of thyroid disease). Therefore, we will use concomitant medications to identify comorbid conditions.

Previous studies have also used the WHO ATC criteria to define comorbid diseases, but usually in routine healthcare data with the goal being descriptive epidemiology, as in a recent paper by Huber et al.(3) We are not aware of any previous study which has used this approach for individual-level participant data from clinical trials, or to examine heterogeneity of treatment effects. We have therefore created a set of definitions substantially different from previous reports, reflecting our need for greater specificity (Table 1).

For each of the drug-based definitions in Table 1, reported concomitant medications are eligible if they were started at any time on or before starting the trial drug (or comparator) regardless of when they were stopped. Topical drugs are not included in the definitions except for M02 or S01E. Nor drugs with an inhaled or nebulised route of administration, except for R03 drugs.

This approach to defining comorbidities is a compromise between sensitivity and specificity and some misclassification is inevitable, reflecting the difficulty of inferring diagnoses from drug-usage. We have attempted to minimise the misclassification based on our understanding of clinical practice.

For example, rather than assuming all participants taking a drug in the A02B class have an acid-related disorder (Table 1) we have limited this definition to exclude participants also taking non-steroidal drugs or any drug with anti-thrombotic actions (aspirin, antiplatelets, warfarin etc). Similarly, we have not used aspirin to define cardiovascular disease because it is in widespread use for primary prevention.(4)

Moreover, while the ATC system is organised around therapeutic indications, not all indications are coded. This is because “A medicinal substance can be given more than one ATC code
\* \* *O**N**L**Y* \* \*
 if it is available in two or more strengths or routes of administration with clearly different therapeutic uses.”(5) For example, finasteride is classified as a dermatological drug if low-dose and as a drug for benign prostatic hyperplasia if high-dose. Therefore, for a single strength and route of administration, there is only “one code, the main indication being decided on the basis of the available information.” (5)

Moreover, the “main” WHO ATC indication is not necessarily the commonest indication. For example, in a US study of drug “mentions” in a representative database, &gt;80% of mentions for gabapentin and amitriptyline were for off-label indications, predominantly pain.(6) Similarly, in a Canadian study of antidepressant use in primary care, amitriptyline was “almost exclusively prescribed for off-label indications” most commonly for pain, insomnia, and migraine.(7) These published findings are consistent with the clinical observation of members of our steering committee (and an independent epileptologist), that these drugs are predominantly used for pain. Despite this, the WHO ATC scheme does not include pain as an indication for these drugs, classifying gabapentin and pregabalin exclusively as antiepileptics and amitriptyline exclusively as an antidepressant.

Nor is there necessarily a code where routes/strengths do differ. For example, prochlorperazine is defined solely as an antipsychotic, despite being available in a buccal preparation for nausea. IN this case the accompanying note states that “The substances in this group are sometimes used for other indications in much lower doses”.

We have attempted to incorporate these nuances into the drug-based comorbidity definitions given in Table 1.

An additional complexity is caused by the fact that for certain trials, sponsors have only provided less specific codes (eg 3 or 4-character codes) and not 5-character codes which uniquely identify each class (7-character codes identifying each agent). Where this is the case, but the drug name with or without route and indication information have been provided, we will assign each potentially-relevant drug to a WHO ATC code using the US Government drug metathesaurus (RXNORM). Where neither the drug name, nor sufficiently detailed drug-class information is provided, we will adopt a workaround suited to each definition (Table 1). The number of trials where this approach was needed will be reported.

The proportion of participants with and without comorbid diseases based on concomitant medications with and without relevant medical histories (in trials where these have been provided) will be compared in 2x2 contingency tables. We expect to find a higher proportion with the relevant condition from the reported medical history among those participants meeting the concomitant medication definitions (eg 80% versus 10% reporting diabetes in participants taking/not taking antidiabetic medications).

### 

### Table 1 Concomitant medication classes

<table>
<colgroup>
<col width="19%" />
<col width="1%" />
<col width="13%" />
<col width="65%" />
</colgroup>
<thead>
<tr class="header">
<th>Condition</th>
<th>ATC codes</th>
<th>ATC label</th>
<th>Exceptions/more specific definitions/notes</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Acid related disorders</td>
<td>A02A</td>
<td>ANTACIDS</td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td>A02B</td>
<td>DRUGS FOR ACID RELATED DISORDERS</td>
<td>Exclude where also taking M01A ANTIINFLAMMATORY AND ANTIRHEUMATIC PRODUCTS, NON-STEROIDS, or B01 (antithrombotic) drugs</td>
</tr>
<tr class="odd">
<td>Diabetes mellitus</td>
<td>A10</td>
<td>DRUGS USED IN DIABETES</td>
<td>Note this includes insulins and analogues, other blood glucose lowering drugs etc. It does not include cardiovascular prevention drugs We do not exclude metformin, although this is used to treat Polycystic ovary syndrome (PCOS) as this is used in PCOS to treat insulin resistance.</td>
</tr>
<tr class="even">
<td>Thromboembolic disease, atrial fibrillation or valvular heart disease</td>
<td>B01AA</td>
<td>Vitamin K antagonists</td>
<td>Do not include if only 4-level codes are available.</td>
</tr>
<tr class="odd">
<td></td>
<td>B01AE</td>
<td>Direct thrombin inhibitors</td>
<td>Do not include if only 4-level codes are available.</td>
</tr>
<tr class="even">
<td></td>
<td>B01AF</td>
<td>Direct factor Xa inhibitors</td>
<td>Do not include if only 4-level codes are available.</td>
</tr>
<tr class="odd">
<td>Cardiovascular diseases</td>
<td>C01</td>
<td>CARDIAC THERAPY DRUGS</td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td>C04</td>
<td>PERIPHERAL VASODILATORS</td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td>C02</td>
<td>ANTIHYPERTENSIVES</td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td>C07</td>
<td>beta-Adrenergic Blocking Agents</td>
<td>Except “propranolol” or other “C07AA Beta blocking agents, non-selective” non-selective beta-blockers where participant is also taking an N02C drug</td>
</tr>
<tr class="odd">
<td></td>
<td>C08</td>
<td>CALCIUM CHANNEL BLOCKERS</td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td>C09</td>
<td>AGENTS ACTING ON THE RENIN-ANGIOTENSIN SYSTEM</td>
<td></td>
</tr>
<tr class="odd">
<td>Urinary frequency and incontinence</td>
<td>G04BD</td>
<td>Drugs for urinary frequency and incontinence</td>
<td>If only-4-character code define as urinary frequency and incontinence or ED. If only 3-character code, define as urological and/or ED and/or BPH.</td>
</tr>
<tr class="even">
<td>Erectile dysfunction</td>
<td>G04BE</td>
<td>Drugs used in erectile dysfunction</td>
<td>If only-4-character code define as urinary frequency and incontinence or ED. If only 3-character code, define as urological and/or ED and/or BPH.</td>
</tr>
<tr class="odd">
<td>Benign prostatic hypertrophy</td>
<td>G04C</td>
<td>DRUGS USED IN BENIGN PROSTATIC HYPERTROPHY</td>
<td>If only 3-character code, define as urological and/or ED and/or BPH.</td>
</tr>
<tr class="even">
<td>Glaucoma</td>
<td>S01E</td>
<td>ANTIGLAUCOMA PREPARATIONS AND MIOTICS</td>
<td>If only 3-character code define as eye disease.</td>
</tr>
<tr class="odd">
<td>Arthritis and arthralgia</td>
<td>M01A</td>
<td>ANTIINFLAMMATORY AND ANTIRHEUMATIC PRODUCTS, NON-STEROIDS</td>
<td>If only 3-character code define as arthritis and arthralgia, but accept some misclassification possible as indications for penicillamine include “conditions associated with impaired copper metabolism” eg Wilson’s disease and gold is used to treat dermatological conditions.</td>
</tr>
<tr class="even">
<td></td>
<td>M01B</td>
<td>ANTIINFLAMMATORY/ANTIRHEUMATIC AGENTS IN COMBINATION</td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td>M02</td>
<td>TOPICAL PRODUCTS FOR JOINT AND MUSCULAR PAIN</td>
<td></td>
</tr>
<tr class="even">
<td>Osteoporosis (or risk factors for osteoporosis)</td>
<td>M05</td>
<td>DRUGS FOR TREATMENT OF BONE DISEASES</td>
<td></td>
</tr>
<tr class="odd">
<td>Gout</td>
<td>M04</td>
<td>ANTIGOUT PREPARATIONS</td>
<td>Although allopurinol is being used for other indications, this is unlikely to be widespread.</td>
</tr>
<tr class="even">
<td>Inflammatory arthropathies, inflammatory bowel disease, systemic lupus erythematosus and connective tissue diseases</td>
<td>A07EA</td>
<td>Corticosteroids acting locally</td>
<td>Where only 3-character codes are provided, define as any A07</td>
</tr>
<tr class="odd">
<td></td>
<td>A07EC</td>
<td>Aminosalicylic acid and similar agents</td>
<td>Where only 3- character codes are provided, define as any A07</td>
</tr>
<tr class="even">
<td></td>
<td>L04AB</td>
<td>Tumour necrosis factor alpha (TNF-) inhibitors</td>
<td>Where only 3- character codes are provided, define as any L04</td>
</tr>
<tr class="odd">
<td></td>
<td>L04AA</td>
<td>Selective immunosuppressants</td>
<td>Where only 3- character codes are provided, define as any L04</td>
</tr>
<tr class="even">
<td></td>
<td>L04AX</td>
<td>Other immunosuppressants (includes methotrexate,azathioprine, and lefluonomide)</td>
<td>Where only 3- character codes are provided, define as any L04</td>
</tr>
<tr class="odd">
<td></td>
<td>M01CB</td>
<td>Gold preparations</td>
<td>Do not define if only 3-character code is available. If only 4-character code available define, since only other agent is an obscure drug oxycinchophen</td>
</tr>
<tr class="even">
<td></td>
<td>M01CC</td>
<td>Penicillamine and similar agents</td>
<td>Do not define if only 3-character code is available. If only 4-character code available define, since only other agent is an obscure drug oxycinchophen</td>
</tr>
<tr class="odd">
<td>Migraine</td>
<td>N02C</td>
<td>ANTIMIGRAINE PREPARATIONS</td>
<td>Do not define if only 3-character code is available</td>
</tr>
<tr class="even">
<td>Pain</td>
<td>N02A</td>
<td>OPIOIDS</td>
<td>If only 3-character code available define as pain</td>
</tr>
<tr class="odd">
<td></td>
<td>N02B</td>
<td>OTHER ANALGESICS AND ANTIPYRETICS</td>
<td></td>
</tr>
<tr class="even">
<td>Schizophrenia and delusional disorders</td>
<td>N05A</td>
<td>ANTIPSYCHOTICS</td>
<td>Prochlorperazine is included in this class. If individual drug data available exclude if prochlorperazine. If 5-character code available exclude “N05AB Phenothiazines with piperazine structure”. If only 4-character code is available do not define.</td>
</tr>
<tr class="odd">
<td>Mood, neurotic and sleep disorders</td>
<td>N05B</td>
<td>ANXIOLYTICS</td>
<td>If only 3-character code available do not define.</td>
</tr>
<tr class="even">
<td></td>
<td>N05C</td>
<td>HYPNOTICS AND SEDATIVES</td>
<td>If only 3-character code available do not define</td>
</tr>
<tr class="odd">
<td></td>
<td>N06A</td>
<td>ANTIDEPRESSANTS</td>
<td>Except amitriptyline. If drug term not available</td>
</tr>
<tr class="even">
<td>Epilepsy</td>
<td>N03</td>
<td>ANTIEPILEPTICS</td>
<td>Except where drug is pregabalin, gabapentin or valproic acid. If specific drug is not given, and if indication for drug is not stated proceed as follows. If only a 5-character code is provided exclude N03AX (which includes gabapentin and pregabalin) and N03AG (includes valproic acid). This will reduce sensitivity, but improve specificity. If only a 4-character code is provided do not attempt to define.</td>
</tr>
<tr class="odd">
<td>Parkinson’s disease and Parkinsonism</td>
<td>N04</td>
<td>ANTI-PARKINSON DRUGS</td>
<td></td>
</tr>
<tr class="even">
<td>Dementia</td>
<td>N06D</td>
<td>ANTI-DEMENTIA DRUGS</td>
<td>Do not define if only 3-character code is available</td>
</tr>
<tr class="odd">
<td>Chronic lower respiratory disease</td>
<td>R03</td>
<td>DRUGS FOR OBSTRUCTIVE AIRWAY DISEASES</td>
<td></td>
</tr>
<tr class="even">
<td>Thyroid disorders</td>
<td>H03</td>
<td>THYROID THERAPY DRUGS</td>
<td></td>
</tr>
</tbody>
</table>

Height and weight
=================

We will use body mass index (BMI) where this is provided, or calculate it from the weight and height (weight in kg/height in meters-squared). Where multiple BMI measures are available, we will use the last BMI measured just prior to the initiation of the intervention. BMI will be standardised to the BMI in the adult population from NHANES 2015-16 (see Blood Pressure section for details). We will treat BMI as a continuous variable in the modelling.

Blood pressure
==============

In the largest study of blood pressure, a meta-analysis of 958,074 participants from 61 prospective studies, mid-blood pressure (0.5 x DBP + 0.5 \* SBP) performed slightly better than SBP alone for both stroke and ischaemic heart disease risk.(8) Consequently, we will use this measure in our models.

In a simulation study, with SBP as the outcome variable, Tobin et al demonstrated that adding a suitable constant (eg 10mmHg) for patients taking anti-hypertensive reduced bias as well as any of several more complex methods, whereas including a dummy variable for treatment introduced bias.(9) We will use this approach for SBP as a covariate in the covariate-treatment interaction models, under the assumption that the true underlying blood pressure is most relevant to the analysis. We will similarly add a constant of 5 mmHg to the diastolic blood pressure. Both constants will be added prior to calculating the mid-blood pressure.

If a participant is taking a drug from any of the following drug classes prior to initiating the study drug we will perform the correction; C02 – ANTIHYPERTENSIVES, C07 - beta-Adrenergic Blocking Agents, C08 - CALCIUM CHANNEL BLOCKERS or C09 - AGENTS ACTING ON THE RENIN-ANGIOTENSIN SYSTEM. We will perform the correction only once regardless of the number of different antihypertensive drugs any participant is taking, and regardless of whether the drug was given for hypertension or a different indication (eg a calcium channel blocker for angina).

Since blood pressure shows considerable within-person variability, we will take the mean of all measures obtained prior to initiation of the drug (ie those from screening and randomisation visits). Having done so we will standardise the blood pressure results to the adult blood pressure results from NHANES 2015-16 (Table 2).

### Table 2 Adult (aged &gt;=18) NHANES 2015-16 blood pressure averaged over (up to) 3 recordings

| Blood Pressure | Mean | Standard deviation |
|----------------|------|--------------------|
| Diastolic      | 70   | 12                 |
| Systolic       | 123  | 17                 |

For data see [*https://wwwn.cdc.gov/nchs/nhanes/continuousnhanes/default.aspx?BeginYear=2015*](https://wwwn.cdc.gov/nchs/nhanes/continuousnhanes/default.aspx?BeginYear=2015).

Laboratory test based definitions
=================================

Liver impairment
----------------

We will use the Fibrosis-4 (FIB4) index to examine for the presence of liver disease. FIB4 will be calculated as follows:-

\\\[FIB4 =   \\\]

Age is measured in years, AST and ALT in international units per litre and platelet counts as 10^9 platelets per litre.

This will not be calculated for patients with anaemia or known inflammatory diseases, which for the purposes of this analysis we will define as the inflammatory arthropathies and inflammatory bowel diseases. We will not include conditions which feature lower levels of systemic inflammation (eg metabolic syndrome, COPD). Operationally, any participant meeting the drug-based definition for “Inflammatory arthropathies, inflammatory bowel disease, systemic lupus erythematosus and connective tissue diseases” will not have a FIB4 calculated. For trials where inflammatory arthropathies or inflammatory bowel diseases conditions are indications, the FIB4 will not be estimated. Where these are comorbidities (defined as per concomitant medications based definitions), the participant will be assigned the median FIB4 value for the trial.

FIB4 will be standardised to FIB4 derived from component variables recorded in NHANES 2015-16 and modelled as a continuous variable.

Renal impairment
----------------

Some of the trials may have been conducted in countries or sites where creatinine levels have not been standardised to an isotope dilution mass spectrometry (IDMS) reference measurement procedure. Therefore we will use the “Creatinine Standardization Recommendations (for countries or regions that are introducing or have not completed standardization of creatinine calibration)” from the NIDDK recommendations (<https://www.niddk.nih.gov/health-information/communication-programs/nkdep/laboratory-evaluation/glomerular-filtration-rate/creatinine-standardization/recommendations>).

This means that we will use the “Original Modification of Diet in Renal Disease (MDRD) Study equation for routine methods that have not been calibrated to be traceable to IDMS” and the “CKD-EPI or IDMS-traceable MDRD Study equation for estimating GFR in adults” for laboratory results where the creatinine measurement “has its calibration traceable to IDMS”. For consistency, we will use the IDMS-traceable MDRD Study equation (GFR (mL/min/1.73 m2) = 175 × (Scr)<sup>-1.154</sup> × (Age)<sup>-0.203</sup> × (0.742 if female) × (1.212 if African American) in the latter case.

The eGFR estimated from either method is normalized to 1.73 m² body surface area. As per the NIDDK guidance for providers (<https://www.niddk.nih.gov/health-information/professionals/clinical-tools-patient-education-outreach/ckd-drug-dosing-providers>) we will adjust for body surface area for people who are “very large or very small”. We will define these groups as having a height, weight or BMI below the 10<sup>th</sup> or above the 90<sup>th</sup> centile based on data from NHANES 2015-2016.

### Table 3 Quantiles for Height and Weight for NHANES 2015-2016

| Quantile                   | Weight (kg) | Height (cm) | BMI |
|----------------------------|-------------|-------------|-----|
| 10<sup>th</sup> percentile | 58          | 155         | 22  |
| 90<sup>th</sup> percentile | 111         | 182         | 38  |

For data see <https://wwwn.cdc.gov/nchs/nhanes/continuousnhanes/default.aspx?BeginYear=2015>

We estimate body surface area using the Mosteller equation(10) and use this to adjust the eGFR as per the NIDDK recommendation (eGFR/1.73m<sup>2</sup> x estimated BSA = eGFR).

Having derived the eGFR we will standardise this to eGFR derived from creatinine measured in NHANES 2015-16 using the IDMS-traceable MDRD Study equation (as the creatinine measure in NHANES is IDMS-standardised) and model it as a continuous variable.

Although for clinical reporting eGFR levels above 60 are simply reported as “&gt;=60” we will not similarly truncate our values, as we are allowing for non-linearity in the modelling.

Anaemia
-------

Since the relationship between haemoglobin and disease states is markedly non-linear (with haemoglobin levels above and below the normal range considered abnormal), we will model haemoglobin using a dichotomous variable for anaemia present/absent, and use an additional continuous term for the severity of anaemia. We propose to define anaemia as per the WHO definitions (<http://apps.who.int/iris/bitstream/10665/85839/3/WHO_NMH_NHD_MNM_11.1_eng.pdf> ). This defines anaemia as follows.

|                                | Not anaemia | Mild anaemia | Moderate anaemia |
|--------------------------------|-------------|--------------|------------------|
| Non-pregnant women (≥15 years) | ≥12         | &lt;12       | &lt;11           |
| Men (≥15 years)                | ≥13         | &lt;13       | &lt;11           |

We will use the “Not anaemia” threshold to define anaemia as present/absent. For the continuous component of the variable we will standardise Haemoglobin to the NHANES 2015-16 laboratory results (<https://wwwn.cdc.gov/nchs/nhanes/search/datapage.aspx?Component=Laboratory&CycleBeginYear=2015>).

Modelling approach
==================

This document focusses on how the covariates for covariate-treatment interactions will be defined and modelled. As such details of the approach to outcome variables and to the selection of treatment are provided in a separate document. Briefly, we will standardise all continuous outcomes to an appropriate reference population (eg a cohort study of people with diabetes for HbA1c). For continuous outcomes we will fit models on the identity and log-scales. For categorical outcomes, we will fit models on the log-odds, log-risk, log-hazard and log-rate scales.

We will model comorbidities as separate conditions, and in a single comorbidity score.

Separate comorbidities
----------------------

For each covariate and covariate treatment interaction we will model the main effect and treatment-covariate interaction unadjusted, and adjusting for age and sex, then age, sex and race, and finally age, sex, race and other covariates of interest.

Categorical variables (including anaemia present/absent) will be included as 0 or 1 for absent/present.

As described above, all continuous variables (age, BMI, blood pressure, eGFR and FIB4) will be standardised to a single common reference population using the mean and standard deviation of that variable. This is being done to help with model fitting. We are using NHANES 2015/16 as the data are readily accessible to the public and because NHANES is a representative sample of a particular population.

We will allow for non-linearity in the continuous variables by using fractional polynomials. We will base our approach on advice given by Royston for modelling interactions in clinical trials;(11) we will (i) find the best second-degree fractional polynomial transformations of the variable within each treatment group using a measure of model fit appropriate to the type of regression model, (ii)l use the chosen powers (which perform best across the treatment arms) in a treatment-covariate interaction. As we will be analysing multiple trials, we will examine fit within treatment arms across all available trials, and will use the same transformation for all trials.

Comorbidity in a single score
-----------------------------

We will also produce a model with a single comorbidity score (based on obesity, renal impairment, liver impairment, anaemia and each of the concomitant medicine derived terms). This will be produced by a simple summation of the categorical (0/1) and continuous variables. For the latter, the standardised variable will simply be included in the summation.

For the comorbidity score calculation, the concomitant medication definition pairs will be collapsed into a single condition.

### Table 4 Combining concomitant medication based definitions

| Definition 1 | Definition 2             |
|--------------|--------------------------|
| Pain         | Migraine                 |
| Pain         | Rheumatologic conditions |

Diagnostic code mapping
=======================

Each of the diagnoses above has been mapped to the closest available WHO ICD-10 codes and US Clinical Classifications Software codes.(12) The latter is an established aggregation system for ICD-10CM and ICD-10 codes for use in health services research.

| Diagnosis              | ICD-10                                | CCS |
|------------------------|---------------------------------------|-----|
| Acid related disorders | K21 Gastro-oesophageal reflux disease |

                                                                                                                       K25-K28 gastric to jejunal sites                                                                 
                                                                                                                                                                                                                        
                                                                                                                       and K29 Gastritis and duodenitis                                                                 | 138 Esophageal disorders                                                              
                                                                                                                                                                                                                                                                                                                
                                                                                                                                                                                                                         139 Gastroduodenal ulcer (except hemorrhage)                                           
                                                                                                                                                                                                                                                                                                                
                                                                                                                                                                                                                         and 140 Gastritis and duodenitis and                                                   |

Anaemia | D50-D53 Nutritional anaemias | 59 Deficiency and other anemia |
Arthritis and arthralgia | M05-M14 Inflammatory polyarthropathies   M15-M19 Arthrosis   M20-M25 Other joint disorders  | 202 Rheumatoid arthritis and related disease 203 Osteoarthritis 204 Other non-traumatic joint disorders 205 Spondylosis; intervertebral disc disorders; other back problems |
Benign prostatic hypertrophy | N40 Hyperplasia of prostate | 164 Hyperplasia of prostate |
Cardiovascular diseases | I10-I15 Hypertensive diseases I20-I25 Ischaemic heart diseases I60-I69 Cerebrovascular diseases I70 Atherosclerosis | 98 Essential hypertension 99 Hypertension with complications and secondary hypertension 100 Acute myocardial infarction 101 Coronary atherosclerosis and other heart disease 104 Other and ill-defined heart disease 106 Cardiac dysrhythmias 108 Congestive heart failure; nonhypertensive 109 Acute cerebrovascular disease 110 Occlusion or stenosis of precerebral arteries 111 Other and ill-defined cerebrovascular disease 112 Transient cerebral ischemia 113 Late effects of cerebrovascular disease 114 Peripheral and visceral atherosclerosis |
Chronic lower respiratory disease | J40 Bronchitis, not specified as acute or chronic   J41 Simple and mucopurulent chronic bronchitis   J42 Unspecified chronic bronchitis   J43 Emphysema   J44 Other chronic obstructive pulmonary disease   J45 Asthma   | 127 Chronic obstructive pulmonary disease and bronchiectasis 128 Asthma |
Chronic renal failure (assumes people with acute renal failure not recruited to trial) | N18 Chronic kidney disease | 158 Chronic kidney disease |
Dementia | F00 Dementia in Alzheimer disease F01 Vascular dementia F02 Dementia in other diseases classified elsewhere F03 Unspecified dementia and G30 Alzheimer disease | 653 Delirium dementia and amnestic and other cognitive disorders. |
Diabetes mellitus | E10-E14 Diabetes mellitus | 49 Diabetes mellitus without complication and 50 Diabetes mellitus with complications |
Epilepsy | G40 Epilepsy | 83 Epilepsy; convulsions. |
Erectile dysfunction | N48.4 Impotence of organic origin F52.2 Failure of genital response | 166 Other male genital disorders |
Glaucoma | H40-H42 Glaucoma | 88 Glaucoma |
Gout | M10 Gout | 54 Gout and other crystal arthropathies |
Hyperlipidaemia | E78 Disorders of lipoprotein metabolism and other lipidaemias | 53 Disorders of lipid metabolism |
Hypertension | I10 - Essential (primary) hypertension | 98 - Essential hypertension. |
Inflammatory arthropathies, inflammatory bowel disease, systemic lupus erythematosus and connective tissue diseases | L40 Psoriasis M05 Seropositive rheumatoid arthritis M06 Other rheumatoid arthritis M07 Psoriatic and enteropathic arthropathies M08 Juvenile arthritis M09 Juvenile arthritis in diseases classified elsewhere M30 Polyarteritis nodosa and related conditions   M31 Other necrotizing vasculopathies   M32 Systemic lupus erythematosus   M33 Dermatopolymyositis   M34 Systemic sclerosis M45 Ankylosing spondylitis K50 Crohn disease
*r**e**g**i**o**n**a**l**e**n**t**e**r**i**t**i**s*
 K51 Ulcerative colitis | 198 Other inflammatory condition of skin 202 Rheumatoid arthritis and related disease 210 systemic lupus erythematosus and connective tissue diseases 144 Regional enteritis and ulcerative colitis |
Liver disease | K70-77 | 151 Other liver diseases (other CCS codes cause-specific) |
Migraine | G43 Migraine | 84 Headache; including migraine |
Mood, neurotic and sleep disorders | F30-F39 Mood
*a**f**f**e**c**t**i**v**e*
 disorders   F40-F48 Neurotic, stress-related and somatoform disorders G47.0 Disorders of initiating and maintaining sleep
*i**n**s**o**m**n**i**a**s*
 | 657 Mood disorders 651 Anxiety disorders Note sleep disorders are just given residual codes |
Obesity | E66 Obesity | 58 Other nutritional; endocrine; and metabolic disorders |
Osteoporosis | M80 osteoporosis with pathological fracture and M81 osteoporosis without pathological fracture. | 206 osteoporosis and 207 pathological fracture. |
Pain | Pain in :- R10 abdomen M54.9 back N64.4 breast R07.1-R07.4 chest H92.0 ear H57.1 eye M25.5 joint M79.6 limb M54.5 lumbar region R10.2 pelvic and perineal F45.4 psychogenic M75.8 shoulder M54 spine R07.0 throat K14.6 tongue K08.8 tooth R52 pain, not elsewhere classified | 259 Residual codes; unclassified |
Parkinson’s disease and Parkinsonism | G20 Parkinson disease G21 Secondary parkinsonism G22 Parkinsonism in diseases classified elsewhere | 79 Parkinson\`s disease Note G21 given a non-specific code and G22 not classified |
Schizophrenia and delusional disorders | F20-F29 Schizophrenia, schizotypal and delusional disorders | 659 Schizophrenia and other psychotic disorders |
                                                                                                                    | | |
Thromboembolic disease, atrial fibrillation or valvular heart disease | I26 Pulmonary embolism I80.2 Phlebitis and thrombophlebitis of other deep vessels of lower extremities I82 Other venous embolism and thrombosis Atrial fibrillation and flutter Z95.2 Presence of prosthetic heart valve | |
Thyroid disorders | E01 Iodine-deficiency-related thyroid disorders and allied conditions   E02 Subclinical iodine-deficiency hypothyroidism   E03 Other hypothyroidism   E05 Thyrotoxicosis
*h**y**p**e**r**t**h**y**r**o**i**d**i**s**m*
   | 48 Thyroid disorders |
Urinary frequency and incontinence | N39.3 Stress incontinence N39.4 Other specified urinary incontinence R32 Unspecified urinary incontinence | 163 Genitourinary symptoms and ill-defined conditions |

References
==========

1. Collection of Race and Ethnicity Data in Clinical Trials. Guidance for Industry and Food and Drug Administration Staff
*I**n**t**e**r**n**e**t*
. Food and Drug Administration; 2016 Oct. Available from: <https://www.fda.gov/downloads/RegulatoryInformation/Guidances/ucm126396.pdf>

2. Institute of Medicine (US) Subcommittee on Standardized Collection of Race/Ethnicity Data for Healthcare Quality Improvement. Race, Ethnicity, and Language Data: Standardization for Health Care Quality Improvement
*I**n**t**e**r**n**e**t*
. Ulmer C, McFadden B, Nerenz DR, editors. Washington (DC): National Academies Press (US); 2009
*c**i**t**e**d*2018*A**p**r*24
. Available from: <http://www.ncbi.nlm.nih.gov/books/NBK219756/>

3. Huber CA, Szucs TD, Rapold R, Reich O. Identifying patients with chronic conditions using pharmacy data in Switzerland: an updated mapping approach to the classification of medications. BMC Public Health. 2013 Oct 30;13:1030.

4. Stuntz M, Bernstein B. Recent trends in the prevalence of low-dose aspirin use for primary and secondary prevention of cardiovascular disease in the United States, 2012–2015. Prev Med Rep. 2016 Dec 28;5:183–6.

5. WHO Collaborating Centre for Drug Statistics Methodology. ATC classification index with DDDs. 2015.

6. Radley DC, Finkelstein SN, Stafford RS. Off-label prescribing among office-based physicians. Arch Intern Med. 2006 May 8;166(9):1021–6.

7. Wong J, Motulsky A, Abrahamowicz M, Eguale T, Buckeridge DL, Tamblyn R. Off-label indications for antidepressants in primary care: descriptive study of prescriptions from an indication based electronic prescribing system. BMJ. 2017 Feb 21;356:j603.

8. Age-specific relevance of usual blood pressure to vascular mortality: a meta-analysis of individual data for one million adults in 61 prospective studies. The Lancet. 2002 Dec 14;360(9349):1903–13.

9. Tobin Martin D., Sheehan Nuala A., Scurrah Katrina J., Burton Paul R. Adjusting for treatment effects in studies of quantitative traits: antihypertensive therapy and systolic blood pressure. Stat Med. 2005 Sep 8;24(19):2911–35.

10. Mosteller RD. Simplified calculation of body-surface area. N Engl J Med. 1987 Oct 22;317(17):1098.

11. Royston P. The use of fractional polynomials to model interactions between treatment and continuous covariates in clinical trials. In: ResearchGate
*I**n**t**e**r**n**e**t*
.
*c**i**t**e**d*2018*A**p**r*6
. Available from: [https://www.researchgate.net/publication/4998077\\\_The\\\_use\\\_of\\\_fractional\\\_polynomials\\\_to\\\_model\\\_interactions\\\_between\\\_treatment\\\_and\\\_continuous\\\_covariates\\\_in\\\_clinical\\\_trials](https://www.researchgate.net/publication/4998077\_The\_use\_of\_fractional\_polynomials\_to\_model\_interactions\_between\_treatment\_and\_continuous\_covariates\_in\_clinical\_trials)

12. Agency for Healthcare Research and Quality. Clinical Classifications Software for ICD-10 Data
*I**n**t**e**r**n**e**t*
. 2012
*c**i**t**e**d*2015*D**e**c*31
. Available from: [http://www.ahrq.gov/research/data/hcup/icd10usrgd.html\\\#elix](http://www.ahrq.gov/research/data/hcup/icd10usrgd.html\#elix)
