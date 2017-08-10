Google Developers

Why care about RNN's?
One to One - image classifcation
One to many - image to caption
Many to one - sentiment analysis
Many to many - translation

Color bot is char-rnn
Generates colors at the character level
Input is one hot encoding of text
Output is vector, but then stack layers on top

Colorbot
Uses for loop for RNN layers    
Sorting sequences by length so that the RNN runs faster


Phonemes you get for free in a RNN
(Maybe not with small dataset)
HMM may be different
Deep learning - don't need to do as much feature engineering (text, images, etc).  Let the network handle it.
More [here](https://github.com/mari-linhares/tensorflow-workshop/tree/master/workshops/GDG_nyc_colorbot_10_07_2017)

Is there some hidden psychology revealed? [Yes, deep dream](https://www.youtube.com/watch?v=9ziVGkt8Gg4)