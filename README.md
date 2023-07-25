# Weakly-Supervised Convolutional Neural Networks for Vessel Segmentation in Cerebral Angiography 
By Arvind Vepa, Andrew Choi, Noor Nakhaei, Wonjun Lee, Noah Stier, Andrew Vu, Greyson Jenkins, Xiaoyan Yang, Manjot Shergill, Moira Desphy, Kevin Delao, Mia Levy, Cristopher Garduno, Lacy Nelson, Wandi Liu, Fan Hung, Fabien Scalzo

This is the repository with code and data for [Weakly-Supervised Convolutional Neural Networks for Vessel Segmentation in Cerebral Angiography](https://openaccess.thecvf.com/content/WACV2022/html/Vepa_Weakly-Supervised_Convolutional_Neural_Networks_for_Vessel_Segmentation_in_Cerebral_Angiography_WACV_2022_paper.html) (WACV 2022).  If you use any of our code or data, please cite:

```bib
@inproceedings{vepa2022weakly,
  title={Weakly-Supervised Convolutional Neural Networks for Vessel Segmentation in Cerebral Angiography},
  author={Vepa, Arvind and Choi, Andrew and Nakhaei, Noor and Lee, Wonjun and Stier, Noah and Vu, Andrew and Jenkins, Greyson and Yang, Xiaoyan and Shergill, Manjot and Desphy, Moira and others},
  booktitle={Proceedings of the IEEE/CVF Winter Conference on Applications of Computer Vision},
  pages={585--594},
  year={2022}
}
```

## Overview

We are currently in the progress of hosting our data and code base on Github. Please check back soon for updates.

- [x] Provide Cerebral DSA Dataset (including both sets of test annotations)
- [x] Provide code for training and testing segmentation models
- [ ] Provide code for generating weak annotations (baseline methods and our proposed method)
- [ ] Provide our generated weak annotations (including HIL)
- [ ] Provide code to general results on DRIVE
- [ ] Provide code/readme for experimentation and analysis

## Dataset

In our paper, we introduced the Cerebral DSA Dataset as well as provided results on the well known DRIVE dataset. Please see the paper for more details on the DSA dataset. The DSA dataset is provided in `data/dsa`. We have provided the train images and test images as well as their ground-truth annotations (including two sets of test annotations). For the benefit of those using our code, we have already converted the groundtruth annotations to `.npy` to be used by the models.  

## Requirements

We have tested our code on Windows 10 with Torch 1.12.1 and Torchvision 0.13.1 with CUDA 11.6 and Python 3.7.9. Our code should be able to work in other environments with minor modifications. We have also included a `requirements.txt` file. We recommend installing those libraries prior to installing Torch and Torchvision.

## Usage

1. Clone the project
```
git clone https://github.com/arvindmvepa/dsa-vessel-seg.git
cd dsa-vessel-seg
```
2. Checkout the latest versions of the submodules
```
git submodule update --init --recursive --remote
```
3. Launch Jupyter Notebook
```
jupyter notebook
```
4. Train the model

Run the train_exp.ipynb notebook. Note that you will need to change the paths to the data and annotations. Additionally, the train notebook is useful for generating results for several parameters. Feel free to peruse the code and add parameters as needed.

5. Test the model

Run the inf_exp.ipynb notebook. Note that, again, you will need to change the paths to the data and annotations. You can provide several parameters - like test metrics. Again, feel free to peruse the code and add parameters as needed.


## Questions

Feel free to reach out to Arvind at [arvind.m.vepa@gmail.com](arvind.m.vepa@gmail.com) with any questions or concerns.