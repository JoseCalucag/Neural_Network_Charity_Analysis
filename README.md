<h1 align = "center"> Neural_Network_Charity_Analysis </h1>

<p align = "center">
<img src = "https://www.charitydata.ca/img/charitydata.png" width = "700" height = "150">
 </p>
 
<h2> Overview of the Analysis </h2> 
I have been tasked to create a binary classifier that is capable of predicting whether applicants can be successfull if funded by the charity Alphabet Soup. Coupled with a knowledge of machine learning and neural networks, I will analyize and use features in a dataset containing more that 34,000 organizations that have previously been funded by Alphabet Soup. With this dataset, I can build a model following these three steps:<br>
<br>
1) Preprocessing the data to implement a neural network <br>
2) Compile, train then evaluate the modeled data <br>
3) Optimize the model <br>

<h2> Results </h2>
<h3> Data Preprocessing </h3>
* What variable is considered the target for your model? <br>
I considered using the IS_SUCCESSFUL column as my target. <br>

* What variable(s) are considered to be the features for your model? <br>
The features that we are using are every column except for two columns that we dropped. <br>

* What variable(s) are neither targets nor features, and should be removed from the input data? <br>
I dropped the columns in EIN and nAME as they're mostly used for labeling and don't have any beneifical influence to the model. <br>

<h2> Compiling, Training, and Evaluating the Model </h2> 
* How many neurons, layers, and activation functions did you select for your neural network model, and why? <br>
Upon implementing various factors, th best neural model that I came across was where I used 8 hidden layers while keeping my neurons low as, from previous modeling tests, I saw that the accuracy is higher when using more neuron/parameter samples. Secondly, I settled upon using the relu activation but using the sigmoid activation for my output layer.

<p align = "center">
<img src = "https://github.com/JoseCalucag/Neural_Network_Charity_Analysis/blob/main/Resources/pic1.png">
 </p>

* Were you able to achieve the target model performance? <br>
Albeit this was my best model, I was only able to achieve 73.2%

* What steps did you take to try and increase model performance? <br>
I've tried various methods in seeing how it can impact on the accuracy of the model. <br>
ATTEMPT #1: Try removing all categorical labelling columns ['EIN', 'NAME', 'AFFILIATION', 'USE_CASE', 'ORGANIZATION']. However, it decreased my accuracy. So, I reverted back to my initial model of just removing the 'EIN' and 'NAME'. <br>
ATTEMPT #2: I increased my bin size to create large 'OTHER' grouping to have lesser columns in the dataset. As I say an increase, I considered the larger bin size moving forward. <br>
ATTEMPT #3: I increased the neuron counts which would also raise the sampling parameters. In this case, I saw a decrease in the model from my second attempt. So, moving forward, I looked to decrease the neuron count to see if there was any impact. <br>
ATTEMPT #4: I increased the number of hidden layers while decreasing the neuron count from Attempt #3. Seeing an increase using 8 hidden layers while decreasing the neuron count to see 1/2 of the amount of the total parameters, I considered using 8 hidden layers moving forward while still decreasing the neuron count. <br>
ATTEMPT #5: I tried various types of activiations to see if there was any difference. Unfortunatly, outside of using RELU and SIGMOID, I would either see the same accuracy or worse. <br>

<h2> Summary </h2>
To recap, we started with a large dataset where we preprocessed it by removing some irrelevant data then encoding the IS_SUCCESSFUL column to create a new dataset with the new encoded data. After, we standardized the data, created scaled training and testing sets then implimented various methods to try to acheive a 75% accuracy. Albeit I was only able to achieve an accuracy of 73.21%, I can only rethink and try to consider what other methods that I might have missed. Could I have tried a different Random Forest Classifier? Was there another activation I could have used? Was the dataset not big enough to achieve an successful accuracy? I believe that with the accuracy so close that there is definitely an x factor not considered where I could have achieved my accuracy goal.
