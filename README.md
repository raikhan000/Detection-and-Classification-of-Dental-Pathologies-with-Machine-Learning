# Detection and Classification of Dental Pathologies Using Machine Learning

## Overview

This project focuses on detecting and classifying dental pathologies in panoramic X-rays using **Machine Learning** techniques. The main goal is to develop models capable of identifying and categorizing dental conditions, including **caries**, **pulpitis**, **periodontitis**, **treated teeth**, **healthy teeth**, and **prostheses**.

The project utilizes state-of-the-art **Object Detection** models, such as **YOLOv8** and **RetinaNet**, to analyze dental X-ray images and predict the conditions of individual teeth. These models are evaluated using key metrics like **Precision**, **Recall**, and **F1-score**, ensuring accurate and reliable detection of dental pathologies.

## Key Features

- **Teeth Labeling**: The project uses machine learning models to label teeth in panoramic X-ray images. Each tooth is assigned a label (e.g., T1, T2 for upper jaw, B1, B2 for lower jaw).
- **Dental Pathology Classification**: The models predict the dental condition for each tooth, categorizing it into conditions such as **healthy**, **treated**, **caries**, **pulpitis**, **periodontitis**, and **prosthesis**.
- **Multiple Model Comparison**: The project compares two powerful models—**YOLOv8** (optimized for real-time object detection) and **RetinaNet** (known for its detailed feature extraction) to evaluate their performance in a dental context.
- **Performance Evaluation**: The models are evaluated using standard metrics (precision, recall, F1-score) to assess the accuracy of detection and classification. The best-performing models are selected based on these metrics.

## Dataset

The dataset consists of panoramic dental X-ray images, each annotated with the corresponding tooth labels and conditions. Data preparation for this project was done using **CVAT** (Computer Vision Annotation Tool), which was used to annotate the images for the detection and classification of dental pathologies.

Key attributes in the dataset:
- **Image Data**: Panoramic dental X-ray images.
- **Labels**: Tooth labels (T1-T8 for the upper jaw, B1-B8 for the lower jaw) and corresponding pathologies.
- **Annotation Format**: The data was annotated using CVAT to create bounding boxes for teeth and to label them with their respective conditions.

## Methodology

1. **Data Preparation**:
   - The **CVAT** tool was used for labeling teeth and classifying their conditions in the panoramic X-ray images. This tool allowed for efficient and accurate annotation of individual teeth and their associated dental pathologies.
   - The dataset was split into training, validation, and test sets to ensure robust model evaluation.

2. **Model Selection**:
   - **YOLOv8**: This model was chosen for its real-time object detection capabilities. It is well-suited for identifying multiple objects in images and excels at speed and efficiency.
   - **RetinaNet**: This model was selected for its deep architecture and ability to handle complex object detection tasks. It excels in capturing fine-grained features, making it suitable for tasks requiring high classification accuracy.

3. **Training and Evaluation**:
   - Models were trained on the labeled dataset, with specific attention given to performance in detecting dental conditions.
   - Key performance metrics—**Precision**, **Recall**, and **F1-score**—were calculated to assess the models' ability to detect and classify dental conditions accurately.

## Results

The results of the models were compared based on the following:
- **YOLOv8** performed well with fast detection and good accuracy for detecting labeled teeth. However, it faced challenges in distinguishing certain subtle dental conditions.
- **RetinaNet**, with its deeper architecture, showed better performance in terms of classification accuracy but was slower in inference time compared to YOLOv8.
- Precision-Recall curves and F1 scores were used to assess how well each model balanced the tradeoff between false positives and false negatives across different dental conditions.

The following pathologies were detected:
- **Caries**: Identified lesions and decay.
- **Pulpitis**: Inflammation of the pulp.
- **Periodontitis**: Inflammation of the supporting structures.
- **Treated Teeth**: Teeth that had undergone treatments.
- **Healthy Teeth**: Teeth that showed no signs of pathology.
- **Prostheses**: Teeth with dental implants or artificial replacements.

## Evaluation Metrics

- **Precision**: The ratio of correct positive predictions to the total predicted positives.
- **Recall**: The ratio of correct positive predictions to the total actual positives.
- **F1-score**: The harmonic mean of precision and recall, providing a balanced view of model performance.

## Technologies Used

- **Python**: Programming language for implementing the machine learning models.
- **PyTorch**: Framework for building and training the neural networks.
- **YOLOv8**: Used for real-time object detection tasks.
- **RetinaNet**: Used for detecting objects with deep learning architectures.
- **Matplotlib and Seaborn**: Visualization libraries for plotting precision-recall curves and evaluating model performance.

## Challenges and Future Work

- **Class Imbalance**: Some dental conditions, like periodontitis, were less frequently represented in the dataset, which could affect model performance. This challenge can be addressed by employing techniques like class weighting or oversampling.
- **Small Objects**: Detecting small and overlapping teeth in X-rays proved to be challenging for both models. Future work may involve refining the models by incorporating multi-scale detection techniques.
- **Real-time Deployment**: While YOLOv8 performed well in terms of speed, further optimization might be required for real-time clinical deployment.

### Future Directions:
- **Expand Dataset**: Gathering more labeled data with diverse cases can help improve model robustness.
- **Explore Advanced Techniques**: Methods like **Transfer Learning**, **Ensemble Learning**, or **Attention Mechanisms** could be explored to improve the models' ability to capture subtle patterns in dental X-rays.
- **Integrating with Clinical Systems**: Future work could explore how this model can be integrated into dental diagnostic systems to assist in real-time decision-making.

## Conclusion

This project demonstrates the application of **Machine Learning** for the detection and classification of dental pathologies in panoramic X-rays. By comparing models like YOLOv8 and RetinaNet, we gained insights into the strengths and limitations of real-time detection and deep learning architectures for medical image analysis. This work has the potential to assist dental professionals in diagnosing conditions more accurately and efficiently.



