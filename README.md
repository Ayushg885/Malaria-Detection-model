🦠 Malaria Cell Classification (VGG19 + Transfer Learning)

A deep-learning project that classifies malaria-infected vs healthy blood cell images using VGG19 transfer learning, image augmentation, class-balancing, and model optimization techniques.

#🚀 Features

CNN model built on VGG19 (ImageNet weights)

Transfer learning + fine-tuning for high accuracy

ImageDataGenerator for augmentation

Class balancing using compute_class_weight

EarlyStopping + ModelCheckpoint

Training history visualization (accuracy & loss plots)

Confusion matrix + classification report

Final saved model: Malaria_model_final3.keras

🧠 Model Architecture

Base Model: VGG19 (include_top=False)

Trainable layers: last 4 layers of VGG19

Custom head:

Flatten

BatchNormalization

Dense(128, ReLU, L1L2 regularization)

Dropout(0.2)

Dense(1, Sigmoid)

Optimizer: AdamW (1e-5)
Loss: Binary Crossentropy

📊 Training

Key steps:

80/10/10 split (train/val/test)

Data augmentation (rotation, zoom, flips, shifts)

Class weights to handle imbalance

20 epochs with early stopping

Training curves and metrics are plotted automatically.

📉 Evaluation

Includes:

Confusion matrix (heatmap)

Precision, Recall, F1-score (classification report)

Validation accuracy & loss graphs

📝 How to Run
pip install tensorflow pandas numpy sklearn seaborn matplotlib


Update dataset_dir inside the script:

dataset_dir = '/path/to/MERGED DATASET MALARIA'


Then run:

python malaria_ayushgupta3.py

📦 Output

After training, the following files are generated:

best_model.h5 — Best checkpoint

Malaria_model_final3.keras — Final saved model

Accuracy/Loss plots

Confusion Matrix heatmap

👨‍💻 Author

Ayush Gupta
B.Tech CSE | AI/ML & Full-Stack Developer
