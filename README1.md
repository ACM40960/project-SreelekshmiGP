# Unraveling COVID-19 Dynamics in the UK:Insights from Multivariate Analysis

In the tumultuous climate of the **COVID-19** pandemic, nations globally faced unparalleled public health trials, 
with the UK standing out as one of the most significantly affected. This project seeks to deeply investigate the 
palpable effects of the vaccination campaign on COVID-19 metrics like infections, hospitalizations, and mortality 
rates in the UK. Through multivariate linear regression analyses of data spanning pre-vaccination and vaccination 
periods, we aim to unravel the real-world efficacy of vaccines while accounting for other external influences like human 
mobility and weather patterns. Our findings aspire to shape public health policies by emphasizing the crucial role of 
vaccinations in our fight against the pandemic.

### Data:

Our principal dataset for this investigation is acquired from Google's extensive open data collection, which chronicles 
COVID-19 details for a plethora of nations. For the purpose of our study, we focused on extracting data pertinent to the UK, 
delving into its unique COVID-19 landscape. This rich dataset encapsulates a wide array of variables, including but not limited 
to confirmed cases, mortality rates, testing frequencies, hospitalization statistics, vaccination data, mobility trends, 
meteorological metrics, and the government's stringency index. The comprehensive nature of this data repository offers us an unparalleled 
window into the multifaceted dynamics of COVID-19, enriching the analytical depth of our project.

**Our analysis segregates the data timeline into two pivotal eras:** the pre-vaccination and the vaccination stages. 
This bifurcation aids in a granular examination of various influencers like testing frequencies, mobility trajectories, 
stringency policies, and meteorological patterns across these two distinct phases. As we transition into the vaccination epoch, our scrutiny 
deepens to encapsulate the direct repercussions of vaccination on the metrics of confirmed cases, fatalities, and hospitalizations.

To convey these intricate trends with clarity, we've adopted a visually driven strategy. For the antecedent pre-vaccination timeline, we delineate 
the progression of cases chronologically in one visual, while juxtaposing hospitalizations and deaths in a separate representation. As we pivot to 
the vaccination phase, our visualization strategy evolves. Here, we present a comparative view, superimposing counts of cases, hospitalizations, 
and deaths against the backdrop of vaccination rates.

### Files in the Repository:

- `UK Pre vaccination period.csv`: This CSV file contains data specific to the UK's pre-vaccination phase, documenting the COVID-19 statistics
  prior to the initiation of vaccination campaigns.

- `UK Vaccination period.csv`: This CSV file is dedicated to the UK's vaccination period, providing insights into the COVID-19 metrics post the
  commencement of vaccination drives.

- `Data book.docx`: An explanatory document that elucidates the variables incorporated within the datasets. It offers a comprehensive breakdown of
  each variable, aiding in understanding the structure and significance of the data.

- `Code and Interpretation.Rmd`: This R markdown file embodies the heart of the project. It encompasses all the R code utilised for data analysis, 
  modeling, and visualization, alongside detailed interpretations and conclusions drawn from the results.

- `Code-and-Interpretation.pdf`: A PDF rendition of the aforementioned Rmd file. It presents the entire project in a readable, portable format, ensuring 
  accessibility even for those without RStudio.

### Dependencies:

This project relies on several R packages to handle, visualise, and analyse the data. Here's a list of the essential dependencies:

- `ggplot2`: A powerful visualisation tool to create complex and aesthetically pleasing graphics.

- `cowplot`: Enhances the visual experience by providing functionalities to arrange and annotate multiple ggplot objects.

- `tidyverse`: An umbrella package that includes a collection of R packages designed for data science.

- `caret`: Short for 'Classification And REgression Training', this package facilitates data splitting, pre-processing, and model training.

It's recommended to ensure all these packages are installed and updated to their latest versions for seamless execution and reproduction of the project.

### Method:

Our endeavour to understand the profound impact of COVID-19 vaccinations in the UK led us to utilise ___Multivariate Linear Regression (MLR)___, a potent 
statistical technique adept at revealing intricate relationships among multiple variables. Prior to delving into the specifics for the UK, we carefully 
scrutinized the main dataset for **multicollinearity**. By identifying and removing correlated independent variables and static variables, we ensured the 
robustness of our subsequent analyses. Post this essential preprocessing step, we partitioned the data into two distinct phases for the UK - pre-vaccination 
and vaccination period - capturing the evolving dynamics of the pandemic.

The process we followed encompassed several pivotal steps:

- Data Preprocessing: Beyond the initial multicollinearity assessment, we meticulously managed missing data, cleaned our datasets, and ensured their uniformity.

- Exploratory Data Analysis (EDA): This phase involved delving deep into variable distributions, discerning relationships, and identifying potential outliers 
  to build a comprehensive understanding of our data.

- Model Building: Harnessing the power of MLR, we constructed models for both pre-vaccination and vaccination periods, aiming to capture the multifaceted 
  influences on infection rates, hospitalizations, and fatalities.

- Model Evaluation: Our models were put to the test. We gauged their efficacy using metrics like R-squared and employed cross-validation techniques for a 
  holistic assessment.

- Comparison Analysis: A comparative study between our models allowed us to discern the tangible impacts of vaccination campaigns, providing clarity on 
its role amidst other influencing factors.

The analytical might of MVR, combined with our structured approach and diligent data pre-processing, offered invaluable insights into the pandemic's dynamics, 
showcasing the multifaceted dimensions of the pandemic in the UK.

### Results:

#### 1. Pre-Vaccination Analysis:

**Method:** Employed __Multivariate Linear Regression__ to analyze relationships between COVID-19 outcomes and various predictors including testing rates, mobility 
patterns, weather metrics, and the stringency index.

**Performance:** Achieved a Mean Squared Error of 0.102 on test data with an R-squared value of approximately 0.80 or higher for each response.The Root Mean Squared Error 
(RMSE) obtained is 0.3207. Thus, the model seems to perform well on the pre-vaccination data, as indicated by a high R<sup>2</sup> value and relatively low error metrics (MSE and RMSE). 
The high R<sup>2</sup> value indicates that the model explains a significant amount of variance in the data.

**Key Findings:**

- Strong positive correlation between cumulative tests and confirmed cases, deceased cases, and hospitalized patients.

- Higher stringency index values correlated with an increase in cases.

- Mobility reductions, especially in retail and transit stations, showed a negative correlation with case numbers.



#### 2. Vaccination Period Analysis:

**Method:** Extended the multivariate regression analysis to capture the dynamics post-vaccination.

**Performance:** Demonstrated an improved Mean Squared Error of 0.0702 on test data with R-squared values consistently over 0.80.The Root Mean Squared Error 
(RMSE) obtained is 0.2692. The model's performance on the vaccination data is even better than its performance on the pre-vaccination data. This is evident from 
the improved (lower) error metrics (both MSE and RMSE) and the consistently high R<sup>2</sup> values. The improvements suggest that the model is more accurate in
predicting outcomes during the vaccination period compared to the pre-vaccination period.

**Key Findings:**

- Significant negative correlation between the number of vaccinated individuals and infection cases, deceased cases, and hospitalizations.

- Decline in transit station activity correlated with reduced cases and hospitalizations.

- Testing rates remained pivotal in affecting case numbers, even post-vaccination.

### Authors:

Sreelekshmi Girijadevi Purushothaman(22200034)

Vinothini Balasubramani(22202390)

### References:

1. Richard A. Johnson and Dean W. Wichern. [Multivariate Linear Regression Models in Applied Multivariate Statistical Analysis](https://ostad.hormozgan.ac.ir/ostad/UploadedFiles/863845/97050509-3761826667770356.pdf). (6th ed.) 360-418 Pearson Prentice Hall,2007.

2. R. Suganya, R.Arunadevi, & Seyed M.Buhari. [COVID-19 Forecasting using Multivariate Linear Regression](https://www.researchsquare.com/article/rs-71963/v1). Research Square.

3. Lewis, F.I., Ward, M.P. [Improving epidemiologic data analyses through multivariate regression modelling](https://doi.org/10.1186/1742-7622-10-4). Emerg Themes Epidemiol 10, 4 (2013). 

4. Keeling MJ, Dyson L, Guyver-Fletcher G, et al. [Fitting to the UK COVID-19 outbreak, short-term forecasts and estimating the reproductive number](https://journals.sagepub.com/doi/full/10.1177/09622802211070257). Statistical Methods in Medical Research. 2022;31(9):1716-1737. doi:10.1177/09622802211070257

5. Rencher, Alvin C. [Methods of Multivariate Analysis](https://www.ipen.br/biblioteca/slr/cel/0241). 2nd ed., John Wiley & Sons, Inc., 2002, pp. 337-339.

6. Dataset source: Google - [Covid19 Open Data](https://storage.googleapis.com/covid19-open-data/v3/location/GB.csv)
