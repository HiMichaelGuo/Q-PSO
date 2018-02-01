## Fast Feature-Less Quaternion-based Particle Swarm Optimization for Object Pose Estimation From RGB-D Images


The code in this repository is related to the original paper:
http://www.bmva.org/bmvc/2016/papers/paper113/
and includes some improvements.

This is the GPU implementation, which includes object segmentation from https://arxiv.org/abs/1605.03746

- - - -
Hardware:

Requires a CUDA enabled GPU (with support for CUDA 7.0 or greater)

Sofware:

* OpenCV
* gcc with support for c++11

Compile:

`make`

Run (estimate the pose of the first 15 detected object clusters):

`for N in {0..15};
do;
./main object_model rgb_image depth_image $N;
done`

Where rgb_image and depth_image are 640x480 png images.

For tuning the object segmentation parameters for different datasets, it could be useful to use the code from https://github.com/morpheus1820/graph-canny-segm

