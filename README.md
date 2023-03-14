QQ809117128  质优价低!!
# 2023-COMP-4446-5046-Assignment-1
NLP   2023 COMP 4446 / 5046 Assignment 1
2023 COMP 4446 / 5046 Assignment 1
Assingment 1 is an individual assessment. Please note the University's Academic dishonesty and plagiarism policy.

Submission Deadline: Friday, March 17th, 2023, 11:59pm

Submit via Canvas:

Your notebook
Run all cells before saving the notebook, so we can see your output
In this assignment, we will explore ways to predict the length of a Wikipedia article based on the first 100 tokens in the article. Such a model could be used to explore whether there are systematic biases in the types of articles that get more detail.

If you are working in another language, please make sure to clearly indicate which part of your code is running which section of the assignment and produce output that provides all necessary information. Submit your code, example outputs, and instructions for executing it.

Note: This assignment contains topics that are not covered at the time of release. Each section has information about which lectures and/or labs covered the relevant material. We are releasing it now so you can (1) start working on some parts early, and (2) know what will be in the assignment when you attend the relevant labs and lectures.
1 - Predicting article length from initial content
This section relates to content from the week 1 lecture and the week 2 lab.

In this section, you will implement training and evaluation of a linear model (as seen in the week 2 lab) to predict the length of a wikipedia article from its first 100 words. You will represent the text using a Bag of Words model (as seen in the week 1 lecture).

1.1 Word Mapping [2pt]
In the code block below, write code to go through the training data and for any word that occurs at least 10 times:

Assign it a unique ID (consecutive, starting at 0)
Place it in a dictionary that maps from the word to the ID

1.2 Data to Bag-of-Words Tensors [2pt]
In the code block below, write code to prepare the data in PyTorch tensors.

The text should be converted to a bag of words (ie., a vector the length of the vocabulary in the mapping in the previous step, with counts of the words in the text).

     
1.3 Model Creation [2pt]
Construct a linear model with an SGD optimiser (we recommend a learning rate of 1e-4) and mean squared error as the loss.

     
1.4 Training [2pt]
Write a loop to train your model for 100 epochs, printing performance on the dev set every 10 epochs.



     
1.1 Measure Accuracy [2pt]
In the code block below, write code to evaluate your model on the test set.

1.2 Analyse the Model [2pt]
In the code block below, write code to identify the 50 words with the highest weights and the 50 words with the lowest weights.


     
2 - Compare Data Storage Methods
This section relates to content from the week 1 lecture and the week 2 lab.

Implement a variant of the model with a sparse vector for your input bag of words (See https://pytorch.org/docs/stable/sparse.html for how to switch a vector to be sparse). Use the default sparse vector type (COO).


     
2.1 Training and Test Speed [2pt]
Compare the time it takes to train and test the new model with the time it takes to train and test the old model.

You can time the execution of a line of code using %time. See this guide for more on timing.







3 - Switch to Word Embeddings
This section relates to content from the week 2 lecture and the week 3 lab.

In this section, you will implement a model based on word2vec.

Use word2vec to learn embeddings for the words in your data.
Represent each input document as the average of the word vectors for the words it contains.
Train a linear regression model.


     
3.1 Accuracy [1pt]
Calculate the accuracy of your model.



     
3.2 Speed [1pt]
Calcualte how long it takes your model to be evaluated.



     
4 - Open-Ended Improvement
This section relates to content from the week 1, 2, and 3 lectures and the week 1, 2, and 3 labs.

This section is an open-ended opportunity to find ways to make your model more accurate and/or faster (e.g., use WordNet to generalise words, try different word features, other optimisers, etc).

We encourage you to try several ideas to provide scope for comparisons.

If none of your ideas work you can still get full marks for this section. You just need to justify the ideas and discuss why they may not have improved performance.

4.1 Ideas and Motivation [1pt]
In this box, describe your ideas and why you think they will improve accuracy and/or speed.

Your answer goes here

4.2 Implementation [2pt]
Implement your ideas


     
4.3 Evaluation [1pt]
Evaluate the speed and accuracy of the model with your ideas


     
In this text box, briefly describe the results. Did your improvement work? Why / Why not?

Your answer goes here
