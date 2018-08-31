1. For each of parts (a) through (d), indicate whether we would generally expect the performance of a flexible statistical learning method to be better or worse than an inflexible method. Justify your answer.

    a) The sample size n is extremely large, and the number of predictors p is small.

        Given the large sample size, a more flexible model is likely the most appropriate route.
        The variance will remain low, so going for a flexible method with lower bias will perform better.

    b) The number of predictors p is extremely large, and the number of observations n is small.

        With many predictors and a small sample size, sample variance will be very high. To counter this,
        we want to use an inflexible model with high bias and low variance, like linear regression.

    c) The relationship between the predictors and response is highly non-linear.

        Without information about the number of predictors or the sample size, it is hard to say,
        but--given ideal conditions--you will want a model that represents the underlying distribution better.
        Go with a more flexible model.

    d) The variance of the error terms, i.e. σ^2 = Var(ε), is extremely high.

        This is our irreducible error--how our sample fits the underlying, true distribution from which it
        has been drawn.

        The best course of action here is to approach with an inflexible model first, as we do not want to
        overfit to an innacurate distribution with a more flexible model

2. Explain whether each scenario is a classification or regression problem, and indicate whether we are most interested in inference or prediction. Finally, provide n and p.

    a) We collect a set of data on the top 500 firms in the US. For each firm we record profit, number of employees, industry and the CEO salary. We are interested in understanding which factors affect CEO salary.

        This is a regression problem. Our dependent variable, CEO salary, is quantitative and continuous. We are attempting to perform inference to determine which factors affect CEO salary.

        n = 500; the number of firms
        p = 3; profit, number of employees, industry

    b) We are considering launching a new product and wish to know whether it will be a success or failure. We collect data on 20 similar products that were previously launched. For each product we have recorded whether it was a success or failure, price charged for the product, marketing budget, competition price, and ten other variables.

        This is a classification problem with the dependent variable, success or failure, being comprised of the two classes,
        success and failure. This is a prediction task, not one in which we perform inference.

        n = 20; the number of products in the study
        p = 13; price charged, marketing budget, competition price, and ten other variables

    c) We are interested in predicting the % change in the US dollar in relation to the weekly changes in the world stock markets. Hence we collect weekly data for all of 2012. For each week we record the % change in the dollar, the % change in the US market, the % change in the British market, and the % change in the German market.

        This is a regression problem. Our dependent variable, % change in the US dollar, is quantitative and continuous. We are attempting to predict the % change present (its in the description...).

        n = 52; weeks in the year
        p = 3; % change in US, British, and German markets, respectively

3. We now revisit the bais variance decomposition

    a) Provide a sketch of typical (squared) bias, variance, training error, test error, and Bayes (irreducible) error curves, on a single plot, as we go from less flexible statistical learning methods towards more flexible approaches. The x-axis should represent the amount of flexibility in the method, and the y-axis shoudl represent the values for each curve. There should be five curves. Make sure to label each one.

    b) Explain why each of the five curves has the shape displayed in part (a)

4. You will now think of some real-life applications for statistical learning.

    a) Describe three real-life applications in which classification might be useful. Describe the response, as well as the predictors. Is the goal of each application inference or prediction? Explain your answer.

    b) Describe three real-life applications in which regression might be useful. Describe the response, as well as the predictors. Is the goal of each application inference or prediction? Explain your answer.

    c) Describe three real-life applications in which cluster analysis might be useful.
