# GAN Model for Number Generation

## Project Overview

This project explores the generation of numerical digit images using a Generative Adversarial Network (GAN). The quality of the generated images is assessed over a series of epochs and further refined through hyperparameter tuning.

## Baseline Model

The initial GAN model was trained with different epoch settings (10, 25, 50) to evaluate the progression of image quality.

- Sample after 10 epochs - Images are indistinct.
- Sample after 25 epochs - Digits become more legible, with '9' and '8' discernible.
- Sample after 50 epochs - 9 out of 16 images are identifiable.

The results indicate a clear improvement in image quality with an increasing number of epochs.

## ReLU Activation Experiment

A variant of the model using ReLU activation instead of LeakyReLU was also tested.

- Sample after 50 epochs with ReLU activation - Images exhibit improved completion and readability.

## Hyperparameter Tuning

Manual experimentation with hyperparameters led to a configuration that outperforms the baseline:

| Parameter | Baseline Model | New Model |
|---|---|---|
| Noise Vector Dimensionality | 100 | 125 |
| Batch Size | 256 | 128 |
| Learning Rate | 1e-4 | 1e-3 |
| Momentum (Beta1) | 0.9 | 0.85 |
| Momentum (Beta2) | 0.99 | 0.85 |

- Sample after 50 epochs post-tuning - The image quality is enhanced with 11 readable digits.

## Conclusions

The experiments demonstrate that both the number of training epochs and the choice of hyperparameters significantly affect the GAN's ability to generate clear and recognizable digit images. The use of ReLU activation and the fine-tuned hyperparameter set show promising improvements over the baseline.

## Future Work

For further refinement, grid search or random search techniques could be employed to systematically explore the hyperparameter space, potentially uncovering even more optimal settings to improve image generation quality.
