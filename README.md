# cs7785-lab3-solved
**TO GET THIS SOLUTION VISIT:** [CS7785 Lab3 Solved](https://www.ankitcodinghub.com/product/cs7785-cs-me-ece-ae-bme7785-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;115150&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;0&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;0&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;0\/5 - (0 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CS7785 Lab3 Solved&quot;,&quot;width&quot;:&quot;0&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 0px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            <span class="kksr-muted">Rate this product</span>
    </div>
    </div>
1 Overview

As you did with lab 2, you should run all les on-board the robot. To move folders from your computer to the robot, use GIT or the scp (secure copy) command. For example,

scp -r &lt;Directory on your cpu to copy&gt; burger@&lt;ip-of-burger&gt;:&lt;Directory to copy to on robot&gt;

2 Lab Instructions

detect_object: This node should be similar to the find_object you created in last lab. It should subscribe to the raspberry pi camera node and publish the location of the of the object you’re tracking.

Note: unlike previous labs, you will now be coordinating your camera with your LIDAR so they will have to agree on reference frames and units. This means you should convert your pixel values to degrees or radians and know the relation between the reference frame of your camera and your LIDAR.

get_object_range: This node should subscribe to receive the location of the object published from your find_object node and publish the angular position and distance of the object using some combination of the LIDAR data and camera data. To get the LIDAR data, this node should also subscribe to the scan topic.

LIDARS produce a lot of data and are one of the more complicated sensors to use. For more information on the LIDAR used on the turtlebot3 please look at:

http://emanual.robotis.com/docs/en/platform/turtlebot3/appendix_lds_01/ You can also echo the topic to view the data that is being produced.

chase_object: This node should subscribe to the data being published by get_object_range. Based on this data you should create two PID (or some variant) controllers to follow your tracked object at a desired distance (meaning the robot drives forward and backwards if needed). One controller should act on the angular error to make the robot face the object while the other acts on the linear error to make the robot maintain a distance from the object. This node should publish the velocity commands for the robot to follow in the same manner you did in lab 2.

Note there are PID controllers already acting on the motors of the turtlebot3. If this was a custom robot, or you did not like the motor controllers of the robot, you would have to design a PID controller for the motors of the robot as well that would have a settling time much faster than your high level controller!

3 Questions

These questions must be answered in a writeup submitted with your code. This does not have to be a formal lab report, just answer the questions directly. Include supplemental material where you think it would help. These questions should also be considered while developing your code.

1. What is the sampling time of your system(hint: how fast can you get sensor data)? Why does sampling time matter, even with a subscriber based controller?

2. What variant of PID control did you use? Why?

3. If you use an integral term, how do you deal with windup? If you use a derivative term how do you deal with noise/fast changes in the object’s location? If you just used a purely proportional control, how does your reject output disturbances (like friction)?

4. What does it mean for this system to be unstable? A helicopter/plane will fall out of the sky if it uses an unstable controller, what does your robot do when your controller is unstable?

5. Describe your algorithm to determine where the object is relative to the robot. Speci cally, how do you use the camera and LIDAR data to produce a desired velocity vector? Include mathematical expressions used and supportive gures where appropriate.

4 Grading

The lab is graded out of 100 points, with the following point distribution:

Consistently determine the location of your object (distance and angle relative to the robot) 20%

Rotate the robot to face the object 20%

Drive the robot to maintain a distance from the object 20%

Robot stops at desired distance and heading of the stationary object within 5 seconds 10%

Question responses 30%

5 Submission

2. Put the names of both lab partners into the header of the python script. Put your python script, your writeup, and any supplimentary les, in a single zip le called Lab3_LastName1_LastName2.zip and upload on Canvas under Assignments Lab 3.

3. Only one of the partners needs to upload code.
