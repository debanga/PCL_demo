# PCL_demo
A simple working example of Point Cloud Library in Ubuntu 16.04

## Requirements
- Install PCL using this blog:

http://pointclouds.org/documentation/tutorials/compiling_pcl_posix.php

- Explanation to the sample code is available here:

http://www.pointclouds.org/documentation/tutorials/writing_pcd.php#writing-pcd


## References

- Using PCL with existing projects with Makefile

https://stackoverflow.com/questions/32485771/adding-pcl-point-cloud-library-to-existing-project-with-makefiles

```
PCL_INCLUDE = /usr/local/include/pcl-1.9
EIGEN_INCLUDE = /usr/include/eigen3
VTK_INCLUDE = /usr/include/vtk-5.10
OTHERS_INCLUDE = /usr/include

INC_DIRS += $(PCL_INCLUDE)
INC_DIRS += $(EIGEN_INCLUDE)
INC_DIRS += $(VTK_INCLUDE)
INC_DIRS += $(OTHERS_INCLUDE)
```
```
LDFLAGS += -L/usr/local/lib -rdynamic /usr/local/lib/libpcl_segmentation.so /usr/local/lib/libpcl_surface.so /usr/local/lib/libpcl_keypoints.so /usr/local/lib/libpcl_tracking.so /usr/local/lib/libpcl_recognition.so /usr/local/lib/libpcl_stereo.so -lboost_system -lboost_filesystem -lboost_thread -lboost_date_time -lboost_iostreams -lboost_serialization -lboost_chrono -lboost_atomic -lboost_regex -lpthread -lflann_cpp /usr/local/lib/libpcl_ml.so /usr/local/lib/libpcl_registration.so /usr/local/lib/libpcl_features.so /usr/local/lib/libpcl_filters.so /usr/local/lib/libpcl_sample_consensus.so /usr/local/lib/libpcl_search.so /usr/local/lib/libpcl_kdtree.so /usr/lib/libvtkGenericFiltering.so.5.10.1 /usr/lib/libvtkGeovis.so.5.10.1 /usr/lib/libvtkCharts.so.5.10.1 /usr/lib/libvtkViews.so.5.10.1 /usr/lib/libvtkInfovis.so.5.10.1 /usr/lib/libvtkWidgets.so.5.10.1 /usr/lib/libvtkVolumeRendering.so.5.10.1 /usr/lib/libvtkHybrid.so.5.10.1 /usr/lib/libvtkParallel.so.5.10.1 /usr/lib/libvtkRendering.so.5.10.1 /usr/lib/libvtkImaging.so.5.10.1 /usr/lib/libvtkGraphics.so.5.10.1 /usr/lib/libvtkIO.so.5.10.1 /usr/lib/libvtkFiltering.so.5.10.1 /usr/lib/libvtkCommon.so.5.10.1 -lm /usr/lib/libvtksys.so.5.10.1 -ldl /usr/local/lib/libpcl_io.so /usr/local/lib/libpcl_octree.so /usr/local/lib/libpcl_common.so -Wl,-rpath,/usr/local/lib:/usr/lib/openmpi/lib -Wl,-rpath-link,/usr/lib/openmpi/lib
```




