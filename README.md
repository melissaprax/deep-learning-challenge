# Deep Learning Challenge (Neural Networks)

## Overview

For the deep learning challenge, I've used sklearn and tensorflow to create a machine learning model. After reviewing the accuracy of the model, I made several attempts to change parts of the model to further optimize it.

## Purpose of analysis

The nonprofit foundation Alphabet Soup wants a tool that can help it select the applicants for funding with the best chance of success in their ventures. With your knowledge of machine learning and neural networks, you’ll use the features in the provided dataset to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup.

## Data Preprocessing

What variable(s) are the target(s) for your model?

- The 'IS_SUCCESSFUL' column from application_df

What variable(s) are the features for your model?

- AFFILIATION—Affiliated sector of industry
- CLASSIFICATION—Government organization classification
- USE_CASE—Use case for funding
- ORGANIZATION—Organization type
- STATUS—Active status
- INCOME_AMT—Income classification
- SPECIAL_CONSIDERATIONS—Special considerations for application
- ASK_AMT—Funding amount requested

What variable(s) should be removed from the input data because they are neither targets nor features?

-EIN (column)
-NAME (column)

## Compiling, Training, and Evaluating the Model

How many neurons, layers, and activation functions did you select for your neural network model, and why?

In my first pass of my neural network model, I used two layers — one layer that contained eight neurons and another that contained 5. I wanted to keep the number of neurons on the lower side to see what the achieved output would be and then, if necessary, increase upon optimiziation.

![alt text](./Screen%20Shot%202023-08-10%20at%204.08.54%20PM.png)

### Were you able to achieve the target model performance?

The goal was to achieve a 75% or higher accuracy score. On my first attempt at the Alphabet Soup Charity model, I was able to get a 71.8% accuracy.

![alt text](./Screen%20Shot%202023-08-10%20at%204.28.44%20PM.png)

### What steps did you take in your attempts to increase model performance?

I already was using relu activation type, which is probably why my first attempt had such a high accuracy. Knowing that, I didn't want to change the activiation type, so I looked into other options.

I chose to keep all the columns in the model, instead of dropping EIN and NAME column like the starter code had me do in the first model attempt.

I also chose to add more neurons to both layers, doubling the number of neurons in the two layers compared to my first attempt.

![alt text](./Screen%20Shot%202023-08-10%20at%204.31.15%20PM.png)

I wanted to take small steps while optimizing the model so I was able to understand what was helping or hurting the accuracy score.

By doubling the number of neurons in my layers and keeping in all columns, the accuracy slightly rose compared to my first attempt to 72.5%.

As I still was unable to achieve 75% in my second attempt, I decided to try a third attempt in hopes I could get closer. I kept additional neurons that I added but this time, instead of keeping all the columns, I wondered what would happen if I not only drop EIN and NAME like I did in the first attempt, but also dropped several others.

![alt text](./Screen%20Shot%202023-08-10%20at%204.35.41%20PM.png)

Unfortunately, that didn't help me get increased accuracy. After running my model, my accuracy was only 68.8%.

### Describe how you could use a different model to solve the same problem, and explain why you would use that model

I would be curious to try a classifier-type model to see if logistical regression would creeate a more accuracte output. As the instrcutions for this project only focused on accuracy as a metric for analysis, I only focused on what each model's accuracy way. It could be also helpful to add more metrics when compiling the model to see what analysis could be derived from understanding the model in a more multi-faceted way.

