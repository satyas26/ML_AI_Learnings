# Practical Application 1 (Coupon Acceptance Analysis)  

## Overview  
This project explores the factors influencing whether drivers accept mobile coupons while driving. The dataset originates from the **UCI Machine Learning Repository**, collected through a survey on Amazon Mechanical Turk. Respondents were asked whether they would accept different types of coupons (restaurants, bars, coffee houses, etc.) under varying conditions such as time of day, weather, passengers, and personal demographics.  

The objective is to identify behavioral patterns and demographic characteristics associated with coupon acceptance.  

---

## Dataset  
The dataset includes three categories of attributes:  

- **User Attributes**  
  - Gender, age, marital status, children, education, occupation, income  
  - Frequency of visiting bars, restaurants, coffee houses, and takeaways  

- **Contextual Attributes**  
  - Destination (home, work, no urgent destination)  
  - Companions (alone, partner, kids, friends)  
  - Weather, temperature, and time of day  

- **Coupon Attributes**  
  - Type of coupon (e.g., cheap restaurants, bar, coffee house, carry out, expensive restaurants)  
  - Expiration time (2 hours or 1 day)  

Target variable: **Coupon Acceptance** (`Y = 1` if accepted, `Y = 0` if not).  

---

## Methodology  
1. **Data Cleaning & Preparation**  
   - Checked for missing values and data consistency.  
   - Recoded categorical variables where necessary.  

2. **Exploratory Data Analysis (EDA)**  
   - Visualized acceptance rates across coupon types.  
   - Explored demographic and contextual differences between accepters and non-accepters.  
   - Segmented analysis for specific coupon types (Bar, Coffee House, and Restaurant < $20).  

3. **Statistical Summaries**  
   - Used proportions and crosstabulations to highlight key differences.  
   - Hypothesis-driven segmentation (e.g., younger drivers vs older, frequency of bar visits).  

---

## Key Findings  
- **Overall Acceptance**: Acceptance rates varied significantly across coupon types. Coffee house and inexpensive restaurant coupons had higher acceptance than bar coupons.  

- **Bar Coupons**:  
  - More likely to be accepted by younger passengers (<30 years old), especially those without children.  
  - Higher acceptance among those who frequent bars more than 3 times per month.  
  - Weather played a role — acceptance was higher on sunny days.  

- **Restaurant (< $20) Coupons** (Independent Investigation):  
  - Had one of the **highest acceptance rates** across all categories.  
  - Acceptance was especially strong among **younger passengers (21–30 years)** and those **with friends**.  
  - Drivers with **no urgent destination** or traveling **with companions** were more likely to redeem these coupons.  
  - Time of day mattered: coupons offered around **lunchtime (2 PM)** had higher uptake compared to morning or evening.  
  - Weather had little impact compared to social and contextual factors.  

- **Contextual Effects**: Passengers were more likely to accept coupons when traveling with friends or partners compared to being alone or with kids.  

- **Demographics**:  
  - Non-widowed individuals showed higher acceptance rates.  
  - Income and occupation had weaker but noticeable influences in some cases.  

---

## Visuals Preview  

Below are selected visualizations from the analysis. For the full set of plots, refer to the Jupyter Notebook.  

### Bar Coupon Investigation  

- **Acceptance by Coupon Type**  
  ![Acceptance by Coupon Type](/Practical_Application_1/images/bar_plot_coupon_type_accepted.png)  
  
- **Acceptance by Frequency of Bar Visits**  
  ![Bar Acceptance by Visits](/Practical_Application_1/images/bar_coupon_freq_bar_visits.png)  

- **Acceptance by Age Group**  
  ![Bar Acceptance by Age](/Practical_Application_1/images/bar_coupon_accept_age.png)  

- **Acceptance by Weather**  
  ![Bar Acceptance by Weather](/Practical_Application_1/images/histogram_temperature_accepted.png)  


### Restaurant (< $20) Coupon Investigation  

- **Overall Acceptance Rate**  
  ![Restaurant (< $20) Coupon Acceptance Overall](/Practical_Application_1/images/restaurant_coupon_acceptance.png)  

- **Acceptance by Companions (Alone, Partner, Kids, Friends)**  
  ![Restaurant Acceptance by Companions](/Practical_Application_1/images/restaurant_coupon_occupancy.png)  

- **Acceptance by Marital Status**  
  ![Restaurant Acceptance by Marital Status](/Practical_Application_1/images/restaurant_coupon_marital_status.png)

- **Restaurant (< $20) Coupon usage by Occupation**  
  ![Restaurant coupon usage by Occupation](/Practical_Application_1/images/restaurant_coupon_gender_occupation.png)

- **Restaurant (< $20) Coupon acceptance by destination**  
  ![Restaurant coupon acceptance by destination](/Practical_Application_1/images/restaurant_coupon_destination.png)   

---

## Conclusion  
The analysis demonstrates that **coupon acceptance is influenced by a mix of personal, contextual, and situational factors**.  

- **Bar Coupons** appealed to younger, socially active passengers without children, especially in good weather.  
- **Restaurant (< $20) Coupons** were broadly popular, particularly among younger groups and when passengers were traveling with friends during lunch hours.  
- Coffee house and inexpensive restaurant coupons showed broader demographic appeal compared to bar coupons.  

These insights can help businesses **target promotions more effectively** by tailoring offers to user profiles and contextual scenarios.  

### Detailed Analysis
- https://github.com/satyas26/ML_AI_Learnings/blob/main/Practical_Application_1/prompt.ipynb