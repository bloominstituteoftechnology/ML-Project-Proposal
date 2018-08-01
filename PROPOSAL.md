# ML Project Proposal
- Paul Fang
- Training a multi-layer RNN (Recurrent Neural Network) to generate syntactically similar new text, from existing current text
- Training a multi-layer CNN/RNN to automatically predict and generate captions for images

## What track are you choosing (analysis or engineering)?
Engineering/Analysis

## What is your data source?
- [MIT OpenCourseWare](https://ocw.mit.edu/ans7870/6/6.006/s08/lecturenotes/files/t8.shakespeare.txt)
- [MS-COCO dataset](http://cocodataset.org/#home)


## Summarize the status of your data and what cleaning is needed.

- Text corpus from the complete works of Shakespeare, provided by MIT OpenCourseWare, as our baseline training set. 
- Training dataset of over 80,000 annotated images, 12+ GB. Potentially reduce the size of the training set for faster training, preprocess/tokenize the annotations, and split data into training/testing.

## Summarize the structure of your data and what models/techniques work with it.
- The dataset consists of a large and structured set of text that can be optimally trained on by an RNN, given that text is naturally sequential, which makes it ideal for application in the domain of natural language processing.
- The dataset consists of tens of thousands of annotated images that can be optimally trained on by a deep CNN followed by an RNN, given that text is naturally sequential, which makes it ideal for application in the domain of natural language processing.

## What is your overall goal with this project?
- My goal is to implement a multi-layer Recurrent Neural Network using LSTM (long short-term memory) to sucessfully generate new text, from existing text, based on character-level language modeling, trained via Tensorflow. This will potentially give me further insight into the relationship between neural networks and how they can be applied to natural language/linguistics, and allows me to further train neural networks on various other existing texts as well.
- My goal is to implement a multi-layer ensemble CNN/RNN to sucessfully detect and label/caption images, using an attention-based model, trained via Tensorflow. This potentially gives me further insight into how neural networks can be used for image detection and recognition, and allows me to further train neural networks on various other image datasets as well.