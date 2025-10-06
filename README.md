# Required Assignment 11.1: What drives the car price? 
## Data used in this research is from the Kaggle Repository 
  Please use the following link to view my findings and supporting plots created using above mentioned data : <url>https://github.com/sganesan64/Module11_CarPrice</url>

## Assignment Objectives
  Identifying the most probable reason that drives the car price using CRISP-DM process.
  
## Assessment of Data
  Provided data from car delaership contains used Car price from different Regions for
  various manufacturers, car details like models with year, Cylinders,odometer and condition.
  
  At First look many of the data seems to be null, so , we may not be able to use all the features effectively.
  ### Risks and benefits
  As this limited data will be used for analysis , it pose a risk of providing wrong assesssment to the car dealers.
  As the benefit, we will be able to use modeling techinques and try to come up with other possible results to analyze further.

## Initial Assessment and plan for this Assignment
  Using the provided data, 
    1. Verify and clean Data
    2. Cleanup all null values
    3. Identify features to use with modeling and their correlation to the price variation
    4. a. create models 
       b. train 
       c. predict
       d. repeat a-c with different features 
       e. Finalize the Model 
       f. Prepare final report
       g. present the decision with Features identified as the cause for the Price changes

## Verified data whenever <u>there is a change in price</u> using Seaborns Joint plot correlation to different factors that affect the price.
### PLOT 1 : 
sns.jointplot(dfcarprice_filtrd_srtd,x='region_n',y='price',kind='hist',hue='region',height=12)
### PLOT 2 : 
sns.relplot(
    data=dfcarprice_filtrd_srtd,
    x='region_n',
    y='price',
    col='manufacturer',  # Separate plots for each manufacturer
    hue='model',         # Different colors for each model within a manufacturer
    style='year',        # Different markers for each year
    kind='scatter',      # Use scatter plot for individual points
    col_wrap=1,          # Wrap columns after 2 plots for better layout
    height=5,            # Height of each facet
    aspect=1.5           # Aspect ratio of each facet
)

plt.suptitle('Price by Region, Manufacturer, Model, and Year', y=1.02)
plt.tight_layout(rect=[0, 0, 1, 0.98]) # Adjusted layout to prevent title overlap
plt.show()
 
<table><tr><td>
    <u>Fig 1:Hist PLOT FOR PRICE BY REGION</u></td><td></u>Fig 2:RelPlot of Price for Model Manufacturer ,Model and Year</u>  </td></tr>
<tr><td><img width="300" height="300"  alt="Seaborn jointplot againt temperature vs accepted" src="https://github.com/sganesan64/Module11_CarPrice/blob/main/images/His%20plot%20-price%20per%20Region.JPG" /></td> <td> <img width="300" height="300" alt="image" src="https://github.com/sganesan64/Module11_CarPrice/blob/main/images/RelPlot%20-Price%20per%20Manufacturer%20for%20Model%20and%20year.JPG" />
    </td></tr></table>

## Findings 1: 
From the above plot (Fig 1) It is obvious Price varies in many regions and certain some with lower only and some with higer prices only.

## Findings 2:
From the PLOT2 it is obvious some Manufacturer's car are sold  broadly across many regions. some Manufacterer's car are sold in only certain regions.
Also impact on price is also visible by region

### Data conditions and concerns
Based on the Data condition , certain Manufacturer and Model may be removed due to lower representation in the data.

Cleaned data to have numbers for Text columns by mapping numbers to categories and cleaning up age by replacing text parts.

## Findings 3: After trying several plots and combinations , 

<img width="785" height="790" alt="image" src="TYPE PLOT PATH FROM GITHUB" />


## Next Steps
    Collecting more Data for creating better sample and examiner to come up with definitive answer or direction.



