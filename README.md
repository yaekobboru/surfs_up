# Project overview

This analysis calculates and summarize temperature data for the months of June and December in Oahu.
The result will determine if the surf and ice cream shop business is sustainable year round.

# Results

* The mean temperature for June is 75 and for December is 71.
* The minimum temperature for June is 64 and for December is 56.
* The maximum temperature for June is 85 and for December is 83.

# Summary

The minimum temperature record is 56 in December and the maximum is 85 in June with
71 as the lowest average recorded in December between year 2010 and 2017.
The below query supports decision by providing latest year average temperature 
and precipitation. 

Temp=session.query(Measurement.tobs).filter(extract('year', Measurement.date)==2017).all()
prcp=session.query(Measurement.prcp).filter(extract('month',Measurement.date)==6).all()
prcp2=session.query(Measurement.prcp).filter(extract('month',Measurement.date)==12).all()
* list(Temp)------------convert to list
* df = pd.DataFrame(Temp)-------convert to data frame
* Summary_Dec = df.describe()-------

