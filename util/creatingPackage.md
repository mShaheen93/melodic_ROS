 Workspace name  **wallE_ws**


## create Workspace
    mkdir wallE_ws
    cd wallE_ws
    mkdir src
    cd src
    catkin_init_workspace


## make Workspace
    cd ..
    catkin_make

### output
    build
    devel
    src


## create Package  
    cd src
    catkin_create_pkg robot_tutorial rospy roscpp std_msgs

### output
    robot_tutorial
        include
        src
        camkelist
        package.xml


After Adding new Package (robot_tutorial)
We need to build the whole workspace


    cd ..
    ctkin_make


Find Package
    rospack find robot_tutorial

To make the package visible
    change dir to devel & run setup.bash


To go to package location use **roscd**
    roscd robot_tutorial

To list package use **rosls**
    rosls robot_tutorial

To see logs of package use **roslog**
    roscd log

Open Package xml under package dir



## XML Package
    Format
    version
    License
    Author email tag
    build depend
    build export depend
    exec depend
