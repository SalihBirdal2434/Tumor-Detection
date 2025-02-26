# Brain CT Analysis Project

## Overview
The Brain CT Analysis Project is designed to assist in the detection and analysis of brain tumors and aneurysms using Computed Tomography (CT) scans. Leveraging advanced machine learning techniques, this project aims to provide accurate and reliable diagnostics to support medical professionals in clinical decision-making.

## Dataset
This project utilizes the [Computed Tomography (CT) of the Brain](https://www.kaggle.com/datasets/trainingdatapro/computed-tomography-ct-of-the-brain) dataset from Kaggle, which includes a comprehensive collection of brain CT scans. The dataset contains images in DICOM format, focusing specifically on cases involving tumors and aneurysms.

## Features
- **Tumor Detection:** Identifies and classifies various types of brain tumors.
- **Aneurysm Detection:** Detects the presence of aneurysms within the brain CT scans.
- **DICOM Support:** Fully compatible with DICOM format, ensuring seamless integration with medical imaging systems.
- **User-Friendly Interface:** Intuitive dashboard for easy navigation and analysis of CT scans.
- **High Accuracy:** Utilizes state-of-the-art algorithms to ensure precise detection and minimal false positives.

## Requirements
- Python 3.7+
- TensorFlow / PyTorch
- OpenCV
- pydicom
- scikit-learn
- NumPy
- pandas
- matplotlib / seaborn

## Installation
1. **Clone the Repository**
    ```bash
    git clone https://github.com/yourusername/brain-ct-analysis.git
    cd brain-ct-analysis
    ```

2. **Create a Virtual Environment**
    ```bash
    python3 -m venv venv
    source venv/bin/activate
    ```

3. **Install Dependencies**
    ```bash
    pip install -r requirements.txt
    ```

4. **Download the Dataset**
    - Download the dataset from [Kaggle](https://www.kaggle.com/datasets/trainingdatapro/computed-tomography-ct-of-the-brain).
    - Extract the files and place them in the `data/` directory.

## Usage
1. **Preprocess the Data**
    ```bash
    python preprocess.py --input_dir data/raw/ --output_dir data/processed/
    ```

2. **Train the Model**
    ```bash
    python train.py --data_dir data/processed/ --model_dir models/
    ```

3. **Evaluate the Model**
    ```bash
    python evaluate.py --model_dir models/ --test_data data/processed/test/
    ```

4. **Run Inference**
    ```bash
    python inference.py --model_dir models/ --input_image path/to/image.dcm
    ```

## Limitations
- **Scope:** This project is specifically tailored for the detection of tumors and aneurysms in brain CT scans. It does not support other types of brain anomalies.
- **Format:** Only works with CT scans in DICOM format. Non-DICOM formats are not supported and will require conversion before processing.
- **Dataset Dependency:** The accuracy and performance are dependent on the quality and diversity of the dataset provided. Limited variations in the dataset may affect the model's generalizability.

## Contributing
Contributions are welcome! Please fork the repository and submit a pull request for any enhancements or bug fixes.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contact
For any inquiries or support, please contact [your.email@example.com](mailto:your.email@example.com).

