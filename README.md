# cgpdm-lib
Library implementing __Controlled Gaussian Process Dynamical Models__ (C-GPDMs).

Class __GPDM()__ implements original model from __Wang et al. (2005) "Gaussian process dynamical models"__.

Class __CGPDM()__ extends the main class to take into account also the presence of control inputs.

## Installation

To install __cgpdm_lib__ on your system, clone the repository, open it in a terminal and run the following command:

```
pip install .
```

Instead if you want to install the package in *editable* mode run the following command:

```
pip install -e .
```

## Dependencies
- [PyTorch] (https://pytorch.org/)
- [NumPy] (https://numpy.org/)
- [Matplotlib] (https://matplotlib.org/)
- [Scikit-learn] (https://scikit-learn.org/stable/)

## Usage
Open a terminal inside __example/__ folder.
- Run __$ python train_cgpdm.py__ to train CGPDM on a cloth movement dataset (stored inside folder __example/DATA/__) and save the resulting model (inside __example/ROLLOUT/__ folder).

  __train_cgpdm.py__ takes the following command line arguments:
  - __seed__: select the random seed
  - __num_data__: select the number of trajectories used for training
  - __deg__: select the oscillation angle used in data collection (5, 10 or 15)
  - __d__: select the latent space dimension
  - __num_opt_steps__: select the number of optimization steps
  - __lr__: select the optimization learning rate
  - __flg_show__: set to 'True' for showing model results


- Run __$ python load_cgpdm.py__ to load a trained CGPDM and show rollouts on training data.

  __load_cgpdm.py__ takes the following command line argument:
  - __model_name__: model label inside the __example/ROLLOUT/__ folder.

(__train_gpdm.py__ and __load_gpdm.py__ scripts works analogously but applying the original GPDM on the same some cloth movement dataset)

## Citing
If you use this package for any academic work, please cite our original [paper](https://arxiv.org/pdf/2103.06615.pdf).
```bibtex
@article{amadio2021controlled,
  title={Controlled Gaussian Process Dynamical Models with Application to Robotic Cloth Manipulation},
  author={Amadio, Fabio and Delgado-Guerrero, Juan Antonio and Colom{\'e}, Adri{\`a} and Torras, Carme},
  journal={arXiv preprint arXiv:2103.06615},
  year={2021}
}
```
