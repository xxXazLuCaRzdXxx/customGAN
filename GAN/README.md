## GAN

It stands for Generative Adversarial Networks. In my case, I have used it to generate images similar to those available in the MNIST digits dataset.

## How it works under the hood?

### Theoretically:

A GAN essentially works by playing a minimax gain for during its training.
<br/>
It has 2 components, Generator and Discriminator. Think of Generator as a thief, trying to generate fake images and Discriminator as a detective, trying to identify real and fakes.
<br/>
Generator's role is to fool the discriminator, hence generating images so real that we fool the discriminator. It is this component which after the training phase would generate our desired images.
<br/>
Discriminator's role is to identify real and fake images correctly. Hence, it has to identify the images given by the Generator which were sampled as a noise from a probabilistic distribution as fakes and the ones sampled from the original dataset as real.

### Formally:

Generator and Discriminator are deep neural networks that are trained as a single system, working on the following loss function:

minG maxD V(D,G)    =    Ex∼P𝑑𝑎𝑡𝑎(x) [logD(x)]  +  E𝑧∼P𝑧(z) [log(1−D(G(z)))]

G(z): Generator generates a fake image from noise vector z
<br/>
D(x): Discriminator outputs a probability that input image x is real.
<br/>
P𝑑𝑎𝑡𝑎(𝑥): Distribution of real images. 
<br/>
P𝑧(𝑧): Prior distribution of noise (usually standard normal N(0,1)).
<br/>
<br/>



After training the Generator is used to generate images similar to those in the respective dataset.
