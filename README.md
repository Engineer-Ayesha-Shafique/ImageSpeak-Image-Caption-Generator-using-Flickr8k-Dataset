# ImageSpeak-Image-Caption-Generator-using-Flickr8k-Dataset

"ImageSpeak.ipynb," implements an Image Caption Generator using a combination of ResNet for image feature extraction and a Transformer Decoder for generating textual captions. Below is an overview of the main components and functionalities of the code:

## Mounting Drive and Downloading Dataset from Kaggle
The script starts by mounting Google Drive to the Colab environment and downloading the Flickr8k dataset from Kaggle.

https://www.kaggle.com/datasets/adityajn105/flickr8k/data

## ImageSpeak Workflow
The ImageSpeak model is divided into two main steps:

### 1. Feature Extraction using ResNet:

- Utilizes a pre-trained ResNet-18 model to extract image features.
- Removes duplicate images from the training and validation datasets.
### 2. Transformer Decoder Model:

-Implements a Transformer Decoder for generating image captions.
- Preprocesses and tokenizes captions, removes single-character and non-alphabetic words, and pads sequences.
- Creates a vocabulary and maps tokens to IDs.
## Data Loading and Splitting
- Reads captions from a txt file into a Pandas data frame. -
-  Preprocesses captions, removes single-character words and adds start, end, and padding tokens.
- Splits the dataset into training and validation sets.
## Vocabulary Creation
Counts occurrences of each word, creates a vocabulary and generates mappings from index to word and word to index.
## ResNet Feature Extraction
- Extracts ResNet-18 features for training and validation images.
- Saves the feature vectors in pickle files.
## Transformer Decoder Model
- Defines a Transformer Decoder model with positional encoding for caption generation.
- Implements training loop with CrossEntropyLoss and Adam optimizer.
- Saves the best model based on validation loss.
## Model Evaluation and Caption Generation
- Loads the trained model and performs evaluation.
- Uses beam search to generate captions for given images.
## Examples
Demonstrates generating expressive captions for random validation images.
