# project-using-cnn
Cat vs Dog Classifier using CNN with MobileNetV2 
# 🐾 Cat vs Dog Classifier using CNN MobileNetV2

📌 **Project Overview**  
This project performs binary image classification to distinguish between cats and dogs using **MobileNetV2** as the base model. It was built and trained in **Google Colab** using the **Oxford IIIT Pet dataset**, with a user-friendly **Gradio interface** that supports webcam and image uploads.

---

⚙ **Technologies Used**

- Python  
- TensorFlow / Keras  
- TensorFlow Datasets (`tfds`)  
- Google Colab  
- Matplotlib  
- Gradio  
- MobileNetV2 (Pretrained on ImageNet)

---

📁 **Dataset**

The dataset is taken from:  
**Oxford IIIT Pet Dataset** via `tensorflow_datasets`

It contains labeled pet images with various breeds. Labels were simplified as:  
- `Cat` if label < 12  
- `Dog` if label >= 12

---

🚀 **How It Works**

1. **Mount Drive**: Save/load the trained model in Google Drive  
2. **Data Preparation**:
   - Downloaded using `tfds`
   - Preprocessed and labeled as binary (`Cat` vs `Dog`)
   - Split into 80% training and 20% validation  
3. **Model**:
   - MobileNetV2 (frozen base)
   - GlobalAveragePooling → Dense(128) → Dense(1, sigmoid)
4. **Training**:
   - 5 epochs (can be increased)
   - Saved to Google Drive
5. **Gradio Interface**:
   - Accepts webcam or image input
   - Shows prediction with confidence
   - Rejects low-confidence predictions as "Invalid image"

---

📊 **Results**

- Achieved good binary classification accuracy (~90%+ with fine-tuning)
- Plotted training/validation accuracy and loss using Matplotlib
- Deployed interactively with Gradio

---

🖼 **Example Output**

🖼 **Example Output**

Predictions:  
**Dog (91.2% confidence)**  
**Cat (88.6% confidence)**  
**Invalid image (not a cat or dog)**

![Output 1](Output%20CNN/output1.png.png)  
![Output 2](Output%20CNN/output2.png.png)  
![Output 3](Output%20CNN/output3.png.png)

---

✅ **Requirements**

Install required libraries using:

```bash
pip install tensorflow tensorflow-datasets gradio matplotlib
