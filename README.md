# 🧠 Convolutional Neural Network for MNIST Digit Classification

### 📘 Overview

This project implements a **Convolutional Neural Network (CNN)** to classify handwritten digits from the **MNIST dataset**.
The MNIST dataset contains 70,000 grayscale images (28×28 pixels each) of digits (0–9).
The model learns to recognise these digits through supervised learning and outputs classification probabilities for each class.

---

## 🎯 Objectives

* Build and train a CNN using TensorFlow/Keras to recognise handwritten digits.
* Demonstrate core deep learning concepts such as convolution, pooling, and activation functions.
* Evaluate accuracy and visualize model performance.
* Provide a clear, modular project structure that can be easily extended.

---

## 🧩 Neural Network Architecture

| Layer                         | Output Shape | Parameters | Description                                         |
| ----------------------------- | ------------ | ---------- | --------------------------------------------------- |
| **Conv2D (32 filters, 3×3)**  | 26×26×32     | 320        | Extracts local features such as edges and textures. |
| **MaxPooling2D (2×2)**        | 13×13×32     | 0          | Reduces spatial dimensions and computation.         |
| **Conv2D (64 filters, 3×3)**  | 11×11×64     | 18,496     | Learns more complex visual patterns.                |
| **MaxPooling2D (2×2)**        | 5×5×64       | 0          | Further compresses the feature maps.                |
| **Flatten**                   | 1600         | 0          | Converts the 2D matrix into a 1D vector.            |
| **Dense (128 units, ReLU)**   | 128          | 204,928    | Fully connected layer for high-level reasoning.     |
| **Dense (10 units, Softmax)** | 10           | 1,290      | Output layer for digit classification (0–9).        |

**Optimizer:** Adam
**Loss Function:** Categorical Crossentropy
**Metrics:** Accuracy

---

## 📊 Model Performance

| Metric                  | Result   |
| ----------------------- | -------- |
| **Training Accuracy**   | ≈ 99%    |
| **Validation Accuracy** | ≈ 99%    |
| **Test Accuracy**       | ≈ 98–99% |

Visual outputs include confusion matrices, sample predictions, and accuracy/loss plots.

---

## ⚙️ Project Structure

```
CNN_MNIST_Project/
│
├── data/
│   └── data_out_pt1.npz         # Training and Test Data
│
├── src/
│   └── CNN_mnist.ipynb
│
├── requirements.txt            # Python dependencies
├── README.md                   # Project overview and usage instructions
```

This modular design keeps your code organized, maintainable, and easy to extend.

---

## 🧰 Requirements

To install dependencies locally:

```bash
pip install -r requirements.txt
```

**Example `requirements.txt`:**

```
tensorflow
numpy
matplotlib
pandas
```

If you’re running the notebook in **Google Colab**, these libraries are already preinstalled.

---

## ▶️ Running the Project in Google Colab

1. Open [Google Colab](https://colab.research.google.com/).
2. Upload the `notebooks/CNN_mnist.ipynb` file.
3. Ensure GPU acceleration is enabled:

   * Go to **Runtime → Change runtime type → Hardware accelerator → GPU**.
4. Run all cells sequentially (`Shift + Enter`).

The notebook will:

* Load and preprocess the MNIST dataset.
* Build and train the CNN model.
* Evaluate test performance.
* Visualize accuracy, loss, and predictions.

---

## 🚀 Future Improvements

* Implement **data augmentation** for improved robustness.
* Save and deploy the trained model as a web app or API service.
* Experiment with deeper architectures or transfer learning.

---

## 🧾 License

This project is provided for **educational and research purposes**.
You may modify or extend it with proper attribution.

---

## 👤 Author

**Developed by:** Michael Di Giantomasso
**LinkedIn:** [linkedin.com/in/michael-di-giantomasso](https://www.linkedin.com/in/michael-di-giantomasso-3b1043243/)
