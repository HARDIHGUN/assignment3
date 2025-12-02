# Loan Approval Visualization

The goal is to explore how loan approval status (Approved vs Rejected) relates to:
- Average credit score
- Average annual income
- Average loan amount

These metrics are shown in a single grouped bar chart



## Dataset
 Loan_approval_data_2025.csv  

Main columns used:

- loan_status – 0 = Rejected, 1 = Approved  
- credit_score – numeric credit score of the applicant  
- annual_income – numeric annual income  
- loan_amount – numeric loan amount requested  

In the visualization, I aggregate the data in D3 to compute average values for each metric per loan_status

## Visualization Description

The main visualization is a grouped bar chart:

- X-axis: Loan status
  - Approved
  - Rejected
- Groups of bars for each status:
  - Average Credit Score (blue)
  - Average Annual Income (orange)
  - Average Loan Amount (red)
- Y-axis: Average value of the metric

### Visual Channel

- X Position: Encodes the loan status category
- Y Position: Encodes the magnitude of the average metric
- Color: Encodes which metric is shown (credit score, income, or loan amount)
- Length of bar: Represents the value of the average

### Interaction  
  Bars start at height 0 and grow up to their final height using a D3 transition 
  When hovering a bar, a tooltip shows:
  - Loan status (Approved / Rejected)
  - Metric name
  - Exact average value (rounded to two decimals)
