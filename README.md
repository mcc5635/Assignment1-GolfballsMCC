# Assignment1-GolfBalls
Your first examinable assignment

This assignment asks you the following:

Allan Rossman used to live along a golf course and collected the golf balls that landed in his yard. Most of these golf balls had a number on them. Allan tallied the numbers on the first 500 golf balls that landed in his yard one summer.

Specifically. he collected the following data:
137  golf balls numbered 1
138  golf balls numbered 2
107  golf balls numbered 3
104  golf balls numbered 4
14 "others" (Either with a different number, or no number at all. We will ignore these other balls for the purposes of this question.)

Question: What is the distribution of these numbers?
In particular, are the numbers 1, 2, 3, and 4 equally likely?


The intuition is that you are going to conduct a simulation-based hypothesis test. (If you happen to know the correct theoretical test, I want you to assess the significance of the associated test statistic using simulation rather than theoretical results.)

Here's the pseudocode. Your job is to flesh it out, run it for at least 3 test statistics (that you have to come up with), and report on the results. Results should be turned in as a nicely formatted R-markdown doc that compiles to an html file. 

```{r pseudocode}
# Pseudocode for the golf ball problem in assignment 1

# Do the following repeatedly, for each test statistic that you use.

# 1 Pick a test statistic. An example might be to use the range between the highest and lowest number in the four cells of the table.

# 2. We then find the behavior of the test statistic under the null hypothesis that all numbers are equally likely by repeatedly doing the following (say 10000 times):
# 2a. Generate a simulated dataset of the same size as the one we observed. So, in this example it will contain 486 simulated golf-balls, # with the number of each being sampled from a discrete uniform distribution DU[1,4].
# 2b. Calculate the value of the test statistic for that simulated dataset (so here, we construct a table of frequencies, just like for the observed data, and then take the difference between the larget and smallest numbers in that table). Store this value.

# 3. After repeating 2a and 2b 10000 times, and storing the 10000 values of the test statistic that results, plot those values, using a histogram, say. This is the "null distribution" of the test statistic under the null hypothesis that all numbers arew equally likely.

# 4. Plot the value of the test statistic for the observed dataset (which is 34 if we use the range as an example).

# 5. If the observed test statistic value falls in the tails of the null distribution plotted in step 3, (quantify this using the percentile of that value in the null distribution - known as the p-value) we reject the null hypothesis that the numbers on the balls are uniformly distributed.

```
