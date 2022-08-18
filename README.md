# Machine translation pipeline from English to French

## Introduction
As a part of Udacity Natural Language Processing project, this is a machine translation pipiline from English to French project to accept English text as input and return the French translation through deep neural network.

### Text Preprocessing
The input data will be tokenised (sequences of integers), and then added padding in order to make all the tokenised data the same length.

### Simple RNN model
Basic RNN model to take a baseline for sequence data. This project uses GRU, Gated Recurrent RNN, in the first layer, and the model is passed through a TimeDistributed Dense layer to flatten for producing the logits, which represents the output for translated French word.

### RNN model with embedding layer
Basic RNN model using Embedding layer to represent the words in n-dimensional space (n is the size of the embedding vectors) for better representation of words.

### Bidirectional RNN
Bidirectional recurrent neural networks to allow the model to see the future input, the sequence from the end to the beginning, as well as the sequence from beginning to the end.

### Simple encoder decoder layer
This model uses encoder creating a matrix representation of the sentence (using bidiretional RNN layer), and repeat vector layer which holds encoder state for decoding. The decoder using bidiretional RNN layer decodes the encoded value into the appropriate dimension space for translation.

### Final model with applying all techniques
The model uses Embedding layer passed to Encode and Decode layer to represent the sentences in dense space.

---

## Datasets
The datasets for this project contains a small vocabulary considering a time to train. Each English and French vocaburalies are stored in `data` folder to load.

## Instructions

1. Download the both vocabulary files, and then place them to a main folder so that `machine_translation.ipynb` can access the datasets.
2. Modify `machine_translation.ipynb` (`Introduction` and `Load Data` step) according to the environment and folder vocabulary files are stored

## Setup

This project requires GPU acceleration to run efficiently. I used [Google Colab](https://colab.research.google.com/) for this project.

## Required packages to install
- Python 3
- NumPy
- TensorFlow 1.x
- Keras 2.x

## File structure

```
|- `machine_translation.ipynb`
|- `helper.py`
|- `roject_tests.py`
|- `README.md`
|-- `data/`
||- `small_vocab_en`
||- `small_vocab_fr`
```

## License
The contents of this repository are covered under the [LICENSE](https://github.com/ucaiado/machine-translation/blob/master/LICENSE) file.
