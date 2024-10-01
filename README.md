# Perceptual Piercing: Human Visual Cue-Based Object Detection in Low Visibility Conditions
A novel machine-learning framework, inspired by the atmospheric scattering model and human visual cortex mechanisms, to enhance object detection under poor visibility scenarios such as fog, smoke, and haze. Implemented a multi-tiered strategy based on human-like visual cues that integrates an initial quick detection, followed by target-specific dehazing, and concludes with an in-depth detection phase.

## Installation

To set up the repository, follow these steps:

1. Clone the repository
```
git clone https://github.com/your_username/perceptual-piercing.git
cd perceptual-piercing
```
2. Create a Virtual Environment
```
python3 -m venv venv
source venv/bin/activate
```
3. Install Required Libraries
```
pip install -r requirements.txt
```
4. Download pre-trained models: Download the YOLOv5 and YOLOv8 pre-trained models and place them in the `models/` directory:

## AOD-NetX

1. Dataset Preparation: Prepare datasets using the corresponding `dataloader.py` script in the `AOD-NetX/` directory.
2. Generate Bounding Box Annotations: Use `yolov5_annotations.py` and `yolov8_annotations.py` scripts to create bounding box annotations from the dataset directory.
3. Model Training: Run `train.py` with clean images, foggy images, and the generated bounding box directory.
4. Model Testing: Execute `test.py` to assess the dehazing performance of the model.

## Evaluation
1. General Dehazing Evaluation: Run `dehazing_evaluation.py` in the `evaluation/` directory to evaluate the performance of any general dehazing method.
2. Foggy Cityscapes Evaluation: Use `test_FC.py` in the `evaluation/` directory to measure dehazing performance on the Foggy Cityscapes dataset.
3. RESIDE Dataset Evaluation: Use `test_RESIDE.py` in the `evaluation/` directory to evaluate dehazing performance on the OTS and RTTS subsets of the RESIDE dataset.
4. Object Detection Performance: Execute `metrics.py` in the `evaluation/` directory to assess object detection performance using the dehazed outputs. 
