# ArtisticStyleTransfer

# Note : For running the .ipynb file on google colab make sure to switch the runtime from cpu to gpu



# Neural Style Transfer: A Neural Algorithm of Artistic Style
This repository implements the Neural Style Transfer algorithm proposed in the paper "A Neural Algorithm of Artistic Style" by Leon A. Gatys, Alexander S. Ecker, and Matthias Bethge. The algorithm introduces an innovative approach to blend the content of one image with the artistic style of another, leveraging deep neural networks.

# Key Components


1.) VGG Model for Feature Extraction:

  - The algorithm utilizes the VGG19 convolutional neural network to extract relevant features from images.
  - Specific layers of the VGG model are chosen to separate content and style information.
2.) Custom VGG Model Implementation:

  - The repository includes a custom VGG model tailored for Neural Style Transfer.
  - The model is designed to extract features from chosen layers, crucial for both content and style representations.
3.) Image Loading and Pre-processing:

  - Images are loaded and pre-processed using the PIL library and torchvision transformations.
  - The pre-processing ensures compatibility with the defined custom VGG model.
4.) Optimization Loop:

  - The optimization loop iteratively updates a generated image to minimize both content and style losses.
  - The total loss, a combination of content and style losses, is calculated and optimized using the Adam optimizer.

    
# Parameters and Configuration:
  - total_steps: The total number of optimization steps, controlling the refinement of the stylized image.
  - Alpha and Beta: Weight factors for content and style losses, influencing the importance of each in the total loss calculation.
  - optimizer: Adam optimizer with a learning rate of 0.001 for image optimization.


Working of VGG19, pretrained on ImageNet
![Screenshot 2023-11-26 020907](https://github.com/MeRonak/ArtisticStyleTransfer/assets/87123160/27de2ef4-4fc0-4ee9-acad-f2a99526d51c)

Layers of VGG
![vgg19](https://github.com/MeRonak/ArtisticStyleTransfer/assets/87123160/6ff390e8-479c-4d66-b742-1f036bbd5c9a)

Original Image to be transformed
![pexels-pixabay-220453-min](https://github.com/MeRonak/ArtisticStyleTransfer/assets/87123160/5569a83f-43d4-4c53-ae93-d3f8406b0e7a)

Artistic Style we want original image to transform into
![art-min](https://github.com/MeRonak/ArtisticStyleTransfer/assets/87123160/b5b79df7-23ce-452a-a106-943ea5d6cf8b)

Result
![generated (1)-min](https://github.com/MeRonak/ArtisticStyleTransfer/assets/87123160/5f89c826-b47e-4c08-a26b-46d4a63e2fb1)


