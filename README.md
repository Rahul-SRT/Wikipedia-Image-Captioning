#  Wikipedia Image Captioning Project

Welcome to the **Wikipedia Image Captioning Project**! This project creates a machine learning model that can write high-quality captions for images in Wikipedia articles. These captions will help make Wikipedia more accessible, especially for visually impaired readers, and improve how people search and understand visual content on Wikipedia. 

##  Project Goals

- **Accurate Captions**: Create captions that are informative and sound like Wikipedia.
- **Accessibility**: Help visually impaired users by adding text descriptions for images.
- **Better Search**: Make Wikipedia’s images easier to find by adding useful information.

---

##  Dataset

We are using the **wikiImgCaption** dataset from [Kaggle](https://www.kaggle.com/c/wikipedia-image-caption/data). It includes:
- **Images**: A mix of images covering topics you find on Wikipedia.
- **Captions**: Human-written descriptions of the images.
- **Metadata**: Additional information, like image titles, categories, and tags, that help create better captions.

---

##  Model Architecture

### 1. Vision-Language Pre-trained Model (VLP)
Our first model uses existing models like **CLIP** and **ViLBERT** that are trained to understand both images and text. This helps create captions that fit the image context.

### 2. CNN + LSTM Model
Our second model uses:
- **CNN**: A neural network that focuses on image features like shapes and colors.
- **LSTM**: A neural network that writes captions word-by-word based on the CNN’s output.

### Fine-Tuning
- **Masked Language Modeling (MLM)**: We hide certain words during training so the model learns to describe images more accurately.
- **Image-Text Matching (ITM)**: We train the model to match images with the right captions and avoid mistakes.

---

##  Evaluation Metrics

To check how well our captions work, we use:
- **BLEU Score**: Measures how close our captions are to human-written captions.
- **CIDEr Score**: Measures how similar captions are for the same image.
- **Human Evaluation**: Manually check for quality, accuracy, and Wikipedia style.

---

##  Deployment

We will deploy our model on **Hugging Face**, where people can upload an image and get a caption. We use **Google Colab** to train the model with enough computing power.

---


---

##  Setup & Usage

### Prerequisites
Make sure you have:
- Python 3.8 or later
- Packages listed in `requirements.txt`

### Installation
1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/wikipedia-image-captioning.git
   cd wikipedia-image-captioning

