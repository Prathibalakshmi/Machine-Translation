# Machine-Translation
Machine Translation
Machine translation or MT refers to fully automated software that can translate source content into target languages. Humans may use MT to help them render text and speech into another language.nMT tools are often used to translate vast amounts of information involving millions of words that could not possibly be translated the traditional way. It is a sub-field of computational linguistics that investigates the use of software to translate text or speech from one language to another.

Question:
Implement a seq2seq model (using LSTM and any deep learning framework of your choice) to perform machine translation from English Language to French Language. The dataset is available here: http://www.manythings.org/anki/ Download the fr-eng.zip file, which contains the txt file containing the English sentence followed by its French translation (separated by tab). Use only the first few thousands records and not the complete dataset. Make sure that all the necessary preprocessing steps are done prior to feeding the dataset to the model. Use the glove representation for word embedding (as it gives one representation per sentence

Objective:
The objective is to implement a seq2seq model to perform machine translation from English Language to French Language and use the glove representation for word embedding (as it gives one representation per sentence

Explanation
What is Seq2Seq Modelling ? Sequence-to-sequence learning (Seq2Seq) is about training models to convert sequences from one domain (e.g. sentences in English) to sequences in another domain (e.g. the same sentences translated to French). Our aim is to translate given sentences from English language to French. Sequence-to-Sequence (seq2seq) models are used for a variety of NLP tasks, such as text summarization, speech recognition, DNA sequence modeling, among others. Here, both the input and output are sentences. In other words, these sentences are a sequence of words going in and out of a model. This is the basic idea of Sequence-to-Sequence modeling.


Here's how it works: Feed the embedding vectors for source sequences (English), to the encoder network, one word at a time. Encode the input sentences into fixed dimension state vectors. At this step, we get the hidden and cell states from the encoder LSTM, and feed it to the decoder LSTM. These states are regarded as initial states by decoder. Additionally, it also has the embedding vectors for target words (French). Decode and output the translated sentence, one word at a time. In this step, the output of the decoder is sent to a softmax layer over the entire target vocabulary.

What is LSTM ? Long Short-Term Memory (LSTM) networks are a modified version of recurrent neural networks, which makes it easier to remember past data in memory. The vanishing gradient problem of RNN is resolved here. LSTM is well-suited to classify, process and predict time series given time lags of unknown duration. It trains the model by using back-propagation. In an LSTM network, three gates are present:


Input gate — discover which value from input should be used to modify the memory. Sigmoid function decides which values to let through 0,1. and tanh function gives weightage to the values which are passed deciding their level of importance ranging from-1 to 1.


Forget gate — discover what details to be discarded from the block. It is decided by the sigmoid function. it looks at the previous state(ht-1) and the content input(Xt) and outputs a number between 0(omit this)and 1(keep this)for each number in the cell state Ct−1.


Output gate — the input and the memory of the block is used to decide the output. Sigmoid function decides which values to let through 0,1. and tanh function gives weightage to the values which are passed deciding their level of importance ranging from-1 to 1 and multiplied with output of Sigmoid.

