cob_robots
===========

## ROS Distro Support

|         | Indigo | Jade | Kinetic |
|:-------:|:------:|:----:|:-------:|
| Branch  | [`indigo_dev`](https://github.com/ipa320/cob_robots/tree/indigo_dev) | [`indigo_dev`](https://github.com/ipa320/cob_robots/tree/indigo_dev) | [`indigo_dev`](https://github.com/ipa320/cob_robots/tree/indigo_dev) |
| Status  |  supported | not supported |  supported |
| Version | [version](http://repositories.ros.org/status_page/ros_indigo_default.html?q=cob_robots) | [version](http://repositories.ros.org/status_page/ros_jade_default.html?q=cob_robots) | [version](http://repositories.ros.org/status_page/ros_kinetic_default.html?q=cob_robots) |

## Travis - Continuous Integration

Status: [![Build Status](https://travis-ci.org/ipa320/cob_robots.svg?branch=indigo_dev)](https://travis-ci.org/ipa320/cob_robots)

## ROS Buildfarm

|         | Indigo Source | Indigo Debian | Jade Source | Jade Debian |  Kinetic Source  |  Kinetic Debian |
|:-------:|:-------------------:|:-------------------:|:-------------------:|:-------------------:|:-------------------:|:-------------------:|
| cob_robots | [![not released](http://build.ros.org/buildStatus/icon?job=Isrc_uT__cob_robots__ubuntu_trusty__source)](http://build.ros.org/view/Isrc_uT/job/Isrc_uT__cob_robots__ubuntu_trusty__source/) | [![not released](http://build.ros.org/buildStatus/icon?job=Ibin_uT64__cob_robots__ubuntu_trusty_amd64__binary)](http://build.ros.org/view/Ibin_uT64/job/Ibin_uT64__cob_robots__ubuntu_trusty_amd64__binary/) | [![not released](http://build.ros.org/buildStatus/icon?job=Jsrc_uT__cob_robots__ubuntu_trusty__source)](http://build.ros.org/view/Jsrc_uT/job/Jsrc_uT__cob_robots__ubuntu_trusty__source/) | [![not released](http://build.ros.org/buildStatus/icon?job=Jbin_uT64__cob_robots__ubuntu_trusty_amd64__binary)](http://build.ros.org/view/Jbin_uT64/job/Jbin_uT64__cob_robots__ubuntu_trusty_amd64__binary/) | [![not released](http://build.ros.org/buildStatus/icon?job=Ksrc_uX__cob_robots__ubuntu_xenial__source)](http://build.ros.org/view/Ksrc_uX/job/Ksrc_uX__cob_robots__ubuntu_xenial__source/) | [![not released](http://build.ros.org/buildStatus/icon?job=Kbin_uX64__cob_robots__ubuntu_xenial_amd64__binary)](http://build.ros.org/view/Kbin_uX64/job/Kbin_uX64__cob_robots__ubuntu_xenial_amd64__binary/) |

## Kinova arm tesing
1. test with MoveIt!:
 
```
roslaunch cob_moveit_bringup demo.launch robot:=cob4-10
```

2. Adding kitchen as collision object:
```
roslaunch ipa_planning_scene_creator planning_scene_creator.launch robot:=cob4-10 base_link:=base_link tip_link:=j2n4s300_end_effector
rosrun ipa_planning_scene_creator test_planning_scene.py --base_link base_link --tip_link j2n4s300_end_effector 
```

3. Set position from rviz if it is wrong and save as publish planning scene
