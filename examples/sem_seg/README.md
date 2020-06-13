## Semantic segmentation of indoor scenes

This is for S3DIS semantic segementation task.


### Train
Data will download automaticlly.
I used 4 RTX 2080Ti for distributed training. Run:
```
CUDA_VISIBLE_DEVICES=0,1,2,3 python train.py --phase train --multi_gpus --batch_size 16
```
Lower the batch size if out of memory. The batch size will not influence the test results.


If you want to train model with other gcn layers (for example mrgcn), run
```
python train.py --conv mr --multi_gpus --phase train
```

If you want to change other cofigurations please make a .sh file or change the cofig.py.

Other parameters for changing the architecture are:
```
    --block         graph backbone block type {res, plain, dense}
    --conv          graph conv layer {edge, mr}
    --n_filters     number of channels of deep features, default is 64
    --n_blocks      number of basic blocks, default is 28
```

### Evaluation
Qucik test on area 5, run:

```
python test.py --pretrained_model ./checkpoints/sem_seg_dense-res-edge-28-64-ckpt_best_model.pth --batch_size 32 
```

#### Pretrained Models
Pretrained model is available here [google driver](https://drive.google.com/open?id=1iAJbHqiNwc4nJlP67sp1xLkl5EtC4PU_)

```
python test.py --pretrained_model ./checkpoints/sem_seg_dense-res-edge-28-64-ckpt_best_model.pth --batch_size 4 
```
Lower the batch size if out of memory. The batch size will not influence the test results.

