## **Adversarial Effects on Medical imaging**

### **Project Description**
This project implements a Generative Adversarial Network (GAN) designed to generate realistic synthetic medical images for lung cancer classification. The GAN is trained on a curated dataset consisting of four lung conditions: Tuberculosis (TB), Tumor (TM), Fibrosis (FB), and Normal (FM). The goal is to aid in adversarial attack research and enhance data augmentation for medical imaging.

### **Features**
- **Custom GAN Architecture:** Designed to generate high-resolution (512x512) synthetic medical images.
- **Classes:** Supports four distinct lung condition categories: TB, TM, FB, and FM.
- **Gradient Penalty:** Implements a gradient penalty for improved discriminator stability.
- **Checkpointing:** Automatically saves and resumes training from checkpoints.
- **Metrics Logging:** Logs discriminator and generator loss, along with real and fake image classification accuracy.

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
- Generated synthetic images for each lung condition.
- Saved generator and discriminator models for further use or analysis.
