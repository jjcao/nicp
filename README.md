NICP (Normal Iterative Closest Point)
====

NICP is a novel on-line method to recursively align point clouds. This method 
exploits the 3D structure to determine the data association between the two 
clouds taking into account each point and its local features of the surface: 
normals and curvature.
This method adopt a line of sight criterion to find the corresponding points between 
the two clouds to register. This, togheter with the efficient algorithms and 
data structures used by NICP, increase the speed of the method allowing 
real-time computation.
NICP solves the alignment problem by casting a least squares formulation that 
minimizes an error metric depending on both the point coordinates and the 
associated normal. This renders the algorithm more robust and accurate, thus 
computing better transformation. 

System Requirements
----

### Minimum

- Eigen3 >= 3.2.0
- OpenCV >= 2.4.8 

### Complete

- OpenGL 
- Qt4 
- QGLViewer 

Building on Linux
----

- mkdir build
- cd build
- cmake ..
- make

Branches
----

- master: current development branch
- nicp_evaluation: experimental evaluation branch


Examples
----

Once you compiled the code you will have the following exmaple binaries:
- pwn_simple_aligner is a binary that, given a set of depth images and a .txt file containing the list of depth images to align, perform the point cloud registrations
- pwn_aligner same as pwn_simple_aligner, but it uses an incremental version of the algorithm 
- pwn_aligner_gui is a simple GUI for point cloud alignment, several parameters of the algorithm can be modified with GUI buttons
- pwn_cloud_prop_viewer simple GUI to see basic properties of a depth image / point cloud
- pwn_simple_viewer is a GUI that given a folder allows to visualize all the point clouds, saved in .pwn format, in the folder

N.B.
----

Temporarily, the NICP library will have still his old name PWN. As soon as possible all the pwn prefixes will be substituted with nicp.
