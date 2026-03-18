# Segmentation-with-partial-cross-entropy
a training strategy for image segmentation where models learn from incomplete or noisy annotations by ignoring unlabeled pixels during loss calculation. This is achieved by setting weights for masked or unknown pixel classes to zero in a weighted cross-entropy function, focusing only on labeled regions.
