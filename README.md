# BUS4029H Thesis Project
### What impact do maternity benefits have onthe healthcare expenditure by medicalschemes in South Africa?

## 1 - Creation of Single Data Set
This interactive python notebook reads in the Excel shreadsheet containing the hospital claims data for Schemes A,B and C. It concatenates the data together and creates a single data frame containing all the claims. This data frame is then exported as an Excel spreadsheet.

## 2 - Cleaning Process
This notebook reads in the single data frame created in the previous notebook. It then performs the following tasks:
- Formats all column headings to be in title case
- Removes any fully duplicated rows 
- Sets a number of columns' data type to category inlcuding
    - Admission Category 
    - Hospital group
    - Magisterial district description
    - Region discription
    - Final diagnosis
    - Patient gender
- Creates a new column called 'member ID', which creates a unique identifier for each patient
- Removes all data points which correspond to claims originating outside of South Africa

The Data is then split. A data frame for claims corresponding to the mothers only is created. A similar data frame is created for the infants. In order to further clean the data, the following steps are taken: 
- Rows corresponding to claims associated with the mother, but where the admission category relates to the infant are removed
- Rows corresponding to claims associated with the infant, but where the admission category relates to the mother are removed

Two Excel Spreadsheets are exported. One containing the cleaned data of the mothers' hospital claims and one containing the infants' hospital claims.

## 3 - Analysis of Mothers
This notebook reads in the single data frame relating to the hospital claims data for the mothers. It then analyses the following:

### Related to the Number of Caeserean Sections and Natural Deliveries Each Year
- The number of natural and caesarean deliveries recorded in the admissions category column 
- The number of patients whose final diagnosis contained one of the following ICD-10 codes:
    - O80.0, O80.1, O80.8, O80.9
    - O81.0, O81.1, O81.2, O81.3, O81.4, O81.5
    - O82.0, O82.1, O82.2, O82.8, O82.9
    - O83.0, O83.1, O83.2, O83.3, O83.4, O83.8, O83.9
    - O84.0, O84.1, O84.2, O84.8, O84.9
- The number of mothers whose final diagnosis indicated they delivered a baby and had a Uterine Scar From a Previous Surgery   
- The yearly change in the number of caesarean and natural births
- The yearly change in the total number of births

### Related to Costs 
- The average total cost and length of stay for natural and caesarean deliveries
- The outlires in the total cost column for natural and caeserian births respectively
    - These were subsequently removed
- The total hospital benefit, primary provider, radiology, pathology, pharmacy and miscellaneous costs as a percentage of total costs for caesarean and natural deliveries respectively 
- The average hospital benefit, primary provider, radiology, pathology, pharmacy and miscellaneous costs for caesarean and natural deliveries respectively 
- The yearly absolute and percentage change in average hospital benefit, primary provider, radiology, pathology and pharmacy costs

### Related to complications
- The number of mothers who experienced distruption of caesarean section wound 
- The number of mothers who experienced infections of the obstetric wound 
- The number of mothers who experienced obstetic high vaginal laceration
- The number of mothers who experienced perineal lacerations during delivery 
- The number of mothers who experienced complicatiosn of anaesthesia
- The number of mothers who experienced complications associated with HIV 
- The number of mothers who experienced postpartum haemorrhage 
- The number of mothers who experienced other peurperal infections e.g. urinary tract infection 

### Other 
- The proportion of births within each province of South Africa 
- The effect of who the direct paying member is on delivery method (group vs. individual)
- The effect of age on delivery method 

## 4 - Analysis of Infants
This notebook reads in the single data frame relating to the hospital claims data for the infants. It then analyses the following:

- The number of babies who were experienced complications
- The number of complications that were caused during labour and delivery
- The presence of respitory distress syndrome 
    - The total number of infants that experienced respitory distress syndrome
    - The average cost associated with respitory distress syndrome 
    - The percentage of total infant complications attributed to respitory distress syndrome
    - The correlation between respitory distress syndrome and the method of delivery
    - The correlation between respitory distress syndrome and pre-term labour without delivery 
- The presence of HIV
    - The total number of infants that were exposed to HIV
    - The average cost associated with complications of infants that were exposed to HIV
- The presence of feeding problems 
    - The total number of infants who experienced feeding problems 
    - The average cost of infant feeding problems 
    - The correlation between feeding problems and the method of delivery


