## GAN

It stands for Generative Adversarial Networks. In my case, I have used it to generate images similar to those available in the MNIST digits dataset.

## How it works under the hood?

### Theoretically:

A GAN essentially works by playing a minimax gain for during its training.
It has 2 components, Generator and Discriminator. Think of Generator as a thief, trying to generate fake images and Discriminator as a detective, trying to identify real and fakes.
Generator's role is to fool the discriminator, hence generating images so real that we fool the discriminator. It is this component which after the training phase would generate our desired images.
Discriminator's role is to identify real and fake images correctly. Hence, it has to identify the images given by the Generator which were sampled as a noise from a probabilistic distribution as fakes and the ones sampled from the original dataset as real.

### Formally:

Generator and Discriminator are deep neural networks that are trained as a single system, working on the following loss function:
[image](https://github.com/user-attachments/assets/b272c3de-a388-4654-a314-cd81a2cd3190)



After training the Generator is used to generate images similar to those in the respective dataset.
