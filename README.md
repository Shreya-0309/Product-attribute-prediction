# Product-attribute-prediction
An automated attribute prediction model leveraging ResNet101 and ViT with stacked ensemble learning to improve E-commerce catalog accuracy. 

![Uploading image.png…]()


## Setup Instructions

1. Clone the Repository
If the project is hosted on GitHub, clone the repository to your local machine:

git clone <repository_url>
cd <repository_name>

2. Install Python

python --version

3. Install Dependencies

Install the required libraries listed in the requirements.txt file:

pip install -r requirements.txt

If you encounter version conflicts or missing packages, install them individually:

pip install torch torchvision transformers scikit-learn numpy pandas matplotlib

4. Set Up Input Data

Place the required dataset files in the paths required.

## Model Pre-processing and Training

To efficiently manage memory, we implemented custom data generators that dynamically loaded images during the training process. We used multi-output tensors to encode labels for all attributes simultaneously, enabling our model to learn multiple attributes concurrently. Our training loop extended over several epochs (10 epochs), during which we processed batches of images, computed loss, and generated predictions for each attribute.

For model evaluation, the dataset is divided into training (80\%), validation (15\%), and test (15\%) sets. This partitioning ensures that the model is assessed on unseen data during both validation and testing phases, providing an unbiased measure of performance.

