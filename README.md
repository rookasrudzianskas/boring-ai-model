# Boring AI Models: AI Powered Clothing Design Generator

![boring-ai](https://user-images.githubusercontent.com/38469892/186376884-bc89b1b7-09a9-4b70-b6e1-67b1c8c8ee6c.gif)

[Devpost Link](https://byrookas.com/) |

## Inspiration
Boring Ai Model or Generative AI Network is a generative model that able to generate images by learning the distribution of a large image dataset. I always find AI architectures fascinating as it enables me to generate high-quality arts or design even without the technical or artistic skill in drawing. Recently, I've seen many face editing demonstrations on AI, but never seen manipulation in other datasets. Hence,  I created Boring AI Models an application where you can collaboratively design clothes without high technical expertise.

## What it does
Boring AI Models able to generate clothing images and mix these images. While mixing, you can control which structure or style that you want the clothing to copy. Additionally, you can edit the generated clothing with several given attributes such as dark color, jacket, dress, or coat.

## How I built it
I trained Fashion dataset on a subset of the Lookbook dataset. The total images I trained it on are 8,726 clothing images with a clean background.

After finished training the AI Model, I proceeded to use AISpace method to find important directions in the latent space. Then, I tried to guess what these directions represent and labeled them accordingly. The reason I use AISpace is that it is unsupervised and does not need an attribute classifier.

Finally, I created a UI with TailwindCss UI library. All the development is done on WebStorm Ecosystem. Tailwindcss and Vercel made deployment very easy. I can directly deploy the UI from WebStorm where Vercel will create a proxy from the Vercel server to their domain and the given URL, hence allowing the general public to use the UI or demo. 

## Challenges I ran into
One of the challenges I faced was fixing a memory leak issue. Part of the code keeps crashing, and I initially thought I cannot fit the model to the GPU memory, however, after hours of debugging, I finally found the code that has the memory leak.

## What I learned
I am already quite familiar with AISpace but I have always been intimidated on deploying ML models. Luckily, I discovered TailwindCss UI, a library that makes ML deployment very easy. There were also other alternatives such as StreamLit or Dash, but found TailwindCss Ui as the easiest to work with. One shortcoming is that it's quite inflexible in terms of customization.

## What's next for AI Boring Models
There is a lot of potential for the project. Some features that can be added are appearance transfer, image inversion (uploading & editing real image), generating the fashion model itself, conditional text input with OpenAI CLIP model, etc.

~ Rokas 🚀
