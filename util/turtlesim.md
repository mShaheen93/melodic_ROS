# TurtleSim Example 

* In Terminal 1
    
    roscore

* In Terminal 2
to see all **Active** nodes

    rosnode list

* In Terminal 3
run the needed node *turtlesim*
    
    rosrun turtlesim turtlesim_node


* In Terminal 2
to see all **info** for nodes

    rosnode info /turtlesim 

tocheck if node is **Alive**
    rosnode ping turtlesim

to start node with different name (change __name property)
    rosrun turtlesim turtlesim_node __name:=twoDwall