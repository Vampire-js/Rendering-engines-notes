# Rendering-engines-notes


Topics touched so far:
1. Voxel based GI
   - Shadow mapping
   - Creation of different passes
   - limitations
2. SDF GI


## Shadow mapping
General idea: create a depth buffer from light space, and use it to apply shadows

- Hence transformations are as follows:
- ```P_light = Projection x (light rotation) x (light translation) x world```

Depth buffer can be found using ray marching, followed by normalization of distance from sdf, and applying the color ```vec3(dist) ``` to that pixel.

