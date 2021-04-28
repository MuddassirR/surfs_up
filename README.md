# surfs_up
## Overview of Analysis
The broad goal of the data analysis was to determine if an entrepreneur should operate a surfing & ice cream shop in Huwaii based on weather analysis. The entrepreneuer hired an investor who asked us to check temperature trends before opening up a shop. Speicifically, he/she asked us to check and analyze temperature data for the months of June and December to determine if the shop is sustainable year-round.

Tasks:
- deliverable 1: determine summary statistics for June
- Deliverable 2: determine summary statistics for December
- Deliverable 3: write a report for the statistical analysis

* Date file used: [hawaii.sqlite](https://github.com/MuddassirR/surfs_up/blob/main/hawaii.sqlite)
* software used: matplotlib, python, pandas, numpy, VS code, Jupyter Notebook, Sqlalchemy

## Results
Summary statistics for June:
- count of 1700
- average temperature in June is 74.94 (farenheit), give or take 3.26 standard deviations
- minimum temperature is 64 degrees
- maximum temperature is 85 degrees

Summary Statistics for December:
- count of 1517 
- average temperature in December is 71.04 (farenheit), give or take 3.75 standard deviations
- minimum temperature is 56 degrees
- maximum temperature is 83 degrees

## Summary
We see December is colder on average than in June by almost 4 degrees farenheight. We also see that the difference between the standard deviations is around 0.5 degrees with Decemeber being higher, implying that December has temperature data more spread whereas June's standard deviation is more clustered around the mean. We also see that botht the minimum and maximum temperatures are lower in December than they are in December, further indicating that December is a colder month. We can also look at percipitation levels.. Our code for calculating temperatures by month was: session.query(Measurement.date, Measurement.tobs).filter(extract('month',Measurement.date)==12).all(). Where 12 represents Decemeber, we'd change this number to 6 to represent June. Tobs represent temperature and to measure precipitation, we could change tobs to prcp after creating a new query session. It his hypothesized that since December is colder, sales would most likely decrease for a surfing & ice cream shop in cold months and increase in hot months. The entrepreneur may wish to open a surfing & ice cream shop for the spring/summer and provide different products and/or services in the Winter. 
