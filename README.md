# IVCam-Install

Multiple instances of iVCam
You can transfer videos from multiple phones to different iVCam instances on the same PC.
To do this, you need to install multiple instances (drivers) on your PC first.

Install
First, please make sure that you’ve already installed the latest verion of iVCam.
Then find the driver_install.bat file in the iVCam installation folder (for example: C:\Program Files\e2eSoft\iVCam) and run it, adding an iVCam driver each time you run it.

If the execution of this file failed with some errors, you can also enter the iVCam installation folder at a Command Prompt running with administrator privileges, and run the following command to install the driver:

`devcon install driver\iVCam.inf iVCamDevice`

Run it twice and you will have 3 iVCam drivers (including the default one). You can see them in system Device Manager application.

If there’s only one instance, the camera name will be “e2eSoft iVCam“, the microphone name will be “Microphone (e2eSoft iVCam)” , and you can only run one iVCam application;

If there’re more, the camera name will be “e2eSoft iVCam #1“, “e2eSoft iVCam #2“, etc., and the microphone name will be “Microphone #1 (e2eSoft iVCam)“, “Microphone #2 (e2eSoft iVCam)“, etc., You can run more instances of the iVCam application.


Uninstall
To uninstall an iVCam driver (instance), locate the iVCam device in the “Imaging devices” group in system Device Manager and right click on it to uninstall the driver, be careful not to uninstall all of them.


Run
Run our app on the phone, it will detect these running instances, select which one to use and the app will transfer the video to the selected instance.


NOTE:
For Android phones, if it connects automatically and you cannot select instances, tap the  button to close the video and return to the main view, wait a while for the instances to be detected, and then you can tap the play button  to choose which instance to connect to.
Please make sure that Bonjour service is running (you can see this in system Task Manager > Services), reinstall iVCam if there’s no Bonjour service installed.
If for some reason you cannot run the Bonjour service (iVCam will use UDP to detect PC client), or you want to connect via USB, please run an iVCam instance and connect it with a phone, then run another instance and connect with another phone, and so on. Don’t run the new instance if the old one is not connected with a phone.
Selecting “Hardware decoding” in the PC client software (if supported by your PC) can greatly reduce CPU usage to support the running of more instances.
