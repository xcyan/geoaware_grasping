# Learning Grasping Interaction with Geometry-aware Representations
### Authors
Xinchen Yan<sup>*</sup>, Mohi Khansari<sup>+</sup>, Yunfei Bai<sup>+</sup>, Jasmine Hsu<sup>#</sup>, Arkanath Pathak<sup>x</sup>,
Arbhinav Gupta<sup>&</sup>, James Davidson<sup>#</sup>, Honglak Lee<sup>#</sup>

#### Affliation
<sup>#</sup>Google Brain, 
<sup>+</sup>X Inc, 
<sup>&</sup>Google Research, 
<sup>x</sup>Google, 
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

### Approach
[<img src="https://umich.box.com/shared/static/bhs5v3ss7rpl146d73hjjgdkes1mx6y9.png">](https://umich.box.com/shared/static/bhs5v3ss7rpl146d73hjjgdkes1mx6y9.png)
### Video Demo
A short video demo regarding details about data collection and experimental results: [link](https://youtu.be/ii7CuDZlxZs)
