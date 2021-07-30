# CREATIVE SKETCH GENERATION
Songwei Ge, Vedanuj Goswami & C. Lawre1113ce Zitnick, Devi Parikh, ICLR 2021
### Summary
In this paper DoodlerGAN is proposed, which is a part-based Generative Adversarial Network (GAN). SketchRNN was the early approach to this direction with a a sequence-to-sequence Variational Autoencoder (VAE) later approaches incorporated a convolutional encoder to capture the spatial layout of sketches.  SketchGAN adopted a conditional GAN model as the backbone to generate the missing part. 
### Main points of the paper
- DoodlerGAN is a part-based GAN which draws any doodle part by part instead of drawing as whole. 

- DoodlerGAN instead of mimicking human drawings, it is used for sketches that are not seen in human drawings. 

- DoodlerGAN basically consists of 2 parts 

    -- Part Selector module 

-- Part Generator module 
