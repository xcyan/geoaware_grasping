# Learning Grasping Interactions with Geometry-aware Representations
### Authors
Xinchen Yan<sup>*</sup>, Mohi Khansari<sup>+</sup>, Yunfei Bai<sup>+</sup>, Jasmine Hsu<sup>#</sup>, Arkanath Pathak<sup>x</sup>,
Arbhinav Gupta<sup>&</sup>, James Davidson<sup>#</sup>, Honglak Lee<sup>#</sup>

<sup>#</sup>Google Brain

<sup>+</sup>X Inc

<sup>&</sup>Google Research

<sup>x</sup>Google

<sup>*</sup>University of Michigan

### Abstract

Learning to interact with objects in the environment is a fundamental AI problem involving perception, motion planning, and control. 
However, learning representations of such interactions is very challenging due to a high dimensional state space, difficulty in collecting large-scale data, and many variations of an object's visual appearance (i.e. geometry, material, texture, and illumination).
We argue that knowledge of 3D geometry is at the heart of grasping interactions and propose the notion of a geometry-aware learning agent. 
Our key idea is constraining and regularizing interaction learning through 3D geometry prediction.
Specifically, we formulate the learning process of a geometry-aware agent as a two-step procedure: 
First, the agent learns to construct its geometry-aware representation of the scene from 2D sensory input via generative 3D shape modeling.
Finally, it learns to predict grasping outcome with its built-in geometry-aware representation. 
The geometry-aware representation plays a key role in relating geometry and interaction via a novel learning-free depth projection layer. 
Our contributions are threefold: 
(1) we build a grasping dataset from demonstrations in virtual reality (VR) with rich sensory and interaction annotations; 
(2) we demonstrate that the learned geometry-aware representation results in a more robust grasping outcome prediction compared to a baseline model; and 
(3) we demonstrate the benefits of the learned geometry-aware representation in grasping planning.

### Video Demo
Please check a short video demo 
[linkname](https://youtubevideourl)

You can use the [editor on GitHub](https://github.com/xcyan/geoaware_grasping/edit/master/README.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/xcyan/geoaware_grasping/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
