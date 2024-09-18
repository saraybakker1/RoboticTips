# Common mistakes when working with the KUKA:
These mistakes might be quite specific for the KUKA set-up that we have in the lab, but some are more general to the KUKA iiwa 14.

## General problems:
**Problem: If it is not possible to run a breaktest-application to reset the system, the joints are too far.**
**Answer 1:** Turn the key on the kuka-pannel, and see if the mode: KRF has appeared. If it has, set the system to this mode, and run the breaktestapplication again.
**Answer 2:** If the robot is not responding anymore and KRF doesn't appear and you did a test with a high velocity where a joint limit is probably exceeded, 
go to the menu (LBR_iiwa7_R8_...), Mastering, do Unmaster and remaster. This will calibrate the joint again. 

## Common problems specific to our set-up:
**Problem: The FRIOverlay500 doesn't show the display "torque"**
**Answer:** The remote PC script is not active.

**Problem: The bringup_local hangs upon sending the command and doesn't say "solver relaxedIk initialized" or prints anything else.**
**Answer:** Your laptop didn't connect to the ethernet, plug in the cable and select "kuka_network" as your network. 

**Problem: The request_joint_position doesn't move the robot (all steps before are managed)**
**Answer:** Restart the local script (on your laptop).

**Problem: The topic of the optitrack is not showing**
**Answer:** Try a different ethernet port on the pc of the optitrack. 


