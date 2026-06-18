# -medicare-hospital-billing-analysis
End-to-end analysis of US Medicare inpatient hospital billing patterns using Python and Tableau. Covers charge inflation, provider outliers, geographic variation, and patient burden.

**Tools:** Python, Pandas, Matplotlib, Seaborn, Tableau Public
**Data Source:** CMS Medicare Inpatient Hospitals by Provider and Service 
(2023), available at data.cms.gov
## Live Dashboard
https://public.tableau.com/app/profile/colleta.wamalwa8497/viz/MedicareHospitalBillingAnalysis2023/Dashboard1 
## Key Findings
- The national average charge-to-payment ratio is 5.17x, meaning hospitals 
  bill over 5 times what Medicare pays on average
- Nevada is the most inflated state at 9.34x, nearly double the national average
- Capital Health Medical Center in Hopewell, NJ appears in 10 of the top 15 
  worst hospital outliers across unrelated DRGs, indicating systematic 
  overpricing rather than procedure-specific cost factors
- 9.73% of hospital-DRG combinations exceed 2x the national median ratio for the same procedure
- Urban patients face an average out-of-pocket burden of 3,525 compared 
  to 1,662 for rural patients, more than double
- 222 hospitals (0.15%) were identified as Critical Access or Tribal 
  facilities operating under non-standard Medicare payment models and 
  excluded from the main analysis
  ## Analysis Sections
1. **DRG-Level Charge Inflation** - Which procedures are most overpriced nationally
2. **High-Risk DRGs** - Procedures combining high volume and high inflation
3. **State-Level Analysis** - Geographic variation in billing practices
4. **Hospital Outlier Detection** - Hospitals charging significantly above 
   national median for the same procedure
5. **Rural vs Urban Comparison** - How location type affects cost and 
   patient burden
   ## Data Notes
- Dataset: CMS Medicare Inpatient Hospitals by Provider and Service (2023)
- Records after cleaning: 145,078 standard hospital records
- 222 Critical Access and Tribal hospitals excluded from main analysis 
  and retained as a separate segment
- Negative cost gaps investigated and explained rather than deleted
- Custom null handling applied at data load
