# XAI for AC-OPF

This repository consists of example codes extracted from the paper
["An Explainable AI Framework for AC Optimal Power Flow"](https://ieeexplore.ieee.org/document/11177141).

This paper uses NREL's [OPF-Learn](https://ieeexplore.ieee.org/document/9817509), code available
[here](https://github.com/NREL/OPFLearn.jl), as a dataset to evaluate a feedforward neural network for solving the AC
optimal power flow (AC-OPF) problem. The objective of the paper is not to provide a highly complex or state-of-the-art
AI aglorithm, but rather to demonstrate interpretability and trustworthiness of a fundamental neural network applied to
critical infrastructures, such as power systems.

The neural network is trained using OPF-Learn dataset. The data are pre-processed then fed into a feedforward neural
network whose parameters are determined using a grid search algorithm. Then the outputs are checked for feasibility.
Finally, interpretability is performed using [Expected Gradients](https://arxiv.org/abs/1906.10670),
[SHAP](https://proceedings.neurips.cc/paper/2017/hash/8a20a8621978632d76c43dfd28b67767-Abstract.html), and Mean
Attributtions (introduced in this paper)

The algorithm requires basic knowledge of Julia and Python (TensorFlow,
[Path Explain](https://github.com/suinleelab/path_explain), [SHAP](https://github.com/shap/shap), and other famous
libraries).

The instructions on how to run this code are found in the following notebooks:

- [Run neural network for Pg on Colab](https://colab.research.google.com/github/RonaldKfouri/XAI_for_AC-OPF/blob/main/Neural_Network_for_Pg.ipynb)
- [Run neural network for Vg on Colab](https://colab.research.google.com/github/RonaldKfouri/XAI_for_AC-OPF/blob/main/Neural_Network_for_Vg.ipynb)

If you use this work in your research, please cite:

```bibtex
@ARTICLE{11177141,
  author={Kfouri, Ronald and Margossian, Harag},
  journal={IEEE Access},
  title={An Explainable AI Framework for AC Optimal Power Flow},
  year={2025},
  volume={13},
  number={},
  pages={167702-167715},
  doi={10.1109/ACCESS.2025.3614071}}
```
