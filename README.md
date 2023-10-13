# B5Net

This repository contains the code for performing physics-based data augmentation and model training for the prediction of experimental autogenous shrinkage.

## Installation Requirements

The basic requirement for using the files is a Python 3.6.3 environment with the packages listed in requirements.txt. It is advisable to create a virtual environment with the correct dependencies.

The work-related experiments were performed on Linux Fedora 7.9 Maipo. The code should be able to work on other Operating Systems as well, but it has not been tested elsewhere.

## Source Files

Here is a brief description of the files and folder content:

* [`network`](./network): code for training the B5Net model from scratch.

* [`dataset`](./dataset): data used for training B5Net model. 

* data augmentation.ipynb : jupyter notebook to convert the raw composition-based input into physics-based composition-based input and perform augmentation.

## Running the code

The code to run the B5Net model is provided in the network folder. In order to run the model, you can pass a sample config file to the dl_regressors_tf2.py from inside of your network directory:

`python dl_regressors_tf2.py --config_file sample/sample-run_example_tf2.config`

The config file defines all the related hyperparameters associated with the model training and model testing, such as loss_type, training_data_path, val_data_path, test_data_path, label, input_type, etc. To add customized input_type, please make changes to the `data_utils.py`.

## Developer Team

The code was developed by Vishu Gupta from the <a href="http://cucis.ece.northwestern.edu/">CUCIS</a> group at the Electrical and Computer Engineering Department at Northwestern University.

## Publication

1. Vishu Gupta, Yuhui Lyu, Derick Suarez, Yuwei Mao, Wei-Keng Liao, Alok Choudhary, Wing Kam Liu, Gianluca Cusatis, and Ankit Agrawal. "Physics-based Data-Augmented Deep Learning for Enhanced Autogenous Shrinkage Prediction on Experimental Dataset." In Proceedings of the 2023 Fifteenth International Conference on Contemporary Computing, pp. 188-197. 2023. [<a href="https://dl.acm.org/doi/abs/10.1145/3607947.3607980">DOI</a>] [<a href="https://dl.acm.org/doi/pdf/10.1145/3607947.3607980">PDF</a>]

```tex
@inproceedings{gupta2023physics,
  title={Physics-based Data-Augmented Deep Learning for Enhanced Autogenous Shrinkage Prediction on Experimental Dataset},
  author={Gupta, Vishu and Lyu, Yuhui and Suarez, Derick and Mao, Yuwei and Liao, Wei-Keng and Choudhary, Alok and Liu, Wing Kam and Cusatis, Gianluca and Agrawal, Ankit},
  booktitle={Proceedings of the 2023 Fifteenth International Conference on Contemporary Computing},
  pages={188--197},
  year={2023}
}
```

## Disclaimer

The research code shared in this repository is shared without any support or guarantee of its quality. However, please do raise an issue if you find anything wrong, and I will try my best to address it.

email: vishugupta2020@u.northwestern.edu

Copyright (C) 2023, Northwestern University.

See COPYRIGHT notice in the top-level directory.

## Funding Support

This work was performed under the following financial assistance award 70NANB19H005 from the U.S. Department of Commerce, National Institute of Standards and Technology, as part of the Center for Hierarchical Materials Design (CHiMaD). Partial support is also acknowledged from DOE awards DE-SC0014330, DE-SC0019358, and DE-SC0021399.
