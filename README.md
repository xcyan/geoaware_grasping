# Learning Grasping Interaction with 3D Geometry-aware Representations
### Authors
Xinchen Yan<sup>*</sup>, Mohi Khansari<sup>+</sup>, Yunfei Bai<sup>+</sup>, Jasmine Hsu<sup>#</sup>, Arkanath Pathak<sup>x</sup>,
Abhinav Gupta<sup>&</sup>, James Davidson<sup>#</sup>, Honglak Lee<sup>#</sup>

#### Affliation
<sup>#</sup>Google Brain, 
<sup>+</sup>X Inc, 
<sup>&</sup>Google Research, 
<sup>x</sup>Google, 
<sup>*</sup>University of Michigan

### Resources
[[PDF]](https://arxiv.org/pdf/1708.07303.pdf) [[Video]](https://youtu.be/ii7CuDZlxZs)

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
(1) we build a grasping dataset from demonstrations in virtual reality (VR<sup>*</sup>) with rich sensory and interaction annotations; 
(2) we demonstrate that the learned geometry-aware representation results in a more robust grasping outcome prediction compared to a baseline model; and 
(3) we demonstrate the benefits of the learned geometry-aware representation in grasping planning.

<sup>*</sup> We use pybullet for VR and simulation ([http://pybullet.org](http://pybullet.org)).

### Approach
[<img src="https://umich.box.com/shared/static/qendrl1zuaptuhqmewv2x6senlpt541w.png">](https://umich.box.com/shared/static/qendrl1zuaptuhqmewv2x6senlpt541w.png)
We develop a two-stage learning framework that performs 3D shape prediction and grasping outcome prediction with geometry-aware representation. Being able to generate 3D object shapes (e.g., volumetric representation) from any scene given 2D sensory input is a very important feature of our geometry-aware agent. More specifically, in our formulation, the geometry-aware representation is (1) an occupancy grid representation of the scene centered at camera target in the world frame and (2) invariant to camera viewpoint and distance.

### Model Architecture
[<img src="https://umich.box.com/shared/static/bhs5v3ss7rpl146d73hjjgdkes1mx6y9.png">](https://umich.box.com/shared/static/bhs5v3ss7rpl146d73hjjgdkes1mx6y9.png)
Our geometry-aware encoder-decoder network has two components: a 3D shape generation network (generative) and a grasping outcome prediction network (predictive).
The shape generation network has a 2D convolutional shape encoder and a 3D deconvolutional shape decoder followed by a global projection layer.
The outcome prediction network has a 2D convolutional state encoder and a fully connected outcome predictor with an additional local shape projection layer. 

### Experiments
A short video demo on experimental results (please click on the figure below): 
[<img src="https://umich.box.com/shared/static/wabu23cu6kj04qj8ofo6h5rqy7p4detb.png">](https://youtu.be/ii7CuDZlxZs)

### Acknowledement
We thank [Brain Research](https://research.google.com/teams/brain/machine-learning/), [Brain Robotics](https://research.google.com/teams/brain/robotics/) and [X](https://x.company/) colleagues for their help to this project!
