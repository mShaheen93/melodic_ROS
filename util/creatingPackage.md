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

=====================================

After Adding new Package (robot_tutorial)
We need to build the whole workspace


    cd ..
    catkin_make


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

==============================================

## XML Package
    Format
    version
    License
    Author email tag
    build depend
    build export depend
    exec depend



## cmake vs catkin_make

*Go to workspace dir (wallE_ws)*
    
    mkdir build
    cd build
    
    cmake ../src
    make   
    *This doesn"t create devel dir*

Option1 *We need to use cmake with build options*  
    
    cmake ../src/ -DCMAKE_INSTALL_PREFIX=../install -DCATKIN_DEVL_PREFIX=../devel

Option2 *We need to use catkin_make* 
    
    catkin_make



## Add executable for CMake

    under package add src folder with it"s cmakelist

    change makelist.txt of package & add executable

## Run Package node 
    After sourcing your workspace
    **This is local to the Terminal**
    go to ws dir
    source devel/setup.bash


    now you can run it from anywhere    


    rosrun robot_tutorial walle_hello_node


## Adding CMake Project

You can"t add another CMake Project(with executables) directly
You need to create a node then add the executables (from CmakeList) needed for this node  to the CMakeListst of the node


CHeck this example
    https://cliutils.gitlab.io/modern-cmake/chapters/basics/structure.html
