---
Course: CSCC 45
Year Level: 3rd
Semester: 2nd
---
---
EDA

Python programming language

instead reading value data you can actually linear plot

**Linear Plot** 
- takes a linear line or curve

**Box Plots** 
- charts which are rendered in a box passion
- sometimes vertical or horizontal
- if perfectly even, then it is a data set that is *normally distributed*
	- example of normally distributed, is white noise, an *IID*
	- the selection of every element in that set has uniform probability, no pattern in the data set
- left hand side, 1st quartile
- line in the right hand side, is q3
- the division, in the median
- if the box (interquartile ranged) is leaning towards the left or right, then the data set is *not white noise*
	- if in the left, minimum, it is rightly skewed
	- if in the right, maximum, it is leftly skewed

**Histogram**
- similar to a column chart and frequency table under statistics
- data set is categorized in different ranges
- the number of data values on a range, the value on the y-axis would vary from one range to another
	- if leaning towards the left, it is rightly skewed, then not an IID
- the idea is, histogram indicates that a data set is not normally distributed, forecast and prediction the information is weathering?

**Rolling Mean and Rolling Standard Deviation**
- rolling mean - a chart that is calculated by getting the mean of the data set given a particular value of a window
- if rolling mean is increasing then decreasing, rest assured there is a *linear trend*
	- linear trend: upward trend, downward trend, no trend.
	- no trend, cant use forecast or prediction
- rolling standard deviation - calculated ...
- if deviation and mean is increasing and decreasing, then no trend

**ADF**
- is a function in python, augmented dickey-fuller test
- a test statistic, a stationarity on a data set
- two hypothesis: null, and alternative.
	- null - time series has a unit root, non stationary. Series follows a random walk, values in a data set are values randomly generated series
	- alternative - time series does not have unit root, stationary. Reverts to a mean value overtime.
- should have unit root, not stationary. there is information in data set to make forecast since non-stationary.

**Auto-correlation Function**
- there is also partial-correlation function
- tests whether there is a linear autocorrelation, every value in the x axis corresponds to a lag in a data set.
- significant region - 
	- if a spike is in, then there is no autocorrelation
	- if spike surpasses significant region, then there is autocorrelation
		- the values are then has correlation within one another
- if partial autocorrelation
	- if there is a spike, the first value and third value in the time series, then middle value?
	- what of these spikes does tell the true truth
	- finds which lag has a correlation
	- does not include the middle value, like if 1st and 3rd, then no 2nd
	- the x-axis is the lag, white ticks are the magnitude of the correlation
- if there is *correlation* - then there is linearity
- if *absent* - does not necessary mean we can't forecast, still could have pattern
- autocorrelation function, only good for linearity
- if upwards then downwards, then vice versa, no linearity is possible
- if negative correlation - an increase on a lag, decreases a lag
- why autocorrelation - applied upon two varaiables, if applied to one value then autocorrelation
IF MAG PMACK DAPAT MAG RECORD - WHAR IS THIS JARGON

