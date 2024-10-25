#  Codes for ACMMM2024 paper ''Improving the Training of the GANs with Limited Data via Dual Adaptive Noise Injection''

We have provided the codes of DANI with Projected GAN on low-shot datasets. The details are shown as follows.

# Dataset

The low-shot datasets can be found in [[link]](https://drive.google.com/file/d/1rWqaVlms55604jrP5t9ShacL6mZKWL8f/view?usp=sharing)

# Requirement

Please follow the Projected GAN [[link]](https://github.com/autonomousvision/projected-gan) to build your conda enviroment.

```
conda env create -f environment.yml
```
```
conda activate pg
```

# Training

To train your own Projected GAN + DANI (FastGAN backbone) on the low-shot dataset (100-shot obama dataset as example), run the following command:

```
python train.py --outdir=training-runs --data="100-shot-obama.zip" --subset=100 --gpus=2 --batch 64 --batch-gpu=32 --cfg fastgan --kimg 70000 --target 0.45 --d_pos first --noise_sd 0.5
```
# Important notes

1. The codes of this module is built upon the codes of the Projected GAN [[link]](https://github.com/autonomousvision/projected-gan) and Diffusion GAN [[link]](https://github.com/Zhendong-Wang/Diffusion-GAN). We thanks a lot for their great work.

2. Feel free to contact me at zzhang55@qub.ac.uk if you have any questions.

# Citation:
