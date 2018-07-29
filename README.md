# PoemGeneration

This project utilizes the concept of Recurrent Neural Networks and the uses the benefits of LSTM over Recurrent Neural Networks(RNN).
The reason behind using LSTM is because while generating text, context is important. Which word comes after whom differentiates the sentence from being deep or profound to downright non-sensical.

Steps involved in the procedure:

1> Importing Dependencies
Required: Keras, Pandas, Numpy

2> Importing Data
Here the data contained in 'sonnets.txt' is the full compilation of Shakespeare's literary works containing poems.

3> Character Mapping
This step is required as the RNN's work much better with numbers than with text. And moreover text is anyway converted to numerical representation anyway.

4> Data Preprocessing
The data that is input to the network must be reshaped such that training data and testing data can be created. Further, how context would be stored would be decided.

5> Modelling
Due to limitations of my current machine and the complete absence of GPU has limited the amount of neurons that can be trained. I am using 3 LSTM layers with 400 neurons each and 3 dropout layers each having a drop ratio of 20%. 
Finally, the output goes through a Dense layer which finally gives out the output.
The activation function can be experimented with to give out better or equal results.

Epochs: 100
Batch_size: 100

6> Generating text
We finally use the generated model to predict one character at a time. We use this characters and generate another character and the cycle goes on.

 

Observations:

Due to the limitations of the machine I am using and no GPU support, the model currently is able to :

create words with proper spelling (most of time)
understands rhyming and tries to incorporate a rhyme scheme
understands the spaces and newlines such that it doesn't create very long sentences.
I am sure better results can be expected by tinkering around with the number of neurons and number of layers while thinking about the vanishing gradient problem.
