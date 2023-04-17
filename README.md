# DeepASD

This is our official code of paper "DeepASD: A deep adversarial-regularized graph learning method for ASD diagnosis with multimodal data".

## Requirements
```
pip install torch==1.13.0+cu117 torchvision==0.14.0+cu117 torchaudio===0.13.0 -f https://download.pytorch.org/whl/cu117/torch_stable.html
```
```
pip install torch-scatter torch-sparse torch-cluster torch-spline-conv torch-geometric -f https://data.pyg.org/whl/torch-1.13.0+cu117.html
```

## Usage
```
bash code/run.sh
```
or
```
python main.py --model DeepASD --dataset ABIDE_A --d 128 --d_hid 32 --d_dis_hidden 128 --lr_GC 0.01 --lr_MP 0.0005
```
```
python main.py --model DeepASD --dataset ABIDE_B --d 256 --d_hid 512 --d_dis_hidden 128
```