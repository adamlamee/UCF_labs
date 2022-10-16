# Answers to the self-check quesitons in [Lab 3: model fitting practice](./README.md)  
### Part 1  
How many position measurements are there?  
**317 rows according to data.shape**  

What was the duration of this data collection?   
**Around 60 seconds, according to the scatterplot.**   

What might be a good type of function to fit to this data?  
**It looks pretty linear, so y=mx+b?**  

Can you figure out what the 's' parameter sets in the plt.scatter function?  
**s sets the point size; try changing its value and running that block of code again.**  

### Part 2  
What's the name of the function you defined to calculate the model y-values?  
**model_1; see the line starting with "def model_1".**  

What is the line equation for your trendline, including the optimized coefficients?  
**y = -0.4922 x - 0.17867297, according to popt.**  

How well does a line fit this data? What are the signs that this data isn't quite linear? Can you think of any functions that might be a better fit?  
**Data points in the middle tend to be below the line and the points to the left and right or mostly above it; a curve would fit better.**  

### Part 3  
Could a residual be zero? Could it be negative?  
**A point exactly on the trendline would have a residual of zero; it could be negative if the point were below the line. See the line of code that calculated the residuals.**   

If all the data points fell exactly on the trendline, what would the model's RSS be? Could a model's RSS be negative?  
**An ideal RSS equal to zero would occur if all points were exactly on the line (summing all residuals equal to zero). Since the RSS sums up *squared* residuals, the RSS is never negative**   

What is this model's RSS?  
**About 1.18.**  

While the RSS for a single model doesn't tell us much, how could comparing the RSS values for two models help determine which one fits the data better?  
**For two models, the one with a *smaller* RSS has its trendline close to the data points and therefor is a better fit.**  

If the position data were linear, the residuals would be evenly distributed across the residual plot. However, the residuals in the middle of the plot are mostly while the residuals at the left and right are positive. What does that communicate about this model function?  
**The residual plot shows how this model doesn't fit as well as a curve that bows down in the middle (i.e., concave up). See the [residual analysis](https://www.itl.nist.gov/div898/handbook/pmd/section6/pmd614.htm) section of the NIST Engineering Statistics Handbook if you want more.**  

What shape of model function might fit this data better?  
**Logarithms, exponential decay, and parabolas can all be concave up.**  

Whenever possible, you should choose a model function that has some basis in theoritical predicitons related to the data. Can you think of any functions that might be reasonable to describe the position of an object speeding up?  
**The three kinematic equations that describe accelerating motion. The one that looks like x = x<sub>0</sub> + v<sub>0</sub>t + 1/2at<sup>2</sup> would be a good choice.**  

### Part 4  
How well does your new model appear to fit the motion data in the scatterplot?  
**Does the curve look close to the data points? "Not well" is a totally acceptable answer here. Sometime you try a model that isn't as good of a fit.**  

Does the residual plot show any pattern like it did for the trendline?  
**Sometimes varying the point size can help see a pattern, if one exists. The main patterns to look for are residuals that look gradually decreasing, increasing, or bowed up or down.**  

What is your new model function equation, including the optimized coefficients?  
**See the answer in Part 2 for how to write that.**  

Based on the RSS, did your new model fit the data better than the trendline?  
**If it has a smaller RSS than 1.69, it's a better fit than the trendline. Otherwise it's not as good of a fit (which is totally okay).**  

If another group were going to try fitting a different function, how would you advise them?  
**Try a quadratic function if they haven't already.**  
