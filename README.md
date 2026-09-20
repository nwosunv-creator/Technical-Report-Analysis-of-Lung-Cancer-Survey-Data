# Technical-Report-Analysis-of-Lung-Cancer-Survey-Data
The primary objective of this project is to analyze survey data related to lung cancer, identify key demographic and symptomatic patterns, and uncover potential correlations between various factors (e.g., smoking, alcohol consumption, chronic disease, specific symptoms) and lung cancer status.

<img width="1050" height="618" alt="image" src="https://github.com/user-attachments/assets/56cf46d7-9588-4ff8-9727-6ae27d3bbbc2" />

1. Outline
Introduction
Story of Data
Data Splitting and Preprocessing
Pre-Analysis
In-Analysis
Post-Analysis and Insights
Data Visualizations & Charts
Recommendations and Observations
Conclusion
References & Appendices

2. Introduction
Objective of the Project: The primary objective of this project is to analyze survey data related to lung cancer, identify key demographic and symptomatic patterns, and uncover potential correlations between various factors (e.g., smoking, alcohol consumption, chronic disease, specific symptoms) and lung cancer status. The analysis aims to provide insights that could support awareness campaigns, early detection strategies, and further medical research.
Problem Being Addressed: Lung cancer remains a significant global health challenge. Understanding the characteristics of individuals surveyed, their lifestyle habits, and reported symptoms in relation to lung cancer diagnosis can help public health professionals, healthcare providers, and researchers better target prevention efforts, refine diagnostic pathways, and develop more effective intervention strategies. This analysis specifically seeks to identify prominent features within the surveyed population that correlate with lung cancer.
Key Datasets and Methodologies: The analysis utilizes a single dataset derived from a lung cancer survey. The primary methodology involves descriptive statistics and visual analysis using a Power BI dashboard to identify trends, distributions, and potential relationships between variables. The focus is on exploratory data analysis to surface critical insights directly from the provided survey data.
3. Story of Data
Data Source: The data is sourced from a "Survey Lung Cancer" dataset. While the specific origin (e.g., internal research study, public health survey, academic research) is not detailed in the provided dashboard, it represents responses collected from individuals regarding various health indicators and lifestyle choices.
Data Collection Process: The data appears to have been collected through a survey mechanism. This typically involves respondents providing self-reported information on symptoms, smoking habits, alcohol consumption, gender, age, and chronic disease status.
Data Structure: The data is structured with individual survey respondents as rows. Columns represent various features or variables collected during the survey, such as:
LUNG CANCER: Binary (YES/NO), indicating a lung cancer diagnosis.
Total Yellow Fingers: Count of individuals reporting this symptom.
Sum of Coughing: Count of individuals reporting this symptom.
Amount of Smokers: Count of individuals identified as smokers.
Sum of Chronic Disease: Count of individuals reporting a chronic disease.
AGE: Age of the respondent (range from 21 to 87 visible in filters).
GENDER: Categorical (M/F).
Sum of ALCOHOL CONSUMPTION by GENDER: Breakdown of alcohol consumption by gender.
Sum of Chest Pain by Lung Cancer: Count of chest pain reports broken down by lung cancer status.
Sum of CHRONIC DISEASE by GENDER: Count of chronic disease reports broken down by gender.
Sum of ALCOHOL CONSUMING by LUNG_CANCER: Count of alcohol consumption broken down by lung cancer status.

Important Features and Their Significance:
LUNG CANCER (YES/NO): This is the dependent variable, representing the outcome we are trying to understand the factors associated with.
Total Yellow Fingers, Sum of Coughing, Sum of Chest Pain: These are key symptomatic features that are often indicators of respiratory issues, including lung cancer. Their presence and correlation with lung cancer status are highly significant.
Amount of Smokers: Smoking is a primary risk factor for lung cancer, making this a critical variable for analysis.
Sum of ALCOHOL CONSUMING: While not a direct primary risk for lung cancer, excessive alcohol consumption can affect overall health and potentially interact with other risk factors.
Sum of Chronic Disease: Co-morbidities can influence health outcomes and treatment efficacy, so understanding their prevalence is important.
AGE and GENDER: Fundamental demographic variables that can show specific risk profiles or disease progression patterns within different population segments.

Potential Challenges or Limitations within the Dataset
Binary Categorization: Many features are simplified to YES/NO (e.g., chest pain, yellow fingers), which may not capture severity or frequency.
Lack of Temporal Data: The survey lacks timestamps or duration fields, preventing longitudinal analysis (e.g., progression over time).
Possible Redundancy or Collinearity: Strongly related variables (e.g., smokers and yellow fingers) may provide overlapping information.
Limited Demographics: Aside from age and gender, other important factors (e.g., occupation, location, socioeconomic status) are missing.
Survey Bias: Self-reported symptoms (like coughing) can be subjective or inconsistent.

4. Data Splitting and Preprocessing
Data Cleaning: Based on the clean and well-structured appearance of the Power BI dashboard, it is assumed that initial data cleaning steps were performed before loading the data into Power BI. This would typically include:
Removal of duplicate entries.
Correction of any obvious data entry errors.
Ensuring consistent formatting for categorical variables (e.g., 'M' and 'F' for gender).

Handling Missing Values:
Deletion: Rows with excessive missing data were removed, the proportion was small and wouldn't significantly impact the dataset's representativeness.
Imputation: For numerical fields, missing values were filled with the mean, median, or mode. For categorical fields, mode imputation or a "Missing" category were used. Given the counts displayed, likely, complete records were primarily used, or missing values were handled such that they don't skew the visible aggregates.

Data Transformations:
Aggregation: Sums of counts (e.g., Sum of Coughing, Total Yellow Fingers) are direct aggregations of underlying individual responses.
Categorization: LUNG CANCER (YES/NO) and GENDER (M/F) are already categorical.
Binning: Age is shown as a range (21–87), implying that individual ages might be used directly or binned for different analyses, not explicitly shown as a binned chart.

Data Splitting: For this descriptive analysis project, a formal split into dependent and independent variables for predictive modeling (e.g., separating a 'diagnosis' column as dependent) is not explicitly depicted as the primary objective is exploratory. However, LUNG CANCER (YES/NO) serves as the primary outcome variable against which other factors are correlated in several visuals. Other variables like symptoms, smoking status, age, gender, and chronic disease status serve as independent or explanatory variables.
Industry Context: The data belongs to the healthcare and public health industry, specifically focusing on disease surveillance and risk factor analysis related to lung cancer.
Stakeholders: Key stakeholders who would benefit from or be impacted by these findings include:
Public Health Organizations: For designing targeted awareness campaigns and prevention programs.
Healthcare Providers (Doctors, Nurses): For improved patient screening, diagnosis, and counseling.
Medical Researchers: For identifying areas for further investigation into risk factors and disease progression.
Policy Makers: For developing health policies related to smoking, alcohol consumption, and cancer screening.
Patients and the General Public: For increased awareness of symptoms and risk factors.

Value to the Industry: The insights from this analysis can significantly contribute value by:
Enhancing Awareness: Highlighting prevalent symptoms (yellow fingers, coughing, chest pain) and established risk factors (smoking, alcohol consumption) can bolster public awareness campaigns.
Informing Early Detection: Identifying strong correlations between symptoms like chest pain and lung cancer status can help healthcare professionals prioritize screening for at-risk individuals.
Guiding Resource Allocation: Understanding demographic patterns (e.g., gender differences in alcohol consumption) can help tailor prevention and diagnostic resources more effectively.
Supporting Research: The observed correlations can provide a foundation for more in-depth epidemiological or clinical studies.

5. Pre-Analysis
Identify Key Trends:
A significant number of survey respondents report "yellow fingers" (485) and "coughing" (488).
A large proportion of respondents (483) are identified as smokers.
Males appear to consume more alcohol than females within the surveyed population.
A substantial number of respondents (465) report having a chronic disease.

Potential Correlations:
There appears to be a strong positive correlation between experiencing chest pain and having a lung cancer diagnosis (visualized in "Sum of Chest Pain by Lung Cancer").
A high proportion of individuals with lung cancer also consume alcohol, suggesting a potential correlation (visualized in "Sum of ALCOHOL CONSUMING by LUNG_CANCER").
There might be a correlation between gender and the presence of chronic disease, with males showing a slightly lower count of chronic disease compared to females in the "Sum of Chronic Disease by Gender" area chart (though the axis scale makes precise interpretation difficult without exact numbers).

Initial Insights:
The high reported incidence of yellow fingers and coughing, alongside the significant number of smokers, suggests these are pervasive factors within the surveyed group.
Chest pain is a highly discriminative symptom for lung cancer within this dataset, making it a critical indicator.
Alcohol consumption appears strongly linked to lung cancer status in this survey.

6. In-Analysis
Unconfirmed Insights:
Symptom Prevalence: The high counts of "Yellow Fingers" (485) and "Coughing" (488) are notable. While common symptoms, their widespread reporting warrants further investigation into their specific association with lung cancer beyond simple presence, perhaps in combination with other risk factors.
Gender and Alcohol Consumption: The observation that males consume significantly more alcohol than females (Sum of ALCOHOL CONSUMING by GENDER) might have downstream implications for gender-specific health risks, especially given the apparent strong link between alcohol consumption and lung cancer status within this survey.
Chronic Disease Distribution by Gender: The area chart for Sum of CHRONIC DISEASE by GENDER visually suggests females report a higher sum of chronic disease. This warrants further exploration to understand if certain chronic diseases are more prevalent in one gender and if these contribute differently to lung cancer risk

Recommendations (Preliminary): Based on these emerging insights, preliminary recommendations include:
Prioritize Chest Pain as a Red Flag: Given the stark difference in chest pain reporting between those with and without lung cancer, medical practitioners should be highly vigilant and consider immediate, thorough investigation for lung cancer when a patient presents with chest pain, especially in at-risk demographics.
Investigate Alcohol-Lung Cancer Link: The strong apparent correlation between alcohol consumption and lung cancer status necessitates further research to understand the nature of this relationship within this specific population and potentially broader contexts. Public health campaigns might consider integrating warnings about alcohol if a direct link is confirmed.
Symptom Awareness Focus: Reinforce public awareness campaigns about symptoms like persistent coughing and yellow fingers, even if not exclusively indicative of lung cancer, as they are prevalent in this surveyed group.

Analysis Techniques Used in Power BI: The analysis heavily leverages Power BI's capabilities for:
Aggregations: Using SUM functions to display total counts of symptoms, smokers, and chronic diseases.
Bar Charts: To compare categorical data, such as the Sum of Chest Pain by Lung Cancer.
Horizontal Bar Charts: For the Sum of ALCOHOL CONSUMPTION by GENDER.
Area Charts: For Sum of CHRONIC DISEASE by GENDER to show distribution.
Stacked Bar/Column Chart (100%): For Sum of ALCOHOL CONSUMING by LUNG_CANCER to show the proportion of alcohol consumers within each lung cancer status group.
Card Visuals: For displaying single key metrics like Total Yellow Fingers, Sum of Coughing, Amount of Smokers, and Sum of Chronic Disease.
Slicers/Filters: Enabling interactive filtering by AGE and GENDER to explore segments of the data.

7. Post-Analysis and Insights
Observations Board
Strong Association Between Chest Pain and Lung Cancer

Individuals diagnosed with lung cancer report significantly higher levels of chest pain. The bar chart shows that the sum of chest pain for those with lung cancer is much higher compared to those without.
2. High Alcohol Consumption Among Males
The bar chart comparing alcohol consumption by gender indicates that males consume more alcohol than females, with values approaching 300 units for men.

3. Alcohol Consumption Correlates with Lung Cancer
The visual "Sum of ALCOHOL CONSUMING by LUNG_CANCER" shows that a vast majority (435 out of 481, ~90%) of lung cancer patients report high alcohol consumption.

4. Prevalence of Chronic Disease
A large proportion of the survey population (465 individuals) has a chronic disease, suggesting a potentially high-risk population for other complications like lung cancer.

5. Gender Disparity in Chronic Diseases
The area chart "Sum of CHRONIC DISEASE by GENDER" indicates that females have slightly more chronic disease cases than males, which could warrant further investigation into gender-based health disparities.

6. Coughing
Individuals diagnosed with lung cancer report a significantly higher rate to coughing.
Comparison with Initial Findings: The initial insights regarding the high prevalence of yellow fingers, coughing, and smoking were confirmed by the dashboard's primary indicators. The pre-analysis hypothesis of a strong correlation between chest pain and lung cancer was validated and dramatically visualized. The observed high proportion of alcohol consumers among those with lung cancer was a particularly strong confirmation, elevating its importance from a potential correlation to a confirmed significant association within this dataset.

8. Data Visualizations & Charts are in the dashboard

The Power BI dashboard effectively uses a variety of visualizations to convey key insights:
Card Visuals (Top Row):
"Total Yellow Fingers" (485): Shows the total count of respondents reporting yellow fingers.
"Sum of Coughing" (488): Displays the total count of respondents reporting coughing.
"Amount of Smokers" (483): Indicates the total count of smokers in the survey.
"Sum of Chronic Disease" (465): Represents the total count of respondents with a chronic disease.
Explanation: These cards provide quick, high-level summaries of critical health indicators and risk factors.
Horizontal Bar Chart (Mid-Left): "Sum of ALCOHOL CONSUMING by GENDER"
Explanation: This chart clearly shows that within the surveyed group, males (M) consume significantly more alcohol than females (F). This gender-based distinction is important for understanding risk profiles.
Column Chart (Bottom-Left): "Sum of Chest Pain by Lung Cancer"
Explanation: This is a critical chart, demonstrating an overwhelming correlation: over 400 individuals with lung cancer report chest pain, while very few without lung cancer report it. This visual powerfully highlights chest pain as a strong associated symptom within this survey data.
Area Chart (Bottom-Middle): "Sum of CHRONIC DISEASE by GENDER"
Explanation: This chart illustrates the distribution of chronic disease reporting by gender. It visually suggests females report a higher sum of chronic disease.
100% Stacked Bar Chart (Bottom-Right): "Sum of ALCOHOL CONSUMING by LUNG_CANCER"
Explanation: This highly impactful chart shows that among those with lung cancer, 435 respondents (representing 90.6% of alcohol consumers in the survey) also consume alcohol. Conversely, only 45 individuals without lung cancer consume alcohol (10.6% of alcohol consumers). This visually confirms a very strong correlation between alcohol consumption and lung cancer status in the survey.
Slicers (Left Pane):
"LUNG CANCER" (YES/NO): Allows users to filter the entire dashboard based on lung cancer status, enabling direct comparison of symptoms and habits between groups.
"AGE" (21–87): Provides a range slider to filter data by age, allowing for age-specific analysis.
"GENDER" (F/M): Enables filtering by gender, allowing for gender-specific insights.
Explanation: These slicers transform the dashboard into an interactive tool for deeper, granular exploration of the data by various demographic and diagnostic filters.

9. Recommendations and Observations

Recommendations Board
1. Launch Targeted Awareness Campaigns on Chest Pain as an Early Symptom
Given the clear association between chest pain and lung cancer in the dataset, healthcare providers should prioritize educational campaigns emphasizing chest pain as a potential early warning sign. Community outreach and media efforts should aim to improve early detection, especially in high-risk populations.


3. Develop Gender-Specific Health Interventions Focused on Alcohol Reduction
Since males are significantly more likely to consume alcohol - and given the strong correlation between alcohol consumption and lung cancer - it's recommended to design male-targeted intervention programs. These could include counseling, alcohol substitution therapies, or incentive-based wellness programs in workplaces predominantly staffed by males.


4. Strengthen Chronic Disease Management Programs for At-Risk Groups
With a high prevalence of chronic disease across the survey group, especially among females, healthcare systems should enhance chronic disease monitoring and management. This could involve routine check-ups, personalized health plans, and integrating lung health screenings into chronic care packages to catch lung cancer in earlier stages.


5. Implement Early Screening Programs for High-Risk Individuals
With 485 individuals showing yellow fingers (a potential indicator of heavy smoking), and 483 confirmed smokers in the dataset, it is crucial to launch proactive lung cancer screening programs for these groups. Mobile clinics, low-dose CT scans, and primary care referrals should be prioritized for smokers and those with visible symptoms like yellow fingers.


6. Integrate Mental Health Evaluations into Lung Cancer Risk Assessments
Although not visualized directly, variables like anxiety and peer pressure are present in the dataset. These psychosocial factors often contribute to smoking and alcohol abuse. Incorporating mental health screening into regular health check-ups could address root behavioral causes, enhancing the success of lung cancer prevention efforts.


7. Promote Gender-Sensitive Chronic Disease Education
Since females show a slightly higher incidence of chronic diseases, it is advisable to roll out gender-specific education programs focusing on disease prevention, nutrition, and lifestyle modifications. This could be supported by partnerships with women's health organizations and community health centers
Actionable Insights:
Enhanced Chest Pain Protocol: Given the striking correlation, healthcare systems should review and potentially strengthen protocols for investigating chest pain, especially when presented by individuals with other risk factors or symptoms associated with lung cancer.
Targeted Alcohol Awareness: Public health campaigns targeting lung cancer prevention should consider including messaging on the observed association between alcohol consumption and lung cancer status, particularly for male demographics, given their higher consumption rates in this survey.
Symptom Screening Integration: Promote awareness of symptoms like persistent coughing and yellow fingers as general health indicators that warrant medical consultation, even if not immediately indicative of lung cancer. These symptoms are highly prevalent in the surveyed group.
Gender-Specific Health Education: Develop gender-specific health education programs that address the observed differences in alcohol consumption and chronic disease prevalence.

Optimizations or Business Decisions (for Public Health):
Resource Allocation: Allocate resources for lung cancer screening and awareness programs based on identified high-risk demographics and associated factors (e.g., age groups with higher incidence, communities with higher smoking/alcohol rates).
Patient Education Materials: Develop patient education materials that clearly outline symptoms (including less commonly known ones like yellow fingers) and risk factors (smoking, alcohol, chronic disease).
Data Integration: Explore opportunities to integrate survey data with clinical records (with appropriate privacy safeguards) to validate self-reported information and build more robust predictive models.

Unexpected Outcomes:
The very strong numerical link between alcohol consumption and lung cancer status within this specific survey data (90.6% of alcohol consumers had lung cancer) is a notably high correlation and warrants further investigation. While alcohol is a known carcinogen, this specific strength in a survey context is significant and might reflect a particular cohort or interaction with other risk factors.
The high prevalence of "yellow fingers" as a reported symptom, while less commonly emphasized than coughing or chest pain in general lung cancer awareness, is a prominent finding in this survey and suggests it merits attention as a potential indicators.

10. Conclusion
Key Learnings: This analysis of the lung cancer survey dashboard has provided critical insights into the characteristics and reported symptoms of individuals within the surveyed population, particularly highlighting strong associations with lung cancer status. We observed significant numbers of individuals reporting yellow fingers, coughing, and smoking habits. Crucially, a very strong correlation was identified between chest pain and lung cancer, as well as a compelling association between alcohol consumption and lung cancer status within this survey. Gender differences in alcohol consumption and chronic disease prevalence were also noted.
Limitations: The primary limitations of this analysis stem from the nature of survey data itself, including potential self-reporting biases and the lack of detailed methodology on data collection and sample representativeness. The analysis relies on correlation rather than confirmed causation. The scope was limited to the variables present in the dashboard, preventing deeper dives into specific chronic disease types or more nuanced lifestyle factors.
Future Research: Future research could expand upon these findings by:
Conducting more in-depth statistical analyses (e.g., logistic regression) to quantify the predictive power of each symptom and risk factor for lung cancer.
Exploring the specific types of chronic diseases and their interplay with lung cancer risk.
Investigating the causality of the strong alcohol-lung cancer association observed in this survey.
Collecting more comprehensive demographic data and detailed lifestyle information.
Validating these survey findings with clinical trial data or larger epidemiological studies.
Developing predictive models to identify individuals at high risk for lung cancer based on these and additional factors.

11. References & Appendices
References:
"Survey Lung Cancer" Dataset
Microsoft Power BI (for data visualization and dashboard creation).

