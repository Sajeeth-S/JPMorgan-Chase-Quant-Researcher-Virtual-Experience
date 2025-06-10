# JPMorgan Chase & Co. Quant Researcher Virtual Experience

This repository contains the code I wrote for achieving this certification. I will briefly go over what I did and the skills and tools I used for each task.

## Task 1

Here, I was given historical prices of natural gas and tasked with predicting future gas prices.

I noticed that from the historical price data, there was a strong indication of seasonal trends and upon looking at the peaks, medians and troughs, there was a clear linear pattern which drew me to applying **Linear Regression** to predict the gas prices for the future year.

I managed to make a function that returns a predicted price for the following year, but instead of restricting myself to only end of month dates, I extended it further for any date in the year. Moreover, I implemented a check to ensure the date provided is valid.

## Task 2

Here, I was tasked with pricing a commodity storage contract. I was required to price it based off the following parameters:
1. Injection dates
2. Withdrawal dates
3. The prices at which the commodity can be purchased/sold on those dates
4. The volumes being injected
5. The volumes being withdrawn
6. The maximum volume that can be stored
7. Injection/Withdrawal costs
8. Storage costs
9. Transport costs

I managed to make a function that could provide a value to a contract whilst taking all of above into account. 

## Task 3

Here, I was tasked to perform credit risk analysis. I was given historical data of previous customers, their features and whether they defaulted on their loan or not, in order to predict if future customers would default on their loan or not.

Since defaulting is binary (either one defaults or does not), I used **Logistic Regression** to model this. Having trained my model on a part of the dataset, and tested it on the rest, I achieved a Test Accuracy Score of 0.9984 and a ROC AUC of 0.99997. 

Since, we are able to predict whether a loanee will default or not, we can also then predict the expected losses of taking on a new loanee. So I also implemented a function, that given features of a loanee, will return the expected loss of taking on that customer.
