# EG-MVSNet
The official implement of EG-MVSNet by PyTorch.

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
