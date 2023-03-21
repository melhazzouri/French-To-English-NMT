# French To English Translation

Bonjour! Hi!

Within the European Union, French holds the distinction of being the fourth most widely spoken mother tongue, and depending on who you ask, it may even be the second most prevalent.A staggering 80 million individuals worldwide claim French as their first language, with 61 million of them residing in France. French-speaking communities can be found dispersed throughout various regions of the world.

Despite the language's global popularity as the "language of love," it remains challenging for many individuals to acquire French fluency. This is a hurdle that I, too, have encountered, having recently relocated to Montreal, Quebec.  I am using this project to build a Neural Machine Translation model to translate from French to English. 

# Preprocess
For this project, the text will be converted into sequence of integers using the following preprocess methods: 

1- Tokenize the words into ids

2- Add padding to make all the sequences the same length.

### Tokenization

In order for a neural network to perform predictions on text data, the text must first be transformed into a format that the network can comprehend. Text data, such as "dog," is essentially a sequence of ASCII character encodings, which is not directly compatible with the multiplication and addition operations of a neural network. Therefore, the input data needs to be represented as numbers.

To achieve this, one can either assign a unique numerical value to each character or each word in the text data. The former is known as character ids, while the latter is referred to as word ids. Character ids are typically used for models that make predictions on a character-by-character basis, whereas word ids are utilized in models that generate predictions for each word in the text. Word-level models are generally preferred since they are less complex and tend to learn more effectively. Consequently, we will use word ids for our model.

### Padding

When processing a sequence of word ids in batches, it is necessary for each sequence to have the same length. As sentences in a text corpus can vary in length, it is possible to achieve uniformity in sequence length by adding padding at the end of each sequence. This way, all sequences will have the same length, making it easier for the neural network to process them.

### Predictions 

Convert back the final prediction by our model into text format.
