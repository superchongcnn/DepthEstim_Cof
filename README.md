This library is the paper "A Monocular Medical Endoscopic Images Depth Estimation Method Based on a Confidence-Guided Dual-Branch Siamese. Network key code.
The hardware configuration for model training and experiments includes a GPU RTX 4090 with 24.0GB of VRAM, a 14-core AMD EPYC 7453 CPU, 64.4GB of RAM, and a
451.0GB hard drive. The software environment consists of PyTorch 2.0.1, TensorFlow 2.13.0, and Python 3.10.12.

 Some data are available on request from the authors, which sup-
port the findings of this study are available from the corresponding author, Nannan
Chong, upon reasonable request. Other data are not available due to patient privacy
restrictions. All the data involved in the experiment came from publicly available
datasets or were anonymized by hospitals and allowed to be used.
• Code availability: In addition to the programs published on github, please contact
the corresponding author for more details.

![f89bcac59d5deceffef5e784f7f7afe9](https://github.com/user-attachments/assets/eb6c626a-c5e1-428d-918d-68a69b9dd8a0)
![d7022c7ee1de8282653b92f7b6f8f6be](https://github.com/user-attachments/assets/5c78169a-df6e-41cc-ab83-8fd1a6c9031f)


## Usage 

### Installation

```bash
git clone https://github.com/superchongcnn/DepthEstim_Cof
cd DepthEstim_Cof
pip install -r requirements.txt
```

### Running

```bash
python run.py --encoder <decof> --img-path <img-directory | single-img | txt-file> --outdir <outdir> [--pred-only] [--grayscale]
```
Arguments:
- ``--img-path``: you can either 1) point it to an image directory storing all interested images, 2) point it to a single image, or 3) point it to a text file storing all image paths.
- ``--pred-only`` is set to save the predicted depth map only. Without it, by default, we visualize both image and its depth map side by side.
- ``--grayscale`` is set to save the grayscale depth map. Without it, by default, we apply a color palette to the depth map.

For example:
```bash
python run.py --encoder DepthEstim_Cof --img-path assets/examples --outdir depth_vis
```

