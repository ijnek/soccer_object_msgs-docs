.. _vision_msgs:

Soccer Vision Msg files
#######################

Ball
****

.. code-block:: cpp

    std_msgs/Header header
    geometry_msgs/Point center

Goalpost
********

``observed_top`` should be set to **true**, if ``point`` is being populated with a point at the top of the goalpost. This is how
goalposts are reported in SimSpark.

``observed_top`` should be set to **false**, if ``point`` is being poulated with a point at the bottom of the goalpost.

Reporting a goalpost with a point other than the top or bottom, is not supported with this msg type. 

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

Flag
****

Flags refer to the corner flags on the field. **base** is the coordinate of the base of the flag's pole.

.. code-block:: cpp

    std_msgs/Header header
    geometry_msgs/Point base

FlagArray
*********

.. code-block:: cpp

    Flag[] flags