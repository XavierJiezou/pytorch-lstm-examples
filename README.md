# PyTorch LSTM MNIST

Train the MNIST dataset using LSTM model implemented by PyTorch.

## Install

```bash
pip install -r requirements.txt
```

## Usage

```bash
git clone https://github.com/XavierJiezou/pytorch-lstm-examples.git
cd pytorch-lstm-examples
python ./code/train_on_mnist.py
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
