# CATastrophe: Image Inpainting with GANs

![image](https://github.com/user-attachments/assets/c9a8ac31-7ad3-4864-8af1-3fb39af230ff)


CATastrophe is a Generative Adversarial Network (GAN) model for image inpainting. It generates realistic images by filling in missing regions based on the surrounding content. The model consists of a generator and a discriminator, trained in an adversarial setting to improve over time.

## Model Overview
* Generator: A U-Net style network with an encoder-decoder architecture and skip connections. It takes an image with missing parts and reconstructs the missing content.
* Discriminator: A CNN that distinguishes between real and generated images, encouraging the generator to produce realistic inpainted results.
The generator uses a combination of adversarial loss and L1 loss to ensure realistic image generation, while the discriminator's binary cross-entropy loss helps improve realism.

## Training Process
The model is trained on masked images from the Animal Faces Dataset, which contains photos of animals with varied facial features. During training, random masks are applied to images, and the generator learns to fill in these masked areas. The training uses mini-batch gradient descent with the Adam optimizer, and both the generator and discriminator are updated iteratively.

![image](https://github.com/user-attachments/assets/f0a7f1ba-6ffb-4b6d-8b4e-283f8bda7dba)


## Results
After training, the generator is able to fill in missing regions, producing inpainted images. The model is evaluated by comparing generated images to real ones, and it steadily improves as training progresses.

## Demo
You can interact with the trained model: https://huggingface.co/spaces/akrasi/CATastrophe
