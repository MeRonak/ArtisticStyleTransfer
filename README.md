# ArtisticStyleTransfer

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


![Screenshot 2023-11-26 020907](https://github.com/MeRonak/ArtisticStyleTransfer/assets/87123160/27de2ef4-4fc0-4ee9-acad-f2a99526d51c)


