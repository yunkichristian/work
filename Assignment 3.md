# Assignment 3

## Methodological Investigation
## Yunki Lee

### Introduction
Poverty is a problem faced globally whether it is in highly developed regions or non-developed regions.  Due to the circumstances of today’s world, many people face poverty due to the economy, social classes, or environment around them.  The most restricting characteristic of poverty is the income of individuals.  In fact studies show that nearly half of the world’s population lives on two dollars and fifty cents a day.  Another shows that a 1.3 billion people of the global population face extreme poverty which is less than a dollar and twenty five cents a day.  

Poverty is described as living conditions that are detrimental to health, economic development, and comfort.  There are different forms and levels of poverty.  Poverty is extremely harmful because it can lead to higher infant mortality, shorter life spans, lower literacy, environmental degradation, and the loss of biodiversity.  Poverty threatens human development and overall well-being globally.

Amartya Sen defines human development as the process of expanding the real freedoms that people enjoy.  Poverty is a threat to human development due to its restrictions on individuals.  It does not allow people to enjoy the real freedoms due to economic, social, and sometimes even environmental factors.  In order for regions to develop, threats such as poverty must be reduced or removed.  One step in the right direction is the prediction of poverty in regions. One area that specifically faces high poverty levels is Southeast Asia as it is still a developing region.  Through recent studies it has shown to be extremely difficult to predict poverty in a large region.
Studies show that poverty prediction can be done on smaller areas through the use of geospatial data.  I wish to investigate poverty prediction in the Philippines.

### Inquiry
The research question is an evaluative inquiry as it is examining the effectiveness of geospatial data methods in predicting poverty.  The research question I wish to answer is: Is poverty prediction an accurate way to combat poverty in the Philippines?  This research question dives deeper into the Philippines which is a country within Southeast Asia.  It evaluates the effectiveness of poverty prediction.  If the poverty prediction is effective, it can result in the reduction of poverty in the area.  

### Data Collection
The data used for the prediction of poverty in the Philippines came from five different data sources.  All the data sources are reliable and have been used by many different studies.  The data sources are the 2017 Philippine Demographic and Health Survey (DHS), the Visible Infrared Imaging Radiometer Suite Day/Night Band (VIIRSDNB) for the year 2016, The High Resolution Settlement Layer dataset, and OpenStreetMap.  

The data used in the study are in the table below.

![Dataset](https://user-images.githubusercontent.com/60199765/80864691-3f929780-8c52-11ea-8c32-4549b610bcc1.png)

Through the data the researchers focused on wealth index, education completed, access to electricity, and access to water.  These four datasets are captured by the DHS and are used to create data by the researchers.  

### Methods
The geospatial methods used were a combination of crowd-sourced geospatial data and satellite data. The specific methods used to evaluate the data were the Satellite-based Transfer Learning Model and the OpenStreetMap Model.  Both models were also evaluated using a five-fold nested cross validation scheme.  

The Satellite-based Transfer Learning Model involves the use of nighttime lights as an assumption of economic activity.  They classified the data with five night time intensity classes.  Their data had to be converted down to 224x224 pixel images from 400x400 pixel images, and so they did their best to adjust them.  Then, they used images to create clusters of up to 400 images that featured vectors.  Through the ridge regression model, they were able to use a ridge regression model to learn mapping from the clusters.  Through the Satellite-based Transfer Learning Model, the researchers were able to create a map showing the wealth index across the Philippines.  

The OpenStreetModel used clusters to extract roads, buildings, and points of interest.  Five types of roads were identified, these were primary, trunk, paved, unpaved, and intersection.  For the roads they calculated the distance to the closest road, the total number of roads, and the total road length per cluster.  Then, six different buildings were identified, these included residential, damaged, commercial, industrial, education, and health.  For every type of building the total number, total area, mean area, and the proportion of cluster area occupied were found.  For the POIs, 100 different points were found.  For each cluster they found the total number of POI’s in the area.  The socioeconomic well-being was predicted through the comparison of the performances of random forest regression models trained on the different types of OpenStreetModel features.  Specifically OpenStreetModel and nighttime light data were used in combinations to train random forest regression models.  

Both these methods are extremely accurate in predicting poverty. This is found through results of poverty prediction.  
The ground-truth wealth index can be seen next to the predicted wealth index below.  
![wealth index](https://user-images.githubusercontent.com/60199765/80864689-3d303d80-8c52-11ea-9354-2a0673e33a97.PNG)

The crowd-sourced geospatial data was used to create the poverty prediction models.  Below are the ground-truth wealth index and cross-validated Philippine poverty predictions using each model.
![cross validated](https://user-images.githubusercontent.com/60199765/80864693-428d8800-8c52-11ea-9b31-f473324780e7.PNG)

Through these geospatial data methods, poverty was able to be accurately predicted in the Philippines.

### Discussion and Conclusion

The results of the study on the prediction of poverty through geospatial data methods resulted in the confirmation of the applicability of the method.  The study also showed that the method can not be exactly copied for another country due to the geography of the Philippines.  The results have also shown that poverty prediction can be done through free and public crowd-sourced geospatial information.  These results have been validated through the comparison in other predictive models.  Other predictive models were analyzed and resulted in r-squared values from 0.51 to 0.75.  The r-squared value for the Philippine predictions were both .63. As a result the predictions are fairly accurate.  This is possible due to the DHS which measures the ground truth for the socioeconomic indicators, and the Philippine Statistical Authority which collects national social, economic, and health-related data.  I can conclude that the prediction of poverty in the Philippines is fairly accurate.  

An area of this research that needs further consideration would be the application to other countries in Southeast Asia.  Although it states that the methods would not work on other countries due to the geography of the Philippines.  I feel that further research could have been done to possibly create a model that can be somewhat used in other countries.  An improvement to the study could also be to do further testing to get a higher r-squared value to increase the accuracy of the poverty prediction.
### References
#### Source 1:  Balisacan, Arsenio M, et al. “Rural Poverty in Southeast Asia: Issues, Policies and Challenges.” Philippine Social Science Council Knowledge Archive, 2005, k-archive.pssc.org.ph/handle/0/1061.
#### Source 2:  Blumenstock, J. E. (2016, August 19). doi: https://doi.org/10.1126/science.aah5217
#### Source 3:  Booth, A. (2019, February 10). doi: https://doi.org/10.1111/apel.12250
#### Source 4:  Elvidge, C. D., Sutton, P. C., Ghosh, T., Tuttle, B. T., Baugh, K. E., Bhaduri, B., & Bright, E. (2009, May 5). doi: https://doi.org/10.1016/j.cageo.2009.01.009
#### Source 5:  Pokhriyal, N., & Jacques, D. C. (2017, October 31). doi: https://doi.org/10.1073/pnas.1700319114
#### Source 6:  Raitzer, David A, and Mywish K Maredia. “Analysis of Agricultural Research Investment Priorities for Sustainable Poverty Reduction in Southeast Asia.” Science Direct, 16 May 2012, doi.org/10.1016/j.foodpol.2012.04.001.
#### Source 7:  Sen, Amartya. Development As Freedom. Anchor Books, 2000.
#### Source 8:  Steel, J.E., Sundsøy, P.R., Pezzulo, C., Alegana, V. A., Bird, T. J., Blumenstock, J., … Bengtsson, L. (2017, February 1). doi: https://doi.org/10.1098/rsif.2016.0690
#### Source 9:  Sumner, Andy, et al. “Poverty And Inequalities In Middle-Income Southeast Asia.” 3 Apr. 2012.
#### Source 10: Tingzon, Isabelle, et al. “Mapping Poverty in the Philippines Using Machine Learning, Satellite Imagery, and Crowd-Sourced Geospatial Information.”
#### Source 11: Warr, Peter G. “Poverty Incidence and Economic Growth in Southeast Asia.” Science Direct, 2001, doi.org/10.1098/rsif.2016.0690.
