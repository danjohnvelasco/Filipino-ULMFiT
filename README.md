# Filipino-ULMFiT
This is an accompanying repository to my paper:
###  [Pagsusuri ng RNN-based transfer learning technique sa low-resource language](https://arxiv.org/abs/2010.06447)

## Contents
*  instructions to download the pre-trained language model.
*  jupyter notebook to show you how to use the pre-trained model on a text classification task using fastai v2. [[notebook](https://github.com/danjohnvelasco/Filipino-ULMFiT/blob/master/Filipino_ULMFiT.ipynb)]



## Contributions
*  Release a pre-trained AWD LSTM language model in Filipino using fastai v2. [[WikiText-TL-39](https://github.com/jcblaisecruz02/Filipino-Text-Benchmarks#datasets)]
*  Benchmark AWD LSTM to the Hate Speech Dataset. [[reference](https://arxiv.org/abs/1907.00409)]

## Requirements
*  [fastai v2](https://pypi.org/project/fastai/2.0.0/) and up
*  NVIDIA GPU (all experiments were done on Colab w/ Tesla T4)

## Language Model
| Total Epochs | Dataset Size | Train Set | Val Set | Accuracy | Perplexity | Total Training Time | Dataset |
|-|-|-|-|-|-|-|-|
| 20 | 160428 | 90% | 10% | 86.71% | 2.028250 | 26H | [WikiText-TL-39](https://github.com/jcblaisecruz02/Filipino-Text-Benchmarks#datasets) |


## Download pre-trained language model
```bash
# Install gdown
pip install gdown

# Make directory
mkdir models

# Download data
gdown --id 19jdv8-XEbDNiqlm_lPb1csbVZYkn3gfA

# Unzip
unzip pretrained.zip -d models

# Finally
You should see two files inside 'models' directory: 
1. finetuned_weights_20.pth (pre-trained weights)
2. vocab.pkl (vocab) 

This will be used later in language model fine-tuning. 
See accompanying jupyter notebook to see usage.
```

## Acknowledgements
Big thanks to [Blaise Cruz](https://github.com/jcblaisecruz02) for answering my questions and for nudging me in the right direction. 
