🛰️ Change Detection Model

Deep learning model for satellite image change detection.
Fully GPU-optimized and ready to run in Google Colab.

📚 Overview

This project includes everything needed to detect changes between two satellite images using a U-Net (ResNet34) model.

Included files:

best_change_detection_model.pth – trained model

ChangeDetection.ipynb – full pipeline notebook

A.zip – before images (LEVIR-CD test set)

B.zip – after images (LEVIR-CD test set)

You can run the entire workflow directly in Colab with GPU, or locally if you prefer.

## 📁 Folder Structure

```
change_detection/
│
├── best_change_detection_model.pth      # Trained PyTorch model
├── ChangeDetection.ipynb                # Full inference + batch processing notebook
├── README.md                            # Documentation
├── A.zip                                # Before images (LEVIR-CD)
└── B.zip                                # After images (LEVIR-CD)
```

After unzipping in Google Colab:

```
/content/A
/content/B
```

Each folder contains matching before/after image pairs  
(example: `1001.png` exists in both folders).


Each folder contains matching before/after image pairs
(example: 1001.png exists in both folders).


Each folder contains matching before/after images
(example: 1001.png exists in both folders).

🚀 Running in Google Colab (Recommended)

Upload all files into Google Drive

Open ChangeDetection.ipynb in Google Colab

Go to: Runtime → Change runtime type → GPU

Run all cells from top to bottom

The notebook already covers:

Model loading

Image preprocessing

Batch processing for A/B dataset

Generating masks

Creating visual overlays

Saving all results

No extra scripts required.

🔧 Running Locally

Install dependencies:

pip install torch torchvision torchaudio
pip install segmentation-models-pytorch pillow numpy


PyTorch automatically uses GPU if available.

🗂️ Using A.zip and B.zip (Batch Testing)

Unzip inside Colab:

!unzip A.zip -d /content/A
!unzip B.zip -d /content/B


The notebook includes a ready-to-use loop that:

Reads filenames from A and B

Runs inference for each pair

Saves masks and overlays in a results folder

🖼️ Output

The model generates:

Binary change mask

White = change

Black = no change

Optional overlay where changed pixels are highlighted in red

Saved outputs for each image pair:

results/
├── 1001_mask.png
├── 1001_overlay.png
├── 1002_mask.png
├── 1002_overlay.png
└── ...

📝 Notes

Input images must be RGB and same resolution

The notebook handles normalization automatically

Model expects a 6-channel tensor (A + B)

Default threshold is 0.5, editable inside the notebook

GPU usage is strongly recommended for performance

✔️ Ready to Use

Everything is set up so you can:

Upload

Open the notebook

Run

Get results

No extra configuration needed.

If you want, I can also prepare:

A PDF version of this README

A banner image

A version formatted like a premium GitHub project
