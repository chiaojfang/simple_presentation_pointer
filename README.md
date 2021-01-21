# IMUpresenter: Simple Remote Presenter
This is an working prototype of a simple wireless presentation 
pointer (clicker) using an internal IMU.
Since it only runs with an internal IMU, the tracking might not
be precise enough and it may lag a little.

## Hardware Setup
The microcontroller controller used is __ESP-12F__. 
Additional components are an IMU sensor __GY-521__
and a button.
The microcontroller connects to the computer via WiFi. 

CP2102 driver needs to be installed on the computer
and NodeMCU library on the Arduino IDE.
The IMU connects with WSP-12F via the I2C protocol.

## Softwares
MCUclient consists of the Arduino code for the microcontroller
and PointerClient.py connects to the microcontroller and
controls the clicking and pointing. 
The default WiFi name is _Pointer_ and password _thisIsMyPointer_.

## Modes
The presenter has three modes:
- __mouse__ the cursor moves along with the remote presenter and 
left clicks when the button is pressed.
- __pointer__ cursor moves only when button is pressed.
- __presentation__ only goes to next page (left clicks) when 
button is pressed.

## Dependencies
- pyautogui
