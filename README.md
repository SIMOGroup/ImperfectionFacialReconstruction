# From Imperfection to Perfection: Advanced 3D Facial Reconstruction Using MICA Models and Self-Supervision Learning

This code is developed on the top of [MICA](https://arxiv.org/pdf/2204.06607) for 3D Face reconstruction, [SwAV](https://arxiv.org/abs/2006.09882) for Self-supervised technique. 
we thank to their efficient and neat codebase. 


## Install requirements 

```bash
$ pip install requirements.txt
```



## Evaluate Self-supervised model's weights 

We provide the pretrained models for **SSL** methods, as listed below: 

| model  | data percentage | pretrained weights |
| :---: | :---: |  :---: |
| SSL-20 | 20  | [GoogleDrive](https://drive.google.com/file/d/1vDS0cMgE8C0Y9PngibsY_kak6OLhy0Y1/view?usp=sharing)|
| SSL-100 | 100 | [GoogleDrive](https://drive.google.com/file/d/1mcGT0Mfp0524bJQpOglEuVq9IYFm-yNE/view?usp=sharing)|


To train **SSL**, run the following command:
```
python -u  ssl_mica.py
```

## Evaluate Downstream tasks 

We provide the pretrained models for **Downstream task** methods, as listed below: 

| model  |  pretrained weights |
| :---: |  :---: |
| BASE-MICA |  [GoogleDrive](https://drive.google.com/file/d/1l403-4DZzYqdpENjrt3YFCXGnhUC-Jm8/view?usp=sharing)|
| SSL-20 |  [GoogleDrive](https://drive.google.com/file/d/1Anw4bZlS9Qk5k_Va2FnYgSMpDsVfUE2S/view?usp=sharing)|
| SSL-100 | [GoogleDrive](https://drive.google.com/file/d/1NHJlNVTRzUL8rWMhvTs6qgECaT6gKHOY/view?usp=sharing)|



To train downstream task without SSL, run the following command: 
```
python -u  downstream_mica.py
```

To train downstream task with SSL, run the following command: 
```
python -u  downstream_ssl_mica.py
```

Example output during training :
```
INFO - 02/08/23 04:00:35 - 0:03:54 - Epoch: [0][350]    Time 0.612 (0.639)     Data 0.000 (0.006)       Loss 0.0001 (0.0293)    Lr: 0.2047
```

## Citation

If you find this work helpful, please kindly consider citing our paper:

```bibtex
@inproceedings{kong2023lasermix,
  title = {From Imperfection to Perfection: Advanced 3D Facial Reconstruction Using MICA Models and Self-Supervision Learning},
  author = {Thinh D. Le, Duong Q. Nguyen, Phuong D. Nguyen, H. Nguyen-Xuan},
  booktitle = {Computer Modeling in Engineering & Sciences},
  year = {2024},
}
```
