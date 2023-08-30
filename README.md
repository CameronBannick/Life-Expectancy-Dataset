# Life Expectancy Dataset
 ## Context 
"Although there have been lot of studies undertaken in the past on factors affecting life expectancy considering demographic variables, income composition and mortality rates. It was found that affect of immunization and human development index was not taken into account in the past. Also, some of the past research was done considering multiple linear regression based on data set of one year for all the countries. Hence, this gives motivation to resolve both the factors stated previously by formulating a regression model based on mixed effects model and multiple linear regression while considering data from a period of 2000 to 2015 for all the countries. Important immunization like Hepatitis B, Polio and Diphtheria will also be considered. In a nutshell, this study will focus on immunization factors, mortality factors, economic factors, social factors and other health related factors as well. Since the observations this dataset are based on different countries, it will be easier for a country to determine the predicting factor which is contributing to lower value of life expectancy. This will help in suggesting a country which area should be given importance in order to efficiently improve the life expectancy of its population." -WHO
 ## Questions
- Does various predicting factors which has been chosen initially really affect the Life expectancy? What are the predicting variables actually affecting the life expectancy? -
- Should a country having a lower life expectancy value(<65) increase its healthcare expenditure in order to improve its average lifespan? -
- How does Infant and Adult mortality rates affect life expectancy? -
- Does Life Expectancy has positive or negative correlation with eating habits, lifestyle, exercise, smoking, drinking alcohol etc.-
- What is the impact of schooling on the lifespan of humans?
- Does Life Expectancy have positive or negative relationship with drinking alcohol?
- Do densely populated countries tend to have lower life expectancy?
- What is the impact of Immunization coverage on life Expectancy?
## The data
The data used was provided by the WHO and contains data on the following features:
   - Country -
   - Year (Between 2000 and 2015) 
   - Status (Developed or developing) 
   - Life Expectancy 
   - Adult Mortality (deaths between 15 and 60) 
   - Infant Deaths (per 1000 population) 
   - Alchohol (consumption per capita in liters) 
   - Percentage Expenditure (on healthcare) 
   - Hepatitis B (immunization) 
   - Measles (cases per 1000) 
   - BMI 
   - Under-Five Deaths (per 1000) 
   - Polio (immunization) 
   - Total Expenditure (on healthcare) 
   - Diphteria (immunization) 
   - HIV/AIDs (deaths per 1000) 
   - GDP 
   - Population 
   - Thinness 1-19 years 
   - Thinness 5-9 years 
   - Income Compostion Of Resources (percentage between 0 and 1) 
   - Schooling (years)
 ## Exploratory data analysis findings
   ### These findings are referenced from the Jupyter Notebook written in Python
   #### Trends over time

   On average, bmi has only gone up between 2000 and 2015.
  
   ![image](https://github.com/CameronBannick/Life-Expectancy-Dataset/blob/main/data_visuals/Average%20BMI.png)

   On average, there was a period of time where alcohol consumption was decreasing, but starts increase towards the middle of the decade.
  
   ![image](https://github.com/CameronBannick/Life-Expectancy-Dataset/blob/main/data_visuals/Avergage%20alcohol%20consumption%20in%20liters.png)

   Cases of young deaths across multiple metrics are also steadily decreasing. For adult mortaltiy (between 15-60) there are two spikes for 2004 and 2008, these 
   years do coincidentally coincide with active moments of conflict during the Iraq and Afganistan wars. However, more analysis is needed to be sure.
   
   ![image](https://github.com/CameronBannick/Life-Expectancy-Dataset/blob/main/data_visuals/Average%20deaths%20under%205%20per%201000.png)
  
   ![image](https://github.com/CameronBannick/Life-Expectancy-Dataset/blob/main/data_visuals/Average%20infant%20deaths%20per%201000.png)
  
   ![image](https://github.com/CameronBannick/Life-Expectancy-Dataset/blob/main/data_visuals/Average%20young%20adult%20deaths%20by%20year.png)

   Regardless, life expectancy has been consistently increasing between 2000 and 2015

   ![image](https://github.com/CameronBannick/Life-Expectancy-Dataset/blob/main/data_visuals/Avergae%20life%20expectancy%20by%20year.png)


   #### Relationships between data

   The visual below shows there is a "positive/moderate" realtionship between life expectancy and bmi; meaning as bmi increases, life expectancy will as well.
   
   ![image](https://github.com/CameronBannick/Life-Expectancy-Dataset/blob/main/data_visuals/Life%20expectancy%20over%20BMI.png)

    Our next visual shows a weak realtionship between gdp and life expectancy, implying access to more resources doesn't indicate a longer life.
   
   !{image](https://github.com/CameronBannick/Life-Expectancy-Dataset/blob/main/data_visuals/Life%20expectancy%20over%20GDP.png)

   The hepatitis-b vaccine also appears to have a weak relationship with life expectancy. All of the data points far from the redline appear to "outliers", 
   meaning they are not representative to the rest of the population. 

   ![image](https://github.com/CameronBannick/Life-Expectancy-Dataset/blob/main/data_visuals/Life%20expectancy%20over%20Hepatitis%20B%20Vaccine%20%25.png) 

   However, the polio vaccine seems to have a "positive/moderate to strong relationship" meaning the more people are vaccinated the larger the life expectancy.
   
   ![image](https://github.com/CameronBannick/Life-Expectancy-Dataset/blob/main/data_visuals/Life%20expectancy%20over%20Polio%20vaccine%20%25.png)

   It also appears adult mortality (15-60) has a moderate negative relationship, meaning the more cases of adult mortality results in a lower life expectancy.
   
   ![image](https://github.com/CameronBannick/Life-Expectancy-Dataset/blob/main/data_visuals/Life%20expectancy%20over%20adult%20mortatilty.png)

   But, it does not appear deaths under five or infant mortality have a realtionship to life expectancy 
  
   ![image](https://github.com/CameronBannick/Life-Expectancy-Dataset/blob/main/data_visuals/Life%20expectancy%20over%20deaths%20under%20age%205.png)
  
   ![image](https://github.com/CameronBannick/Life-Expectancy-Dataset/blob/main/data_visuals/Life%20expectancy%20over%20infant%20deaths.png)
   
   How does population density play in? Well belowe we can see that there isn't a relationship between population desity and life expectancy.

   ![image](https://github.com/CameronBannick/Life-Expectancy-Dataset/blob/main/data_visuals/Life%20expectancy%20over%20population.png)

   Does the percentage spent on Healthcare play a role? According to the plot below there doesnt appear to be much of a relationship.

   ![image](https://github.com/CameronBannick/Life-Expectancy-Dataset/blob/main/data_visuals/Life%20expenditure%20over%20%25%20spent%20on%20health.png)
   
   The strongest relationship found was a little surprising, the strongest postive relationship is between years of schooling and life expectancy. Meaning the 
   more years of schooling one has the higher the life expectancy.

   ![image](https://github.com/CameronBannick/Life-Expectancy-Dataset/blob/main/data_visuals/Life%20expectancy%20over%20years%20in%20school.png)

  So in conclusion, upon completion of the exploratory data anlysis, it would appear that the strongest indicators of life expectancy are bmi, polio
  vaccinations, adult mortality, and years of schooling. 

### These findings are referenced from the Excel file 
  #### Analysis of potential relationships
  After seeing what parts of the data looked like they were related, a number was found to quantify the relationship. This confirmed the relationship between 
  adult mortality and life expectancy as well as between bmi and life expectancy. However, a negative relationship a moderate negative relationship was found 
  between HIV/AIDS cases and life expectancy; meaning that more HIV/AIDS cases seems to indicate a lower life expectancy. 

  The polio vaccine and diphteria vaccine both appear to have a moderate positive reltionship. This means higher rates of vaccinations seem to indicate higher l 
  life expectancy.

  GDP and percentage expenditure are on the cusp of being in the "moderate relationship zone", but less so than the former mentioned.

  The strongest relationship found in the dataset is still years of schooling, indicating education is potentially the strongest indicator of a long life 
  expectacncy. You could make the argument that it is more schooling typically comes with more resources such as medical and capitol. However, the relationships 
  with those data features were a lot smaller.

  
  
     
     
