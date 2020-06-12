# PIAO_TAIREN_GCN_Final_DeepGCNs
 Course GCN final project

This repository is highly borrowed from original paper's code.
This repository is only for the final porject.
After that it would be deletede.

## DeepGCNs: Can GCNs Go as Deep as CNNs?
* [Paper](https://arxiv.org/pdf/1904.03751.pdf)

<div style="text-align:center"><img src='./misc/intro.png' width=800>

<div style="text-align:center"><img src='./misc/pipeline.png' width=800>


## Requirements
* [Pytorch>=1.4.0](https://pytorch.org)

There are many package version requirements so please just install a new conda enviroment to run the code.

Install enviroment by runing:
```
conda env create -f deepgcn.yml
```

## Code Architecture
    .
    ├── misc                    # Misc images
    ├── utils                   # Common useful modules
    ├── gcn_lib                 # gcn library
    │   ├── dense               # gcn library for dense data (B x C x N x 1)
    │   └── sparse              # gcn library for sparse data (N x C)
    ├── examples 
    │   ├── sem_seg_dense       # code for point clouds semantic segmentation on S3DIS (data type: dense)
    │   ├── sem_seg_sparse      # code for point clouds semantic segmentation on S3DIS (data type: sparse)
    │   ├── part_sem_seg        # code for part segmentation on PartNet
    │   └── ppi                 # code for node classification on PPI dataset
    └── ...

## How to train, test and evaluate our models
Please look the details in `Readme.md` of each task inside `examples` folder.
All the information of code, data, and pretrained models can be found there.

## Contact
PIAO TAIREN
E-mail: piaotairen@snu.ac.kr
