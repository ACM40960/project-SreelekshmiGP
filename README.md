<div align="center">
    <img src="Images/Header.jpg" alt="Title" width="950" height="225">
</div>
<br>

In the tumultuous climate of the COVID-19 pandemic, nations globally faced unparalleled public health trials, with the UK standing out as one of the most significantly affected. This project seeks to deeply investigate the palpable effects of the vaccination campaign on COVID-19 metrics like infections, hospitalizations, and mortality rates in the UK. Through multivariate linear regression analyses of data spanning pre-vaccination and vaccination periods, we aim to unravel the real-world efficacy of vaccines while accounting for other external influences like human mobility and weather patterns. Our findings aspire to shape public health policies by emphasizing the crucial role of vaccinations in our fight against the pandemic.

## Overview

🚀 **Introduction**: This project offers a comprehensive exploration of the distinctive challenges presented by the COVID-19 pandemic, with a particular emphasis on understanding the context and outcomes within the UK. By delving into the experiences and responses of the UK in the face of this global crisis, the project seeks to unravel the intricate dynamics that have shaped the nation's journey through the pandemic. This approach provides an insightful lens through which to examine the multifaceted aspects of public health, policy interventions, and societal resilience.

💡 **Objectives**: 
-	Analyze the correlation between vaccination rates and COVID-19 outcomes in the UK.
-	Explore the impact of human mobility on the virus's transmission during pre-vaccination and vaccination periods.
-	Examine potential associations between weather patterns and COVID-19 metrics to elucidate any indirect influences.

## Data Exploration

🗄️ **Data Source**: Our principal dataset for this investigation is acquired from Google's extensive open data collection, which chronicles COVID-19 details for a plethora of nations. For our study, we focused on extracting data pertinent to the UK, delving into its unique COVID-19 landscape. This rich dataset encapsulates a wide array of variables, including but not limited to confirmed cases, mortality rates, testing frequencies, hospitalization statistics, vaccination data, mobility trends, meteorological metrics, and the government's stringency index. The comprehensive nature of this data repository offers us an unparalleled window into the multifaceted dynamics of COVID-19, enriching the analytical depth of our project.

✂️ **Data Segmentation**: Our analysis segregates the data timeline into two pivotal eras - the _pre-vaccination_ and the _vaccination stages_. This bifurcation aids in a granular examination of various influencers like testing frequencies, mobility trajectories, stringency policies, and meteorological patterns across these two distinct phases. As we transition into the vaccination epoch, our scrutiny deepens to encapsulate the direct repercussions of vaccination on the metrics of confirmed cases, fatalities, and hospitalizations. 

## Methodology

Our endeavor to understand the profound impact of COVID-19 vaccinations in the UK led us to utilize **Multivariate Linear Regression (MLR)**, a potent statistical technique adept at revealing intricate relationships among multiple variables. Prior to delving into the specifics for the UK, we scrutinized the main dataset for multicollinearity. By identifying and removing correlated independent variables and static variables, we ensured the robustness of our subsequent analyses. Post this essential preprocessing step, we partitioned the data into two distinct phases for the UK - pre-vaccination and vaccination period capturing the evolving dynamics of the pandemic.

The implementation of the Multivariate Linear Regression (MLR) method involves the following steps:

🔍 **Data Preprocessing**: Beyond the initial multicollinearity assessment, we meticulously managed missing data, cleaned our datasets, and ensured their uniformity.

📊 **Exploratory Data Analysis (EDA):** This phase involved delving deep into variable distributions, discerning relationships, and identifying potential outliers to build a comprehensive understanding of our data.

#### The plots shown below help to understand the trends of cases, hospitalizations, and deaths in the pre-vaccination data set:

![Pre Vaccination Trends](Images/Pre%20Vaccination%20Trends.jpg)

A discernible trend is evident in the pre-vaccination data set: as the days progress, there is a marked increase in the number of cases, hospitalizations, and deaths.

#### The plots shown below help to understand the trends of cases, hospitalizations, and deaths in the vaccination data set:

![Vaccination Trends](Images/Vaccination%20Trends.jpg)

In the vaccination data set, there is a conspicuous decline in the number of cases, hospitalizations, and deaths as the days unfold.

🧱 **Model Building:** Harnessing the power of MLR, we constructed models for both pre-vaccination and vaccination periods, aiming to capture the multifaceted influences on infection rates, hospitalizations, and fatalities.

✅ **Model Evaluation:** Our models were put to the test. We gauged their efficacy using metrics like R-squared and employed cross-validation techniques for a holistic assessment.

📑 **Comparison Analysis:** A comparative study between our models allowed us to discern the tangible impacts of vaccination campaigns, providing clarity on its role amidst other influencing factors.

The analytical might of MLR, combined with our structured approach and diligent data pre-processing, offered invaluable insights into the pandemic's dynamics, showcasing the multifaceted dimensions of the pandemic in the UK.

## Pre-Vaccination Analysis

Employed __Multivariate Linear Regression__ to analyze relationships between COVID-19 outcomes and various predictors including testing rates, mobility patterns, weather metrics, and the stringency index.

📈 **Performance:** Achieved a Mean Squared Error of 0.102 on test data with an R-squared value of approximately 0.80 or higher for each response. The Root Mean Squared Error (RMSE) obtained is 0.3207. Thus, the model seems to perform well on the pre-vaccination data, as indicated by a high R<sup>2</sup> value and relatively low error metrics (MSE and RMSE).  The high R<sup>2</sup> value indicates that the model explains a significant amount of variance in the data.

🗝️ **Key Findings:**

-	Strong positive correlation between cumulative tests and confirmed cases, deceased cases, and hospitalized patients.
-	Higher stringency index values correlated with an increase in cases.
-	Mobility reductions, especially in retail and transit stations, showed a negative correlation   with case numbers.

#### Visualizations of the impact of multiple variables in the pre-vaccination Multivariate Linear Regression model

![Pre Vaccination Model Results](Images/Pre%20Vaccination%20Model%20Results.jpg)

For the pre-vaccination data, the forest plots offer a visual representation of various factors and their associations with Covid-19 cases, deaths, and hospitalizations.

## Vaccination Period Analysis

Extended the multivariate regression analysis to capture the dynamics post-vaccination.

📈 **Performance:** Demonstrated an improved Mean Squared Error of 0.0702 on test data with R-squared values consistently over 0.80.The Root Mean Squared Error (RMSE) obtained is 0.2692. The model's performance on the vaccination data is even better than its performance on the pre-vaccination data. This is evident from the improved (lower) error metrics (both MSE and RMSE) and the consistently high R<sup>2</sup> values. The improvements suggest that the model is more accurate in predicting outcomes during the vaccination period compared to the pre-vaccination period.

🗝️ **Key Findings:**
-	Significant negative correlation between the number of vaccinated individuals and infection cases, deceased cases, and hospitalizations.
-	Decline in transit station activity correlated with reduced cases and hospitalizations.
-	Testing rates remained pivotal in affecting case numbers, even post-vaccination.

#### Visualizations of the impact of multiple variables in the vaccination Multivariate Linear Regression model

![Pre Vaccination Model Results](Images/Pre%20Vaccination%20Model%20Results.jpg)

For the vaccination data, the above forest plots offer a visual representation of various factors and their associations with Covid-19 cases, deaths, and hospitalizations.

## Conclusion and Future Directions

🏁 **Implications**: In our extensive analysis of COVID-19 dynamics and vaccination impact, several pivotal insights surfaced:

i) **Testing** remains **paramount in understanding the pandemic's trajectory**, with a direct correlation seen across essential metrics.

ii) **Vaccination** emerged as a **crucial mitigator**, with data overwhelmingly supporting its effectiveness in curbing the virus's devastation.

iii) **Mobility**, particularly in public spaces, **significantly influences the spread**, suggesting the importance of monitoring and managing public movements.

iv) **Stringency measures** by governments, though effective to an extent, **yield optimal results when synergized with a robust vaccination drive**.

v) **Weather**, intriguingly, has its indirect yet noteworthy influence, with **warmer climates showing a promising correlation with diminished infections**.

In essence, the investigation underscores the importance of a multi-pronged approach to Covid-19 control, where testing, vaccination, controlled mobility, stringent government measures, and an understanding of weather interplays are vital in steering us towards a safer tomorrow.

🔮 **Future Scope**: Future studies could probe the impact of vaccination on emerging COVID-19 variants, the role of vaccine boosters, and the synergistic effects of public health measures combined with vaccination.

## Dependencies and Files

🔧 **Dependencies**: To bring the project to life, we rely on a set of essential R packages that streamline data handling, visualization, and analysis:
-	`ggplot2`: This powerful package empowers us to create intricate and visually appealing graphics, enabling us to visualize complex data relationships.
-	`cowplot`: Enhancing visual experiences, cowplot assists in arranging and annotating multiple ggplot objects, optimizing the presentation of our insights.
-	`tidyverse`: This comprehensive collection of R packages is tailor-made for data science tasks, providing tools for data manipulation, visualization, and more.
-	`caret`: An acronym for 'Classification And REgression Training,' caret simplifies data splitting, pre-processing, and model training, elevating our analysis

📁 **Files in the repository**: 
-	`UK Pre vaccination period.csv`: This file provides a comprehensive collection of COVID-19 statistics specifically before the initiation of vaccination campaigns. 
-	`UK Vaccination period.csv`: Unlock insights into the COVID-19 metrics that unfold post the commencement of vaccination drives with this dataset. 
-	`Data book.docx`: Curious about the variables driving the analysis? This document is your guide to the intricate details of each dataset variable. 
-	`Code and Interpretation.Rmd`: This R Markdown file encapsulates the heart of the project. Within its lines of code lies the key to analyzing, modeling, and interpreting the data. Explore the data pre-processing steps, multivariate linear regression models, and visualization techniques employed to derive meaningful insights from the datasets.
-	`Code and Interpretation.pdf`: If you're seeking a comprehensive summary of the project's journey, this PDF is your go-to resource. It condenses the entire analytical process into an accessible format. From data analysis and modeling to visualizations and conclusions, this document allows you to explore the project's insights without needing to dive into the code directly.
Each of these files serves a unique purpose in unravelling the intricate dynamics of COVID-19 in the UK and the impact of vaccination campaigns.

## Authors and References

👥 **Authors**: 

**Sreelekshmi Girijadevi Purushothaman/22200034** (mailto:sreelekshmi97@gmail.com)

**Vinothini Balasubramani/22202390** (mailto:vinothinibs09@gmail.com)


📚 **References**:

Key academic sources and datasets used in the analysis are referenced for further exploration.
1. Richard A. Johnson and Dean W. Wichern. [Multivariate Linear Regression Models in Applied Multivariate Statistical Analysis](https://ostad.hormozgan.ac.ir/ostad/UploadedFiles/863845/97050509-3761826667770356.pdf). (6th ed.) 360-418 Pearson Prentice Hall,2007.

2. R. Suganya, R.Arunadevi, & Seyed M.Buhari. [COVID-19 Forecasting using Multivariate Linear Regression](https://www.researchsquare.com/article/rs-71963/v1). Research Square.

3. Lewis, F.I., Ward, M.P. [Improving epidemiologic data analyses through multivariate regression modelling](https://doi.org/10.1186/1742-7622-10-4). Emerg Themes Epidemiol 10, 4 (2013). 

4. Keeling MJ, Dyson L, Guyver-Fletcher G, et al. [Fitting to the UK COVID-19 outbreak, short-term forecasts and estimating the reproductive number](https://journals.sagepub.com/doi/full/10.1177/09622802211070257). Statistical Methods in Medical Research. 2022;31(9):1716-1737. doi:10.1177/09622802211070257

5. Rencher, Alvin C. [Methods of Multivariate Analysis](https://www.ipen.br/biblioteca/slr/cel/0241). 2nd ed., John Wiley & Sons, Inc., 2002, pp. 337-339.

6. Dataset source: Google - [Covid19 Open Data](https://storage.googleapis.com/covid19-open-data/v3/location/GB.csv)

<div align="center">
  <hr style="border: none; height: 1px; background-color: #ccc; width: 50%; margin-top: 40px; margin-bottom: 40px;">
</div>
