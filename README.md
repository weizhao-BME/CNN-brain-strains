# CNN-brain-strains (Work in progress)
Convolutional neural network for efficient estimation of  regional brain strains
## Authors:
Shaoju Wu, Wei Zhao, Kianoosh Ghaz, and Songbai Ji
## Prerequisites
- System: MacOS/ Linux (e.g: Ubuntu 16.04)
- Matlab 2017 or above
- [Python 2.7](https://www.anaconda.com/distribution/)
- [Scikit-Learn](https://scikit-learn.org/stable/install.html)
- [Scipy](https://www.scipy.org/)
- [Keras 2.08](http://faroit.com/keras-docs/2.0.8/#installation)
- [Tensorflow 1.4.0](https://pypi.org/project/tensorflow/1.4.0/#files)
## Data preprocessing:
- Resampling the impact profile to 1 ms (temporal resolution) 
- Conjugate axis transform
- Shifting based on resultant peak location
- Replicated padding 

## Preprocessing demo example:
![](https://github.com/Jilab-biomechanics/CNN-brain-strains/blob/master/figures/preprocessing.png)

## Pretrained models:
Three pretrained CNN neural network models are provided based on all of the brain response samples available in the published study (N=3069). They correspond to the peak maximum principal strain (MPS) of the whole brain (WB), MPS of the corpus callosum (CC), and fiber strain (FS) of the CC, all assessed at the 95th percentile levels. 

## Additional Evaluations:
The accuracy of the trained CNN using real-world impacts is extensively reported in the published paper. Here, we further report the CNN-estimation accuracy using a separate, [idealized rotational impact dataset](https://link.springer.com/article/10.1007%2Fs10439-017-1888-3) (N=1521). This additional testing dataset is completely unseen by the trained CNN. The accuracy for MPS of the whole brain in terms of coefficient of determination (R^2) and root mean squared error (RMSE) are shown below:
![](https://github.com/Jilab-biomechanics/CNN-brain-strains/blob/master/figures/Testing_results.png)

We further train the CNN using the idealized impacts (N=1521) with the same CNN architecture. The resulting 10-fold cross-validation accuracy is shown below (virtually perfect performance).


## License:
CNN-brain-strains is an open-source library and is licensed under the [GNU General Public License (v3)](https://www.gnu.org/licenses/gpl-3.0.en.html). 
