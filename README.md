RoAH IPCam
==========

This repository contains a ROS package that can be used to receive
images from the camera that will be used in the RoCKIn@Home competition.
This is just the simplest way of communicating with the camera,
teams are welcome to develop and share more elaborate methods.

This is designed to acquire data from an ipcamera and publish it on
ROS. This node acts as a simple webgrabber that publishes the
acquired images on a topic.


## Dependencies

You need to use ROS, probably any recent version with catkin will do.
Follow the instructions at http://wiki.ros.org/ROS/Installation/ .

This was tested with Ubuntu 12.04.5 LTS (Precise Pangolin) and
14.04.1 LTS (Trusty Tahr).


## Compiling

Compile as a normal ROS package in your Catkin workspace.


## Running

The roah_ipcam node only publishes the compressed transport of the
image topic. You need to use `image_transport/republish` to publish
the raw transport that can be used directly. Check the launch files
for examples.

To simply test the node, you can use:
```bash
roslaunch roah_ipcam roah_ipcam_view.launch --screen
```
