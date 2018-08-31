# Chapter 2 - Statistical Learning - Conceptual Problems
- - - -

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

- - - -

2. Explain whether each scenario is a classification or regression problem, and indicate whether we are most interested in inference or prediction. Finally, provide n and p.

    a) We collect a set of data on the top 500 firms in the US. For each firm we record profit, number of employees, industry and the CEO salary. We are interested in understanding which factors affect CEO salary.

        This is a regression problem. Our dependent variable, CEO salary, is quantitative and continuous.
        We are attempting to perform inference to determine which factors affect CEO salary.

        n = 500; the number of firms
        p = 3; profit, number of employees, industry

    b) We are considering launching a new product and wish to know whether it will be a success or failure. We collect data on 20 similar products that were previously launched. For each product we have recorded whether it was a success or failure, price charged for the product, marketing budget, competition price, and ten other variables.

        This is a classification problem with the dependent variable, success or failure,
        being comprised of the two classes, success and failure.
        This is a prediction task, not one in which we perform inference.

        n = 20; the number of products in the study
        p = 13; price charged, marketing budget, competition price, and ten other variables

    c) We are interested in predicting the % change in the US dollar in relation to the weekly changes in the world stock markets. Hence we collect weekly data for all of 2012. For each week we record the % change in the dollar, the % change in the US market, the % change in the British market, and the % change in the German market.

        This is a regression problem. Our dependent variable, % change in the US dollar,
        is quantitative and continuous. We are attempting to predict the % change present.
        (its in the description...)

        n = 52; weeks in the year
        p = 3; % change in US, British, and German markets, respectively

- - - -

3. We now revisit the bias-variance decomposition

    a) Provide a sketch of typical (squared) bias, variance, training error, test error, and Bayes (irreducible) error curves, on a single plot, as we go from less flexible statistical learning methods towards more flexible approaches. The x-axis should represent the amount of flexibility in the method, and the y-axis should represent the values for each curve. There should be five curves. Make sure to label each one.

        This one is just copying curves already in the book. I'll describe the nature below...

    b) Explain why each of the five curves has the shape displayed in part (a)

        i. Bias:
            This starts relatively high with the most inflexible models, and decreases with more flexible models.

            As this is the error introduced by approximating a real-life problem, assuming simplicity will
            have its cost on analysis and prediction. Real relationships are seldom linear.

        ii. Variance:
            This starts releatively low with the most inflexible models, and increases as flexibility increases.

            Variance refers to the amount that our approximated model would change if we change the data it is
            trained on.

            Less flexible models are less likely to conform to different data, while more flexible
            models are likely to take the shape of the data presented. This is especially true with smaller
            sample sets.

        iii. Training Error:
            This starts at a middling amount, but trends monotonically downward as flexibility increases.

            As we introduce more complexity into our model, we will conform more and more to the training set.
            While this may seem good, the impact on Test Error is less desirable...

        iv: Test Error:
            This starts in roughly the same place as Training Error, decreases, then increases significantly
            as the model grows more complex.

            As the model conforms more and more to the training data it has seen, it will generalized worse
            and worse to data it has not seen--negatively impacting the Test Error.

        v: Irreducible Error:
            This is an unchanging straight line. The nature of this error does not lie within the model,
            but in the data as it has been collected.

- - - -

4. You will now think of some real-life applications for statistical learning.

    a) Describe three real-life applications in which classification might be useful. Describe the response, as well as the predictors. Is the goal of each application inference or prediction? Explain your answer.

        - Classifying Spam email:
            - Response:
                Spam or Not Spam
            - Predictors:
                Number of specific keywords present in specific emails
            - Goal:
                Prediction -- we want to predict whether to allow mail into the inbox or to send it to spam

        - Classifying Infectious Diseases based on symptoms present in patient:
            - Response:
                Which diseases are likely present
            - Predictors:
                Symptoms of patient. Qualitative and Quantitative.
            - Goal:
                Both prediction and inference.
                As a prediction task, this can provide a second or third opinion to medical professionals.
                As an inference task, this can teach us a lot about the relationships between symptoms and diseases.

        - Classifying Species of Plant
            - Response:
                Species of certain plants
            - Predictors:
                Sepal lenght, width, whether it opens in the day or night, that kind of thing
            - Goal:
                Both prediction and inference. Honestly you can do both with most methods...and want to...

    b) Describe three real-life applications in which regression might be useful. Describe the response, as well as the predictors. Is the goal of each application inference or prediction? Explain your answer.

        pass - not challenging

    c) Describe three real-life applications in which cluster analysis might be useful.

        pass - not challenging

- - - -

5. What are the advantages and disadvantages of a very flexible (versus a less flexible) approach for regression or classification? Under what circumstances might a more flexible approach be preferred to a less flexible approach? When might a less flexible approach be preferred?

    ```
    Flexible pros:
    - Low bias, can fit a variety of data sets really well, especially niche data
    - Can get you closer to the best test accuracy, depending on the nature of the data

    Flexible cons:
    - Easy to overfit to data when using smaller datasets or the underlying nature is far simpler
    - Much harder to interpret for inference

    Best circumstances for Flexible:
    - Data is very non-linear and plentiful
    - Inference doesn't matter as much as prediction (i.e. predicting stock values)

    Best circumstances for Inflexible:
    - Data is fairly linear or sparse
    - Inference is desirable, so an interpretable model would be better for the task
    ```

- - - -

6. Describe the differences between a parametric and a non-parametric statistical learning approach. What are the advantages of a parametric approach to regression or classification (as opposed to a non-parametric approach)? What are its disadvantages?



- - - -

7. In the table below there is provided a training data set containing six observations, three predictors, and one qualitative response variable. Suppose we wish to use this data set to make a prediction for Y when X_1 = X_2 = X_3 = 0 using K-nearest neighbors.

    Obs | X_1 | X_2 | X_3 | Y
    --- | --- | --- | --- | -------
    1   | 0   | 3   | 0   | Red
    2   | 2   | 0   | 0   | Red
    3   | 0   | 1   | 3   | Red
    4   | 0   | 1   | 2   | Green
    5   | -1  | 0   | 1   | Green
    6   | 1   | 1   | 1   | Red

    a) Compute the Euclidean distance between each observation and the test point, X_1 = X_2 = X_3 = 0.

    b) What is our prediciton with K = 1? Why?

    c) What is our prediction with K = 3? Why?

    d) If the Bayes decision boundary in this problem is highly non-linear, then would we expect the best value for K to be large or small? Why?

- - - -
