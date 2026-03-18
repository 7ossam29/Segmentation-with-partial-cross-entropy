# Segmentation-with-partial-cross-entropy
a training strategy for image segmentation where models learn from incomplete or noisy annotations by ignoring unlabeled pixels during loss calculation. This is achieved by setting weights for masked or unknown pixel classes to zero in a weighted cross-entropy function, focusing only on labeled regions.


📌Weakly Supervised Semantic Segmentation
📖 Overview

This project implements a semantic segmentation model for remote sensing images using sparse point annotations instead of full pixel labels, reducing annotation cost.

🧠 Method

Backbone: ResNet (18, 34, 50)

Head: FCN-style segmentation

Loss: Partial Cross-Entropy

Uses only labeled pixels

Ignores others with ignore_index = -1

📊 Experiments & Results
🔹 Number of Points

Best performance at 250 points

More points → not always better (due to noise & redundancy)

🔹 Backbone

ResNet34 performed best

ResNet18 → underfitting

ResNet50 → overfitting

🔹 Epochs

Best at 10 epochs

More epochs → overfitting

🖼️ Output

Model generates:

Segmentation maps

Overlay visualizations

📌 Key Takeaways

Works well with sparse supervision

Balance between model size and data is critical

Training must be carefully controlled

🛠️ Tech Stack

Python, PyTorch

ResNet, FCN
