# Grapevine Disease Detection

An educational machine learning project exploring image classification of grapevine diseases using TensorFlow.

The project focuses on building a Dockerized workflow for training and evaluating a convolutional neural network. Results are intended for learning purposes and are not production-grade.

---

## Getting Started

### Requirements
- Docker installed and running  
- No local Python, TensorFlow, or GPU required  

### Dataset
The dataset is **not included**. Before running, create the following directory structure locally:

```
data/
train/ (.jpg files named healthy_.jpg or esca_.jpg)
val/ (.jpg files named healthy_.jpg or esca_.jpg)
test/ (.jpg files named healthy_.jpg or esca_*.jpg)
```

---

### Build Docker Image
From the project root:

```bash
docker build -t grape-cnn .
```

---

### Train the Model
Run training inside Docker (mounts current directory into container):
```
docker run --rm -it -v "$(pwd):/workspace" grape-cnn python train.py
```
This will train the model and save `grape_model.keras` to the project directory.

---

### Evaluate the Model
After training completes:
```
docker run --rm -it -v "$(pwd):/workspace" grape-cnn python evaluation.py
```
Outputs include test loss, precision, and recall.
