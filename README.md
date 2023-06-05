# Alphabet Soup Charity Analysis

## Overview
This analysis aimed to build a neural network capable of predicting whether applicant organizations will be succeessful if given funding by Alphabet Soup. Input data included industry affiliation, use case, organization type, government classification, income amount, and other considerations. 

## Results
### Data Preprocessing
- The target variable in this analysis was the IS_SUCCESSFUL column in the dataset, describing whether or not the charitable organization was successful after receiving funding.
- All other columns were considered features, with the exception of the identifier columns EIN and NAME, which were dropped in preprocessing.

### Compiling, Training, and Evaluating.
- I used the relu activation function for the input layer, and the selu activation function for the hidden layers. There were 3 hidden layers, starting with 16 neurons for layer 1, 8 neurons for layer 2, and 5 neurons for layer 3.
- I was not able to achieve the target model performance, the best I could get was 57%.
- I dropped the STATUS and SPECIAL_CONSIDERATIONS columns since they were both extremely lopsided. I binned all the remaining columns of USE_CASE, AFFILIATION, ORGANIZATION. The only column I did not bin was income amount since this had a more reasonable distribution of uniques.
- I increased the number of layers to 3 and added neurons to each. I tried different combinations of relu, selu, and sigmoid activation functions in each layer. Despite all of these measures I was unable to beat 57%.

## Summary
In summary, this model does a fairly poor job at predicting the success rate of charitable organizations. For future work in this analysis, I would suggest improving the original dataset. Try to find additional metrics such as number of employees, lifetime of the organization, or location of the organization. These factors may be more important in determining success than the ones included in this dataset.
