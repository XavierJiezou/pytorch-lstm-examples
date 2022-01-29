﻿# PyTorch LSTM MNIST

Train the MNIST dataset using LSTM model implemented by PyTorch.

## Install

```bash
pip install -r requirements.txt
```

## Usage

```bash
git clone https://github.com/XavierJiezou/pytorch-lstm-mnist.git
cd pytorch-lstm-mnist
python ./code/train_on_mnist.py
```

## Config

You can modify the [configuration file](./config/mnist.yaml) before training.

```yaml
data:
  data_root: ./data/mnist # Path to data
  train_ratio: 0.8 # Ratio of training set
  val_ratio: 0.1 # Ratio of validation set
  batch_size: 64 # How many samples per batch to load
  visualize_data_save: ./image/training_data_mnist.png

model:
  input_size: 28 # Number of expected features in the input
  hidden_size: 64 # Number of features in the hidden state
  num_layers: 1 # Number of recurrent layers
  output_size: 10 # Number of expected features in the output

train:
  num_epochs: 100 # How many epochs to use for data training
  sequence_length: 28 # Length of the input sequence
  learning_rate: 0.001 # Learning_rate
  device: cuda:0 # On which a `torch.Tensor` is or will be allocated
  save_path: ./checkpoint/mnist.pth # Path to save the trained model

log:
  sink: ./log/mnist.log # Path to save the logging file
  level: INFO # Logging level: DEBUG | INFO | WARNING | ERROR | SUCCESS | CRITICAL
  format: '{message}' # logging output format. Example: '{time:YYYY-MM-DD at HH:mm:ss} {level} {message}'
  visualize_log_save: ./image/training_log_mnist.png # Path to save the visualization result
```

## Dataset

> MNIST: [http://yann.lecun.com/exdb/mnist/](http://yann.lecun.com/exdb/mnist/)

![mnist](./image/training_data_mnist.png)

## Result

| Dataset | Sequence Length | Input Size | Accuracy |
|---------|-----------------|------------|----------|
| MNIST   | 28              | 28         | 0.9892   |

## Reference

> - pytorch: [https://github.com/pytorch/pytorch](https://github.com/pytorch/pytorch)
> - loguru: [https://github.com/Delgan/loguru](https://github.com/Delgan/loguru)
> - tqdm: [https://github.com/tqdm/tqdm](https://github.com/tqdm/tqdm)
> - numpy: [https://github.com/numpy/numpy](https://github.com/numpy/numpy)
> - pillow: [https://github.com/python-pillow/Pillow](https://github.com/python-pillow/Pillow)
> - matplotlib: [https://github.com/matplotlib/matplotlib](https://github.com/matplotlib/matplotlib)
> - easydict: [https://github.com/makinacorpus/easydict](https://github.com/makinacorpus/easydict)
