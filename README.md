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
we develop a two-stage learning framework that performs 3D shape prediction and grasping outcome prediction with geometry-aware representation. Being able to generate 3D object shapes (e.g., volumetric representation) from any scene given 2D sensory input is a very important feature of our geometry-aware agent. More specifically, in our formulation, the geometry-aware representation is (1) an occupancy grid representation of the scene centered at camera target in the world frame and (2) invariant to camera viewpoint and distance.

### Model Architecture
[<img src="https://umich.box.com/shared/static/bhs5v3ss7rpl146d73hjjgdkes1mx6y9.png">](https://umich.box.com/shared/static/bhs5v3ss7rpl146d73hjjgdkes1mx6y9.png)
Our geometry-aware encoder-decoder network has two components: a 3D shape generation network (generative) and a grasping outcome prediction network (predictive).
The shape generation network has a 2D convolutional shape encoder and a 3D deconvolutional shape decoder followed by a global projection layer.
Our shape encoder network takes RGBD images of resolution 128 x 128 and
corresponding 4-by-4 camera view matrices as input; the network and outputs identity units as an intermediate representation.
Our shape decoder is a 3D deconvolutional neural network 
that outputs voxels at a resolution of 32 x 32 x 32.
We implemented the projection layer (with camera view and projection matrix) that transforms the voxels back 
into foreground object silhouettes and depth maps at an input resolution (128 x 128).

The outcome prediction network has a 2D convolutional state encoder and a fully connected outcome predictor with an additional local shape projection layer. 
Our state encoder takes RGBD images (pre-grasp scene) of resolution 128 x 128 and corresponding actions (position and orientation of the gripper end-effector) and outputs state unit as intermediate representation.
Our outcome predictor takes both current state (e.g., pre-grasp scene and action) and shape features (e.g., global shape from identity units and the local surface from the local shape projection layer) into consideration.
Note that the local dense sampling transforms the surface around the gripper fingers into a foreground silhouette and a depth map at resolution 48 x 48.

### Video Demo
A short video demo regarding details about data collection and experimental results: [link](https://youtu.be/ii7CuDZlxZs)
