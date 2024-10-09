# Skyhack Hackathon: Call Center Optimization

## Project Overview

This project focuses on analyzing and optimizing call handling times for a call center dataset. The goal is to improve call efficiency by exploring factors that contribute to long Average Handle Time (AHT) and Average Speed to Answer (AST), identify self-solvable issues for IVR optimization, and categorize primary call reasons into broader groups for more efficient call routing.

### Key Deliverables
1. *Exploring Factors Contributing to Long AHT and AST*
2. *Identifying Self-Solvable Issues for IVR Optimization*
3. *Categorizing Call Reasons for Enhanced Operational Efficiency*

---

## Dataset Description
The dataset consists of multiple data files, including:
- calls_dataframe.csv: Contains details of each call such as call start time, agent assignment, and call end time.
- customers_df.csv: Customer details including name and elite level.
- reasons_df.csv: Primary reasons for each call.
- sentiment_df.csv: Sentiment analysis of the call transcripts, including customer and agent tones.
- test_df.csv: Contains test call IDs for which the primary reasons need to be predicted.

---

## Analysis and Key Insights

### Deliverable 1: Exploring Factors Contributing to Long AHT and AST
1. *Overall Average Handle Time (AHT)*:  
   - *1134.12 seconds* (18.90 minutes)

2. *Overall Average Speed to Answer (AST)*:  
   - *437.07 seconds* (7.28 minutes)

3. *Key Factors Contributing to Long AHT and AST*:
   - *Agent Performance*:  
     - Significant variations in handle time among agents.
     - Some agents have an average handle time of over 4000 seconds, indicating training needs or complex calls.
   - *Call Reasons*:  
     - *Post-Flight Issues* and *Cancellation and Changes* contribute the most to extended handle times.
     - *Baggage and Traveler Updates* have the highest average speed to answer, suggesting that these calls require more preparation before engaging the customer.

4. *Impact of Sentiment on AHT and AST*:  
   - *Silence Percentage* has a *positive correlation* of *0.4* with handle time, suggesting that a higher percentage of silence during a call is linked to longer handle times.
   - *Sentiment Analysis* shows a weak negative correlation with handle time, meaning that sentiment alone does not significantly affect call durations.

5. *Percentage Difference Between Most Frequent and Least Frequent Call Reasons*:  
   - *Most Frequent Call Reason*: Cancellation and Changes  
   - *Least Frequent Call Reason*: Accessibility Services  
   - *Percentage Difference in AHT: **46.67%*

### Deliverable 2: Identifying Self-Solvable Issues for IVR Optimization
1. *Self-Solvable Issues Identified*:
   - Recurring self-solvable call reasons include *IRROPS, **Voluntary Change, **Seating, and **Mileage Plus*.

2. *Suggested IVR Improvements*:
   - *IRROPS (Irregular Operations)*: Add IVR options for automatic flight rescheduling and cancellations.
   - *Voluntary Changes*: Provide self-service options for flight changes, cancellations, and modifications.
   - *Mileage Plus*: Include options for customers to manage their loyalty program points, account details, and redemption options.
   - *Seating*: Create self-service menus for seat selection and upgrades.
   - *Baggage*: Automate the process of baggage claim and status tracking.

3. *Sentiment-Based Recommendations*:
   - Identified over *33,409* calls with neutral or positive sentiments that can be routed to IVR for self-service, significantly reducing agent workload.

### Deliverable 3: Categorizing Call Reasons for Enhanced Operational Efficiency
1. *Broader Categories Created*:
   - Mapped the detailed primary reasons into *7 broader categories*:
     1. Cancellation and Changes
     2. Booking Issues
     3. Upgrades and Seating
     4. Post-Flight Issues
     5. Customer Support
     6. Baggage and Traveler Updates
     7. Accessibility Services

2. *Impact on AHT and AST*:
   - *Cancellation and Changes* and *Post-Flight Issues* have the highest AHT.
   - *Baggage and Traveler Updates* have the highest AST, suggesting delays in agent assignment for these calls.

### Final Recommendations
1. *Focus on Reducing AHT for Complex Categories*:
   - Improve call handling for *Post-Flight Issues* and *Cancellations* by optimizing workflows and providing additional resources.

2. *IVR Optimization*:
   - Develop a detailed IVR menu structure that covers the most common call types and offers more self-service options.

3. *Agent Performance Optimization*:
   - Provide targeted training for agents with high AHT deviations to reduce performance gaps.

4. *Further Investigation*:
   - Explore additional features such as agent expertise, call complexity, and call duration patterns to improve predictive models for AHT and AST.

---

## Technical Details

### Project Setup
1. *Python Version*: 3.8+
2. *Libraries Required*:
   - pandas
   - numpy
   - matplotlib
   - seaborn
   - scikit-learn
   - re

### Running the Code
1. Clone the repository.
2. Install the necessary libraries using:
   ```bash
   pip install -r requirements.txt

### Run the main analysis file to generate insights and outputs:
    jupyter notebook skyhack.ipynb
The predictions for the test file will be saved as test.csv in the project directory.
Final Output
The final deliverable includes a detailed report and a test.csv file with the predicted primary call reasons for each call in the test dataset.# skyhackk
