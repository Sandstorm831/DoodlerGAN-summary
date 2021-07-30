# CREATIVE SKETCH GENERATION
Songwei Ge, Vedanuj Goswami & C. Lawre1113ce Zitnick, Devi Parikh, ICLR 2021
### Summary
In this paper DoodlerGAN is proposed, which is a part-based Generative Adversarial Network (GAN). SketchRNN was the early approach to this direction with a a sequence-to-sequence Variational Autoencoder (VAE) later approaches incorporated a convolutional encoder to capture the spatial layout of sketches.  SketchGAN adopted a conditional GAN model as the backbone to generate the missing part. 
### Main points of the paper
- DoodlerGAN is a part-based GAN which draws any doodle part by part instead of drawing as whole. 
- DoodlerGAN instead of mimicking human drawings, it is used for sketches that are not seen in human drawings.
- DoodlerGAN basically consists of 2 parts
    - Part Selector module 
    - Part Generator module 
- Part Selector predicts which part to be drawn next whereas Part Generator draws the raster image of the part. 
- Part generator is a Conditional GAN based upon the styleGAN2 Architecture. It uses a 5-layer styleGAN2 generator with [512,256,128,64,32] output channels starting from 4x4x64 constant feature map. For encoding the input partial sketches, it uses a 5-layer CNN with [16, 32, 64, 128, 256] output channels. It downsample the intermediate feature map after each encoder layer and concatenate it channel-wise with the corresponding layers in the generator, giving it access to the hierarchical spatial structure of the input sketch. 
![image](https://user-images.githubusercontent.com/76916164/127710929-148f3840-2d5f-4551-9450-b0d7661a06c9.png)
