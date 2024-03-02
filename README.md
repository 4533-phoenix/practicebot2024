# Practice Bot 2024

todo: 
-rotate control aka right stick X seems to rotate at only one speed, not proportional, is it gyro related or ?
-lower max drive speeds (I already lowered Ramp rates 
-note ramp rates are in deploy but max speed might be in constants?


Based on Yagsl 2024 example code 

So this is experiment to see if YAGSL is good starting point 

Using 
* Neos
* Cancoders
* SDS Mk4 with L2 ratio
* navx_spi 


added swerve/practicebot json config files to give base characterization of the robot

**Controls:**

Robot has 3 possible teleop modes of control that affect mainly how the Right stick affects robot facing angle.

In the driveFieldOrientedDirectAngle mode, Right stick controls the desired angle NOT angular rotation. (default) See AbsoluteDrive.java.

In the driveFieldOrientedAnglularVelocity mode, Right stick controls the angular velocity of the robot. See AbsoluteFieldDrive.java.

Third mode is like the 2nd above but also maps buttons ABCD to point robot in those directions instantly.

See RobotContainer.java 

Xbox or Logitech F310 

Left stick controls Field Translation in Absolute Field Centric mode

Right stick controls the desired angle NOT angular rotation

Buttons

*  Y lookAway      Face the robot towards the opposing alliance's wall in the same direction the driver is

*  A lookTowards   Face the robot towards the driver

*  X lookLeft      Face the robot left

*  B lookRight     Face the robot right

*  Back button does a gyro reset

*  Start button might be coded later to lock wheels (also robot disable does same for 10 secs)
  
 
MAX Speed is now set in Constants , default was Units.feetToMeters(14.5), but changed to 6 or 8 to slow it down for testing.



