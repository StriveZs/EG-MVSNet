# EG-MVSNet
The current project page provides pytorch code that implements the following paper.
Title: "Edge aware depth inference for large-scale aerial building multi-view stereo'

Abstract:
Aerial building depth estimation is a crucial task in 3D digital urban reconstruction and learning-based multi-view stereo (MVS) methods have recently shown promising results in this field. However, these methods are mainly developed by modifying the general learning-based MVS framework for aerial depth estimation, which lack consideration about the intrinsic structures of buildings and result in insufficient accuracy. Therefore, we propose an end-to-end edge aware depth inference network for large-scale aerial building multi-views stereo, called EG-MVSNet, which incorporates the building edge information and jointly estimate the depth map and edge map. Firstly, we propose a novel Edge-Sensitive Network based on the differentiable Dynamic Sobel Kernels to obtain reliable building edge features while eliminating other irrelevant features. We further propose an UNet-like Edge Prediction Branch and a Building Edge-Depth Loss to constrain the model focus primarily on the building edge features. Notably, the pseudo ground truth (GT) edge map for each aerial image is obtained with classical gradient operators which do not require additional annotation. Secondly, to incorporate the edge features into the depth prediction module, we introduce an Inter-volume Adaptive Fusion Module that adaptively incorporates the edge features volume into a standard cost volume and guides the regularization of the cost volume. An Edge Depth Refinement Module is further proposed to performs 2D-guidance refinement and avoid over-smoothed or blurred depth boundaries. Extensive experiments on the WHU dataset and LuoJia-MVS dataset show that our model significantly outperforms state-of-the-art performance by more than 22% mean absolute error (MAE) compared to RED-Net and 57% MAE compared to MVSNet. Additionally, to validate our proposed model, we reconstruct a synthetic aerial building benchmark based on WHU dataset. The results as far as correctness and accuracy exceeded the results of other MVS methods in a between-method comparison by at least 12% in MAE metric.

## Code
### Train
1. In ```train.py```, set ```mode``` to ```train```, set ```model``` to ```egnet```
   
2. In ```train.py```, set ```trainpath``` to your train data path ```YOUR_PATH/dataset/train```, set ```testpath``` to your train data path ```YOUR_PATH/dataset/test```

3. Train EG-MVSNet (RTX 3090 24G):
```
python train.py
```

### Test
1. In ```train.py```, set ```testpath``` to your train data path ```YOUR_PATH/dataset/test```,
   set ```loadckpt``` to your model path ```./checkpoints/xx/xxx.ckpt```, set depth sample number ```numdepth```.

2. Run EG-MVSNet (RTX 3090 24G):
```
python train.py 
```
