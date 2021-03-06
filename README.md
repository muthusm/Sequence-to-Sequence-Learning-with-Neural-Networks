# Sequence-to-Sequence-Learning-with-Neural-Networks

# Overview
1. DNNs cannot be used to map sequences to sequences. This paper addresses this issue and presents a general end-to-end approach to sequence learning using Long Short-Term Memory (LSTM).
2. Sequence Models are the machine learning models that input or output the sequence of data.We cannot use standard neural network., ie DNNs for this kind of data.
3. Though very powerful, DNNs cannot map sequences to sequences. It can only map vectors to vectors. Meanwhile, RNNs can work with sequences but have trouble learning the long dependencies. RNNs also have problems like vanishing (or exploding) gradient/long-term dependency problem where information rapidly gets lost over time.
4. Hence this paper uses a multilayered Long Short-Term Memory (LSTM) to map the input sequence
to a vector of a fixed dimensionality, and then another deep LSTM to decode the target sequence from the vector. 
5. The main result from conducting experiements from the paper is that on an English to French translation task from the WMT'14 dataset.

### About the data
- This dataset has about 700 million words.
- The model has 60000 input words and 80000 output words.
- 4 layers of 1000D cells LSTM, 8000 dimensional state.
- Trains only on 30% of the training data



### Solution
LSTM architecture is the solution to learn long term dependecies. RNNs overwrite the hidden state but LSTMs add to the hidden state.A multilayered Long Short-Term Memory (LSTM) is used to map the input sequence to a vector of a fixed dimensionality, and then another deep LSTM to decode the target sequence from the vector. This general end-to-end approach to sequence learning, improves the statistical machine translation (SMT) e.g.: English to French translation task.



### Approach 
There have been a number of related attempts to address the general sequence to sequence learning problem with neural networks. Different LSTMs for input(encoder) and output(decoder) languagues


### Framework : Sequence to Sequence (Seq2Seq) Model

![alt text](https://github.com/muthusm/Sequence-to-Sequence-Learning-with-Neural-Networks/blob/main/Presentation/image1.png)

#### Function

Estimate the conditional probability p where x is an input sequence and y is its corresponding output sequence whose length T??? may differ from T.
 Here : p(y1,???,y???T|x1,???,xT), x(x1,???,xT) and y(y1,???,y???T)
 
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
Why DNNs and basic RNNs cannot be used for sequence to sequence learning?

# Discussion Topic 2
Why does the authors reversed the order of the words of the input sentence and then feeded to the LSTM.General thoughts on reversing input sentences? Any similar models?

# Discussion Topic 3
Why do we require that each sentence in LSTM ends with a special end-of-sentence symbol "<EOS>"?

# Critical Analysis
The output sequence relies heavily on the context defined by the hidden state in the final output of the encoder, making it challenging for the model to deal with long sentences. In the case of long sequences, there is a high probability that the initial context has been lost by the end of the sequence. The hidden state vector is a fixed-size length and thus it is hard for the encoder to encapsulate/compress all the information from the sentence. If the input is long, it can suffer from what is called the information bottleneck. Inability to correctly translate very rare words: end-to-end NMTs tend to have relatively small vocabularies with a single unk symbol that represents every possible out-of-vocabulary (OOV) word

# Resource Links
- Paper Link : https://arxiv.org/abs/1409.3215
- https://www.analyticsvidhya.com/blog/2020/08/a-simple-introduction-to-sequence-to-sequence-models/
- https://github.com/tensorflow/nmt
- https://www-nlp.stanford.edu/pubs/luong2016iclr_multi.pdf
- https://staff.fnwi.uva.nl/m.derijke/wp-content/papercite-data/pdf/jiang-why-2018.pdf
- https://adacheng.github.io/paper_note/2019/06/11/Sequence-to-Sequence-Learning-with-Neural-Networks/
- https://nlp.stanford.edu/projects/nmt/
- https://karpathy.github.io/2015/05/21/rnn-effectiveness/
 https://arxiv.org/pdf/1410.8206.pdf
- https://medium.com/nlp-chatbot-survey/paper-review-4-sequence-to-sequence-learning-with-neural-networks-40ce8f66b1e2
- https://medium.com/analytics-vidhya/how-seq2seq-sequence-to-sequence-models-improved-into-transformers-using-attention-mechanism-9905fb88d5ef

 
## [Code Demonstration](https://github.com/muthusm/Sequence-to-Swquence-Learninr-with-Neural-Networks/blob/main/cOde%20Demonstration/code_demonstration.ipynb)


## [Link to Video](https://youtu.be/DjGq1TAbNlE)
