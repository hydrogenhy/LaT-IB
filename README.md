# AAAI26 | Is the Information Bottleneck Robust Enough? Towards Label-Noise Resistant Information Bottleneck Learning

This repository provides the official implementation of LaT-IB, a method designed to address a key limitation of the classical Information Bottleneck (IB) framework: its vulnerability to label noise.

LaT-IB reformulates the IB objective in the latent representation space and introduces a new principled objective that improves robustness under noisy labels. Furthermore, we provide upper and lower bound analysis to theoretically justify the information meaning and effectiveness of our formulation.

![Framework](./compare.png)
![Framework](./Framework.png)

We conduct extensive experiments on two representative tasks to validate LaT-IB:

- Image Classification
- Graph Node Classification

The results consistently demonstrate that LaT-IB achieves better robustness and generalization under noisy supervision.

```
./
├── IC (image classification, LaT-VIB)
│   ├── LaT_VIB.py
│   ├── README.md
│   ├── attack.py
│   ├── data
│   │   ├── animal_10N.py
│   │   ├── cifar.py
│   │   ├── datasets.py
│   │   └── utils.py
│   ├── log
│   ├── model
│   │   ├── __init__.py
│   │   ├── modelIB.py
│   │   └── resnet.py
│   ├── test_attack.py
│   ├── utils
│   │   ├── fmix.py
│   │   ├── loss.py
│   │   ├── mix.py
│   │   └── randaug.py
│   └── visual.py
├── NC (ndoe classification, LatT-GIB)
│   ├── LaT_GIB.py
│   ├── Noise_about.py
│   ├── README.md
│   ├── arg.py
│   ├── data
│   ├── data_loader.py
│   ├── log
│   ├── loss.py
│   ├── model.py
│   └── utils.py
├── README.md
└── tree.py
```

---

## Environment requirement

### IC

- torchvision
- PIL
- sklearn
- matplotlib (optional)

### NC

- torch_geometric
- torch_sparse

