# Life Expectancy Report
 ## Introduction
    As the human era continues advancements in medicine keep improving the quality of life for countries around the world. In the pursuit to ensure these advancements are made available to everyone, the question then becomes what factors contribute most to the life expectancy in the modern era. The goal of this project was to see which features in our data had the strongest relationship with life expectancy. 
 ## The data
The data used was provided by the WHO and contains data on the following features:
   - Country -
   - Year (Between 2000 and 2015) 
   - Status (Developed or developing/1 or 0) 
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

 For data cleaning, all that was done was standardized the type format and imputed the missing data. The average was used for numerical data types and mode for categorical.

 ## Exploratory data analysis findings
   ### Trends over time

   On average, BMI has only gone up between 2000 and 2015.
  
   ![image](https://github.com/CameronBannick/Life-Expectancy-Dataset/blob/main/data_visuals/Average%20BMI.png)

   On average, there was a period where alcohol consumption was decreasing but starts increase towards the middle of the decade.
  
   ![image](https://github.com/CameronBannick/Life-Expectancy-Dataset/blob/main/data_visuals/Avergage%20alcohol%20consumption%20in%20liters.png)

   Cases of young deaths across multiple metrics are also steadily decreasing. For adult mortaltiy (between 15-60) there are two spikes for 2004 and 2008, these 
   years do coincidentally coincide with active moments of conflict during the Iraq and Afganistan wars. However, more analysis is needed to be sure.
   
   ![image](https://github.com/CameronBannick/Life-Expectancy-Dataset/blob/main/data_visuals/Average%20deaths%20under%205%20per%201000.png)
  
   ![image](https://github.com/CameronBannick/Life-Expectancy-Dataset/blob/main/data_visuals/Average%20infant%20deaths%20per%201000.png)
  
   ![image](https://github.com/CameronBannick/Life-Expectancy-Dataset/blob/main/data_visuals/Average%20young%20adult%20deaths%20by%20year.png)

   Regardless, life expectancy has been consistently increasing between 2000 and 2015

   ![image](https://github.com/CameronBannick/Life-Expectancy-Dataset/blob/main/data_visuals/Avergae%20life%20expectancy%20by%20year.png)


   ### Relationships for life expectancy 

   ![image](https://github.com/CameronBannick/Life-Expectancy-Dataset/blob/main/data_visuals/Life%20expectancy%20over%20BMI.png)
   
   BMI has a moderately strong relationship with life expectancy as seen above, the higher the BMI the higher the life expectancy. This appears to be a little counter intuitive because you'd expect a negative relationship with a lower BMI making a higher life expectancy. When calculating the correlation coefficient (which you can think of as "percent correlated") we get .56, so just a little over 50% correlated.
   
 ![image](https://github.com/CameronBannick/Life-Expectancy-Dataset/blob/main/data_visuals/Life%20expectancy%20over%20GDP.png).  

   Our next visual shows a weak realtionship between gdp and life expectancy, when calculating the correlation coeefficient (from now on called CC) you get 43%. So while there is a relationship, it doesn't appear to be a strong one. 
   
  ![image](https://github.com/CameronBannick/Life-Expectancy-Dataset/blob/main/data_visuals/Life%20expectancy%20over%20Hepatitis%20B%20Vaccine%20%25.png)  

   The hepatitis-b vaccine appears to have a weak relationship with life expectancy. All the data points far from the redline appear to be outliers, meaning they are not representative to the rest of the population. The CC came out to 20%.

   ![image](https://github.com/CameronBannick/Life-Expectancy-Dataset/blob/main/data_visuals/Life%20expectancy%20over%20Polio%20vaccine%20%25.png)

 However, the polio vaccine seems to have a "positive/moderate to strong relationship" meaning the more people are vaccinated the larger the life expectancy. The CC calculated was 46%
   
   
   ![image](https://github.com/CameronBannick/Life-Expectancy-Dataset/blob/main/data_visuals/Life%20expectancy%20over%20adult%20mortatilty.png)

   It appears adult mortality (15-60) has a strong negative relationship, meaning the more cases of adult mortality results in a lower life expectancy. The CC calculated was 70% in the negative direction.
   
![image](https://github.com/CameronBannick/Life-Expectancy-Dataset/blob/main/data_visuals/Life%20expectancy%20over%20deaths%20under%20age%205.png)

The relationship between under 5 deaths and life expectancy is very weak as you can say is above. CC calculated at 20% in the negative direction.
  
 ![image](https://github.com/CameronBannick/Life-Expectancy-Dataset/blob/main/data_visuals/Life%20expectancy%20over%20infant%20deaths.png)
  
  Similarly, infant deaths seem to have a very weak relationship with life expectancy at 20% in the negative direction.
   
   ![image](https://github.com/CameronBannick/Life-Expectancy-Dataset/blob/main/data_visuals/Life%20expectancy%20over%20population.png)

  Population doesn't appear to be a strong factor, seeing how the trend line goes flat across. The CC calcualtion was only 20%.

   ![image](https://github.com/CameronBannick/Life-Expectancy-Dataset/blob/main/data_visuals/Life%20expenditure%20over%20%25%20spent%20on%20health.png)

   FOr the chart above, we filtered all countries with a life expectancy under 65 and see if their was a relationship between that and percentage spent on healthcare. As shown, there doesn't appear to be a strong relationship with a CC of 1%.

  ![image](https://github.com/CameronBannick/Life-Expectancy-Dataset/blob/main/Life%20expectancy%20over%20alcohol%20consumption%20(in%20liters).png?)

  Alcohol has a weak relationship to life expectancy with only a 39% correlation

   ![image](https://github.com/CameronBannick/Life-Expectancy-Dataset/blob/main/data_visuals/Life%20expectancy%20over%20years%20in%20school.png)
   
   Schooling appears to have a very strong relationship to life expectancy. You can clearly see on the graph about more schooling means a higher life expectancy, the cc calculatede was 70%.

   We did run a statistical analysis on all these features where we split two samples from the life expectancy median and did find a statistical signifance in the samples on all these features. However, their were some limitatons that we will expand upon later.

  ## Modeling 

  After playing with a few different types of models, the Random Forest Regressor. This is a type of Descision Tree model that is good with numerical data. Think if you ask a bunch of friends for advice on a given descision and you took all of their advice to create a refined choice in your descision. This is how the random forest works. We split our data into a standard train test split and used the default parameters, this got us a model that can predit life expectancy withing about 1-3 years of error. When tuning the parameters, the error increased so we opted to leave it alone.

  ## Results and interpretations

  The two strongest factors given in regards to life expectany are schooling and adult mortality. However, I am not sure if schooling is directly assosciated with life expectancy. It could also be possible with more schooling avaliable means more public works meaning higher standards of santitation which could also be contributing. However, with adult mortaility, it does appear there are enough young deaths that are effecting the average life expectancy. 

  As far as moderate relationships, we have BMI, GDP, and the polio vaccine, however these three can also be connected. Notice earlier how higher BMI's were associated with higher life expectancy. Higher BMI could also mean higher access to food and doctors (polio vaccine).

  ## Limitations
  With no subject matter expert on hand, the sample groups for the statistical analysis were all split from the median. This was probably not the correct move since everything came back with a statistical significance.

  In addition, this dataset treats all countries the same and social differences such as diets should be taken into account. 

  ## Reccomendations
    It is clear that if we want to increase the average life expectancy we need to lower adult mortality. More research needs to be done on adult mortality on it's own to discover the leading causes to mitigate that issue.

   ## Conclusion
   While this project gives us some glimpses into what effects life expectancy, more research needs to be done on these features on their own to come up with a clear path to a healthier human race. 

   ## Next steps
   If possible, we need to look at these findings in a more cultural context. Separating or marking the countries by region and continent to better see how culture impacts these numbers would be ideal. In addition, a seperate study into adult mortality is needed seeing as that is something effecting worldwide averages significanlty. 



  
  
     
     
