# Text-to-Image_synthasizer

**Project Title**

Text-to-Image Synthesizer

**Introduction**

This project implements a two-stage StackGAN architecture for generating text descriptions from images. The model is trained on the CUB-200-2011 dataset, which consists of images of 200 bird species.

**Project Goal**

The primary objective of this project is to develop a robust Image-to-Text Synthesis model capable of generating accurate and detailed textual descriptions for input images. This involves training a deep learning model that can effectively learn the complex relationship between visual and textual information.

**Dataset**

The project uses the CUB-200-2011 dataset, available for download on Kaggle: [https://www.kaggle.com/datasets/thiagojr/cub-200-2011](https://www.kaggle.com/datasets/thiagojr/cub-200-2011)

**Model**

The model is a StackGAN (Stacked Generative Adversarial Network) architecture, which consists of two stacked GANs. The first GAN generates an image representation from the text description, and the second GAN refines the generated image to improve photorealism.

**Model Architecture:**

Stage 1:

Text Encoder: This component processes the input text description into a latent representation.

Image Generator: This component generates a low-resolution image based on the encoded text.

Discriminator: This component differentiates between real images and fake images generated by the Image Generator.

Stage 2:

Refined Image Generator: This component takes the low-resolution image from Stage 1 and refines it to a higher resolution.

Discriminator: This component distinguishes between real high-resolution images and fake ones generated by the Refined Image Generator.

**Training Process:**

Text Encoding: The input text description is fed into the Text Encoder to obtain a latent representation.

Image Generation: The latent representation is used to generate a low-resolution image.

Image Refinement: The low-resolution image is further refined to a high-resolution image.

Discriminator Training: The Discriminator learns to distinguish between real and fake images at both stages.

Generator Training: The Generator is trained to produce images that can fool the Discriminator.

**Dependencies**

* Python (tested with version X.X)
* TensorFlow (tested with version X.X)
* Other libraries (e.g., NumPy, Matplotlib) -  List any other libraries your project requires

**Installation**

1. Clone this repository:

   ```bash
   git clone https://github.com/<your_username>/image-to-text-synthesizer.git
   ```

2. Create a virtual environment (recommended) and activate it.

3. Install the required dependencies:

   ```bash
   pip install -r requirements.txt
   ```

**Usage**

1. Download the CUB-200-2011 dataset and place it in the project directory.

2. Train the model:

   ```bash
   python train.py
   ```

3. Generate text descriptions for images:

   ```bash
   python generate.py <image_path>
   ```
![86a94c8f-800b-4d1e-817b-9f4b8c86ca6b](https://github.com/user-attachments/assets/75ebd8e6-fca9-4246-b195-ecc7d9b8f584)
