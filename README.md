# Time Series Analysis
# Projections and Investor Insights | Zillow dataset

**Author: Miguel Santana | Flatiron Review: 11/4/2020, 1 PM**

The contents of this repository detail an analysis of real estate investment using Zillow's research dataset. The data can be found on [here](https://www.zillow.com/research/data/)

### Business problem:
A real-estate firm is looking to invest in residential property in the state of Colorado. Provide the top five Zip Codes for real estate investment. As a consultant, I will analyze the dataset and offer recommendations based on positive trending values, average return on investment and risk respective of a two year holding period. 

## Framework
![graph1](/images/OSEMN.png)
**The OSEMN Framework was used to analyze the data**

## Exploratory Data Analysis | Zip Codes

**General Data Distribution for homes in Colorado**

![graph1](/images/coloradodata.png)

**Error, Trend, Seasonality | Colorado Data**

![graph1](/images/ETS.png)

The 249 Zip Codes in Colorado were reduced to the top five through:

**Choices**
* Filter 1: Calculate a two year rolling return on investment values per Zip Code.
* Filter 2: Average the last 12 rolling ROI values per Zip Code.
* Filter 3: The 5 largest returned values were selected. 

**Zip Codes selected:**

![graph1](/images/12MRM.png)

• Pueblo, CO – 81003

• Clifton, CO – 81520

• Parachute, CO – 81635

• Colorado Springs, CO – 80916

• Colorado Springs, CO – 80921

**General Data Distribution | Top 5**

![graph2](/images/general.png)

## Modeling

**SARIMAX models were performed on each of the selected Zip Codes. A test/train split was performed where the test set was the exact same length as the expected future projection length. The train data was used to predict into the test data and a RMSE was used to validatate the model before including the full dataset. Each of the models were validate  by illustrating a RMSE to mean value ratio under 11%.**

## Recommended Zip Code Visualizations
**Colorado | Return On Investment Summary**

![graph3](/images/ROIsummary.png)

**Colorado | Return On Investment Summary**

![graph4](/images/ROIsummarynums.png)

## Results | Business Recommendations

Zip Codes 80916, 80921, 81520, 81003 and 81635 are the top five Zip Codes for real estate investment in Colorado. The safest investments (lowest risk) are Zip Code 81003 and 80916. The most profitable investment (highest risk) is Colorado Springs, CO 80921.

Zip Code 81003 and 80916:

(Lowest risk) - Both of the mentioned Zip Codes offer a positive value for minimum, projected and maximum return on investment. 

Zip Code 80921:

The minimum return on investment is -231,939. The projected return on investment is 85,606. The maximum return on investment is 403,151.

## Limitations
The final models were created using Zillow values from the last 10 years. While this increased the predictive ability of our models, making 2 year projections using 10 years of data will lead to a certain level of inconsistency. Additionally, awareness of additional factors that may influence these regions such as commercial development, federal poverty line data, etc is needed in order to solidify our business recommendations. 

## Future Work
Future work should be completed using Zillow's additional datasets. Zillow offers census, economic and additional data that can be used to help build better models that offer additional insight. 

### For further information
Please review the narrative of our analysis in our [our jupyter notebook](./jupyter_notebook.ipynb) or review our [presentation](./presentation.pdf)

For any additional questions, please reach out via email at santana2.miguel@gmail.com, on [LinkedIn](https://www.linkedin.com/in/miguel-angel-santana-ii-mba-51467276/) or on [Twitter.](https://twitter.com/msantana_ds)

##### Repository Structure:

```

├── README.md               <- The top-level README for reviewers of this project.
├── jupyter_notebook.ipynb     <- narrative documentation of analysis in jupyter notebook
├── presentation.pdf        <- pdf version of project presentation

```
