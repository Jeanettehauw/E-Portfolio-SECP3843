# 🖼️ Image Classification Using Convolutional Neural Network

> A deep learning project implementing and optimizing Convolutional Neural Networks (CNNs) to automatically detect features and classify images without manual feature extraction[cite: 3].

**Prepared By:** 
* Neo Li Xin[cite: 3]
* Richard Yonathan Julio Clay Heng[cite: 3]
* Jeanette Hauw Chandra[cite: 3]

**Institution:** Faculty of Computing, Universiti Teknologi Malaysia (UTM)[cite: 3]  
**Course:** SECP3843-01 - Special Topic in Data Engineering[cite: 3]

---

## 📖 Overview

Artificial Intelligence has brought revolutionary changes to processing and comprehending visual information[cite: 3]. While traditional machine learning requires tedious and imprecise manual feature extraction, Convolutional Neural Networks (CNNs) solve this by automatically detecting features within images[cite: 3]. This project explores the implementation of CNNs to categorize images into 10 distinct classes (such as airplanes, automobiles, birds, and cats) using the CIFAR-10 dataset[cite: 3].

## 🏗️ System Architecture & Workflow

The image classification pipeline leverages a hierarchical deep learning structure:

| Layer / Step | Function | Description |
| :--- | :--- | :--- |
| 📥 **Data Preprocessing** | **Normalization & Reshaping** | The CIFAR-10 dataset (50,000 training and 10,000 testing images) is loaded, reshaped into one-dimensional arrays, and normalized by dividing pixel values by 255.0 to improve training stability[cite: 3]. |
| 🔍 **Convolution Layer** | **Feature Extraction** | Extracts relevant image features, such as edges and shapes, using kernels[cite: 3]. Parameter sharing is utilized to detect features regardless of their location in the image[cite: 3]. |
| 📉 **Pooling Layer** | **Dimensionality Reduction** | Reduces the size of the feature map without losing significant information, which lowers computational complexity and helps avoid overfitting[cite: 3]. |
| 🧠 **Fully Connected Layer** | **Classification** | Uses the automatically extracted features to generate output predictions and classify the image[cite: 3]. |

## 💻 Technology Stack

* **Programming Language:** `Python`[cite: 3]
* **Deep Learning Frameworks:** `TensorFlow`, `Keras`[cite: 3]
* **Numerical Operations:** `NumPy`[cite: 3]
* **Data Visualization:** `Matplotlib`, `Seaborn`[cite: 3]

## ✨ Key Features & Enhancements

- [x] **Baseline Models Comparison:** Initially implemented an Artificial Neural Network (ANN) which yielded ~48% accuracy, and a baseline CNN which achieved ~69.95% accuracy[cite: 3].
- [x] **Error Pattern Analysis:** Identified that the model reliably distinguishes broad groups but occasionally confuses visually similar classes (e.g., misclassifying animals as other animals, or vehicles as other vehicles)[cite: 3].
- [x] **Advanced Regularization:** Added `Batch Normalization` layers to stabilize data flow and a `Dropout` layer to randomly turn off neurons during backpropagation, effectively minimizing the risk of overfitting[cite: 3].
- [x] **Hyperparameter Optimization:** Improved learning efficiency and model stability by lowering the learning rate to 0.0002, increasing the batch size to 128, introducing a 0.1 validation split, and extending the training duration to 50 epochs[cite: 3].

---

## 💡 Project Reflection

<details>
<summary><b>Click to expand the project reflection</b></summary>

### Connecting Technical Design with Real Decision Making
Implementing the data architecture and BI dashboard provided a very concrete lesson in connecting technical design with real decision-making[cite: 3]. Working from raw source systems through ETL processes into a star-schema warehouse demonstrated that establishing clean and consistent definitions for KPIs matters just as much as utilizing any specific tool[cite: 3]. 

### Key Learnings & Takeaways
* **Data Quality & Standardization:** Dealing with data quality issues, clarifying the grain of each fact table, and standardizing business terms sometimes felt tedious[cite: 3]. However, these efforts directly reduced confusion for end-users and ensured the final dashboard felt reliable[cite: 3].
* **User-Centric Systems:** The project highlighted the importance of building data systems for people, rather than just for technical correctness[cite: 3]. Early versions were technically sound, but user feedback was crucial in revealing which visuals were confusing and which questions remained unanswered[cite: 3].
* **Continuous Improvement:** Iterating on feedback to simplify views and document key design choices made the solution much easier to adopt and maintain[cite: 3]. Ultimately, the team gained a stronger appreciation for making small, continuous improvements and for keeping communication lines open between data practitioners and stakeholders[cite: 3].

</details>
