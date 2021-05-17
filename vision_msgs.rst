.. _vision_msgs:

Soccer Vision Msg files
#######################

Goalpost
********

.. code-block:: cpp

    std_msgs/Header header
    bool observed_top
    geometry_msgs/Point point

GoalpostArray
*************

.. code-block:: cpp

    Goalpost[]  posts

FieldLine
*********

.. code-block:: cpp

    std_msgs/Header header
    geometry_msgs/Point start
    geometry_msgs/Point end

FieldLineArray
**************

.. code-block:: cpp

    FieldLine[]  lines


Robot
*****

Data type for robot observation in vision.
Due to how robot observations are sent in SimSpark, this data message uses the "head" point
of the robot.

.. code-block:: cpp

    std_msgs/Header header
    geometry_msgs/Point head
    string team
    int32 id

RobotArray
**********

.. code-block:: cpp

    Robot[]  robots 