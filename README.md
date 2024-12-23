## **Adversarial Effects on Medical imaging**

### **Project Description**
This project implements a Generative Adversarial Network (GAN) to generate high-resolution synthetic medical images for lung cancer analysis. The dataset, sourced from Kaggle, focuses on four lung conditions: Tuberculosis (TB), Tumor (TM), Fibrosis (FB), and Normal (FM). The workflow is divided into two stages:
1. **Data Preprocessing** - Conducted in `conversion of dcm and preprocessing.ipynb`, organizing and preprocessing the Kaggle dataset.
2. **GAN Implementation** - Executed in `WGAN Implementation.ipynb`, training the GAN and generating synthetic images.

### **Features**

- **Kaggle Dataset Integration**: Preprocesses and trains on the Medical Deepfakes Lung Cancer Dataset.
- **Two-Stage Workflow**: Separate scripts for preprocessing and GAN implementation.
- **Custom GAN Architecture:** Designed to generate high-resolution (512x512) synthetic medical images.
- **Classes:** Supports four distinct lung condition categories: TB, TM, FB, and FM.
- **Gradient Penalty:** Implements a gradient penalty for improved discriminator stability.
- **Checkpointing:** Automatically saves and resumes training from checkpoints.
- **Visualization**: Displays generated images after each epoch.
- **Metrics Logging:** Logs discriminator and generator loss, along with real and fake image classification accuracy.

## **Dataset**
The dataset is sourced from Kaggle: [Medical Deepfakes Lung Cancer Dataset](https://www.kaggle.com/datasets/ymirsky/medical-deepfakes-lung-cancer). Download the dataset and place it in the appropriate folder before running the preprocessing script.

### **Directory Structure**
- `"conversion of dcm and preprocessing.ipynb"` - Preprocessing script for the dataset.
- `"WGAN Implementation.ipynb"` - GAN training and implementation script.
- `train/` - Contains preprocessed training images organized by class labels.
- `test/` - Contains preprocessed testing images organized by class labels.
- `checkpoint.pth` - Stores saved model weights and optimizer states.

### **Dependencies**
- Python 3.9
- PyTorch
- NumPy
- Matplotlib

Install dependencies using:
```bash
pip install torch numpy matplotlib
```

### **Usage**
1. Clone the repository:
   ```bash
   git clone https://github.com/saadhvi-r28/Adversarial-Effects-on-Medical-Imaging.git
   cd Adversarial-Effects-on-Medical-Imaging
   ```
2. Preparing the dataset:
   - Training data is placed in `./train`.
   - Testing data is placed in `./test`.

3. Run training:
   - Run the preprocessing script (`"conversion of dcm and preprocessing.ipynb"`) to prepare the dataset:
    ```bash
    python "conversion of dcm and preprocessing.ipynb"
    ```
   - Run the GAN implementation script (`"WGAN Implementation.ipynb"`) to start training:
    ```bash
    python "WGAN Implementation.ipynb"
    ```

4. Monitor progress:
   - Training loss and accuracy metrics are displayed after each epoch.
   - Generated images are visualized and saved during training.

5. Resume training:
   - Ensure `checkpoint.pth` is present in the working directory, and the training script will automatically load it.

### **Output**
- Preprocessed datasets saved in structured folders.
- Generated synthetic images for each lung condition.
- Saved generator and discriminator models for further use or analysis.
- Final model weights for the generator and discriminator.

### **Acknowledgment**
This project uses the [Medical Deepfakes Lung Cancer Dataset](https://www.kaggle.com/datasets/ymirsky/medical-deepfakes-lung-cancer) provided on Kaggle.
