## Inspiration
Alzheimer’s disease affects millions of families worldwide. Early detection, which can improve treatment outcomes and patient quality of life, remains a major challenge due to the complexity and subtlety of the disease’s progression. We were inspired to harness the power of deep learning to analyse medical images and make early, objective risk predictions accessible to every clinician and patient.
## What it does

## How we built it
Data Loading and Preprocessing:
We converted raw brain scan images from byte arrays, normalised and reshaped them, and ensured label integrity.

Model Architecture:
We designed a custom CNN, adapting it to our image data dimensions and classes. Further, we explored transfer learning (EfficientNet) for improved accuracy.

Training and Evaluation:
Using PyTorch, we implemented a robust training loop, careful device management, and validation checks. Our model achieved near-perfect accuracy with a loss curve showing rapid, steady improvement.

Error Handling:
We overcame crucial challenges—including CUDA device-side errors and label mismatches—by restarting the runtime, validating inputs, and ensuring all tensors were correctly placed on the GPU.

Interpretability:
Optional enhancements included GradCAM visualisations, empowering clinicians to see which image regions influenced the prediction.

## Challenges we ran into
Device Errors:
Early attempts resulted in CUDA accelerator and device-side errors, mainly caused by mismatched tensor types and invalid label values.

Data Quality:
Ensuring labels stayed within the correct range was essential for stable training and evaluation.

Model Optimisation:
We iterated through batch sizes, learning rates, and architectural tweaks to balance accuracy and generalisation.

## Accomplishments that we're proud of
Built an end-to-end AI system: Developed a robust deep learning pipeline for early Alzheimer’s detection using real-world brain scan data.

Overcame technical challenges: Navigated and resolved complex CUDA and model architecture errors, ensuring stable and accurate training.

Achieved high performance: Our model reached a test accuracy of 97.3%, demonstrating strong generalization and reliability.

Created interpretable results: Enhanced clinical trust by implementing tools for visualizing model decisions on medical images.

Made a positive impact in healthcare: Designed a solution accessible to clinicians and patients, with potential for real-world deployment.

## What we learned
Throughout this project, we learned how artificial intelligence can transform healthcare by identifying patterns and features in data that often escape the human eye. We deepened our understanding of:

Image preprocessing and conversion of biomedical data for model consumption.

Convolutional neural networks (CNNs) and transfer learning for medical image analysis.

The critical importance of handling class labels, device placement, and robust error-checking in model pipelines.

Evaluating models beyond accuracy—including loss curves, confusion matrices, and interpretability.

## What's next for Alzheimer's AI
Expand dataset diversity: Incorporate more brain scans from varied demographics to strengthen generalization and fairness.

Deploy clinically: Collaborate with healthcare institutions to validate the model in real hospital settings and assist doctors in early intervention.

Add multi-modal analysis: Integrate medical history, genetic data, and lifestyle factors to enhance accuracy and personalization.

Enable real-time diagnosis: Optimize the model for rapid, on-device predictions in clinics and mobile apps.

Advance explainability: Further develop tools like GradCAM and saliency mapping to boost clinician trust and regulatory approval.

Continuous learning: Update the model as new data arrives, ensuring it adapts to evolving medical standards and discoveries.
