# Object Detection on Indian Driving Dataset (IDD) using YOLOv11

This repository contains my Kaggle notebook project focusing on **Object Detection** using the [YOLOv11](https://github.com/ultralytics/ultralytics) architecture on the **Indian Driving Dataset (IDD)**. 

The project demonstrates fine-tuning a YOLOv11 model to detect and classify 15 different object categories commonly found on Indian roads.

## Features
- **Environment Setup:** Verifies GPU availability (supports Dual Tesla T4) and installs the required `ultralytics` library.
- **Dynamic Configuration (`CFG`):** Easily tweak hyperparameters such as epochs, batch size, learning rates, and dataset paths.
- **Data Preparation:** Automatically generates the `data.yaml` configuration required by YOLO for training, validation, and testing splits.
- **Exploratory Data Analysis (EDA):** Includes utility functions to visualize images and class distributions across all dataset splits using `seaborn` and `matplotlib`.
- **Model Training:** Initializes a YOLO model (e.g., `yolo11n.pt`) and trains it on the custom IDD dataset.
- **Inference & Validation:** Performs predictions on test images and evaluates the model's performance.

## Classes Detected
1. animal
2. autorickshaw
3. bicycle
4. bus
5. car
6. caravan
7. motorcycle
8. person
9. rider
10. traffic light
11. traffic sign
12. trailer
13. train
14. truck
15. vehicle fallback

## Getting Started

### Prerequisites

To run the notebook successfully, especially if running outside of Kaggle, you will need:
- Python 3.8+
- PyTorch (with CUDA support recommended)
- `ultralytics`, `pandas`, `numpy`, `matplotlib`, `seaborn`, `PyYAML`, and `opencv-python`.

You can install the primary dependencies with:
```bash
pip install ultralytics pandas numpy matplotlib seaborn pyyaml opencv-python
```

### Usage
If running on Kaggle, simply attach the **Indian Driving Dataset (IDD)** to your notebook environment. The notebook expects the following directory structure inside the `CUSTOM_DATASET_DIR`:
```
/train/images/
/train/labels/
/val/images/
/val/labels/
/test/images/
/test/labels/
```

1. Review and adjust the hyperparameters within the `CFG` class.
2. Run all cells to initialize data configurations, display sample images, and train the YOLOv11 model.
3. Review the outputs in the generated `runs/detect/` folder to analyze the training metrics, validation scores, and final predictions on the test set.

## Attribution
This project was developed on Kaggle. [View the original notebook here](https://www.kaggle.com/code/pranayfadtare777/notebook934aa61c58).
