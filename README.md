# CAMS

This is a PyTorch implementation of [CAMS website](https://cams-hoi.github.io). 

### Environment

Install PyTorch and most other packages we use are listed in [environment.yml](https://github.com/cams-hoi/cams-hoi.github.io/environment.yml). We use the implementation of MANO hand from [manotorch](https://github.com/lixiny/manotorch). 

### Data Preparation

Raw data will be released soon!

### Training Demo: Pliers

After finishing data preparation, you can use the following command to start training.
```
sh experiments/pliers/train.sh [1] [2] [3]
# [1] = GPU IDs you use, eg. 0, 1
# [2] = number of GPUs you use, eg. 2
# [3] = port
```

### Synthesis and Evaluate Demo: Pliers

After training, you will get some outputs in `experiments/pliers/tmp`, use the following command to start synthesizing.
```
sh synthesizer/run.sh [1] [2]
# [1] = aforementioned output path, eg. experiments/pliers/tmp/val/
# [2] = meta data path, eg. data/meta/pliers_meta.torch
```

You have finished generation of new manipulation after synthesizing, the results are in `experiments/pliers/synth`. You can also step forward and run evaluation metrics using the following command.

```
sh eval/run.sh [1] [2]
# [1] = final results path, eg. experiments/pliers/synth
# [2] = name of the file saving evaluation result, eg. eval.txt
```

# Website License

TBD
