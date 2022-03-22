# Sequence-to-Sequence-Learning-with-Neural-Networks

# Overview
- DNNs cannot be used to map sequences to sequences. This paper addresses this issue and presents a general end-to-end approach to sequence learning using Long Short-Term Memory (LSTM).
- The main result from conducting experiements from the paper is that on an English to French translation task from the WMT'14 dataset.

### About the data
- This dataset has about 700 million words.
- The model has 60000 input words and 80000 output words.
- 4 layers of 1000D cells LSTM, 8000 dimensional state.
- Trains only on 30% of the training data

# Existing problem 
Though very powerful, DNNs cannot map sequences to sequences. It can only map vectors to vectors. Meanwhile, RNNs can work with sequences but have trouble learning the long dependencies. 

### Solution
LSTM architecture is the soultion to learn long term dependecies. RNNs overwrite the hidden state but LSTMs add to the hidden state.A multilayered Long Short-Term Memory (LSTM) is used to map the input sequence to a vector of a fixed dimensionality, and then another deep LSTM to decode the target sequence from the vector. This general end-to-end approach to sequence learning, improves the statistical machine translation (SMT) e.g.: English to French translation task.



### Approach 
There have been a number of related attempts to address the general sequence to sequence learning problem with neural networks.


### Framework : Sequence to Sequence (Seq2Seq) Model

![alt text](https://github.com/muthusm/Sequence-to-Sequence-Learning-with-Neural-Networks/blob/main/Presentation/image1.png)

#### Function

Estimate the conditional probability p where x is an input sequence and y is its corresponding output sequence whose length T′ may differ from T.
 Here : p(y1,…,y′T|x1,…,xT), x(x1,…,xT) and y(y1,…,y′T)
 
![alt text](https://github.com/muthusm/Sequence-to-Sequence-Learning-with-Neural-Networks/blob/main/Presentation/image4.png)


#### Training

Maximize the log probability of a correct translation T given the source sentence S.
![alt text](https://github.com/muthusm/Sequence-to-Sequence-Learning-with-Neural-Networks/blob/main/Presentation/image5.png)


#### Decoding

Produce translations by finding the most likely translation according to the LSTM.
![alt text](https://github.com/muthusm/Sequence-to-Sequence-Learning-with-Neural-Networks/blob/main/Presentation/image6.png)

### Results

#### 2D PCA Projection

![alt text](https://github.com/muthusm/Sequence-to-Sequence-Learning-with-Neural-Networks/blob/main/Presentation/image2.png)


#### Long sentences
![alt text](https://github.com/muthusm/Sequence-to-Sequence-Learning-with-Neural-Networks/blob/main/Presentation/image3.png)



# Discussion Topic 1
Cover first chosen topic, ask a question for the class to discuss

# Discussion Topic 2
Cover second chosen topic, ask a question for the class to discuss

# Discussion Topic 3
Cover third chosen topic, ask a question for the class to discuss

# Critical Analysis
Answer one or more of the following questions: What was overlooked by the authors? What could have been developed further? Were there any errors? Have others disputed the findings?

# Resource Links
Prepare links of where to go to get more information (other papers, models, blog posts (e.g. papers with code))

# Code Demonstration
Make a Jupyter notebook demonstrating using the model

# Link to Video
Will be uploaded soon.
