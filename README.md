# OpenGL-Texture-Mapping
Texture mapping a face into a 3d head

# Shaders
The basic unit of computer graphics is the **vertex**. A vertex is just a point in 3D; rather than (x,y) coordinates, it has (x,y,z). We use vertices to construct triangles, which are made of 3 vertices.

Importantly, triangles have normals (as do vertices). The normal is the line that is perpendicular to all 3 of the triangle's edges. These normals are used by OpenGL to do many calculations. Almost all models (also called **meshes**) in OpenGL are made from triangles. 

A shader is a program that we'll use on the GPU. The shader is compiled and returns an ID. We have two types of shaders: the **vertex** shader and the **fragment** shader. The vertex shader changes the position of a vertex (translation, rotation, etc.), and can also determine the color. The fragment shader, also sometimes called the **pixel** shader, determines the colors of the pixels in-between vertices using lighting, materials, normals, etc.

# UV Coordinates
Objects in OpenGL are made of triangles. If we want to put an image onto an object, we'll need to tell OpenGL which part of of the image goes in each triangle. UV coordinates are how we do that.

Each vertex has a position, but it also has UV coordinates, specified as (u,v). Think of these as texture coordinates; it's what part of the texture corresponds to that vertex. These UV coordinates range from 0 to 1, and have an x-y axis since the texture itself is 2D. (0,0) corresponds to the lower left of the texture image, and (1,1) corresponds to the upper right of an image. We specify 3 texture coordinate points, each corresponding to a vertex of the triangle. 

There's many different ways texture sampling can be done. Thus, we need to tell OpenGL exactly which method we want to use.
