# Learning about Arduino

## Setup IDE

We can use **Arduino Desktop IDE** or **Visual Studio (VS) Code** with **Arduino** extension. 
VS Code Arduino extension still requireds Arduino Desktop IDE installed. 

### Installation Steps

Download Arduino Desktop IDE from https://www.arduino.cc/en/main/software

Download VS Code from https://code.visualstudio.com/download

In VS Code, from the extensions, search for Ardunio and install it. 

### Configure VS Code 

Open VS Command Palette (View>Command Palette) OR, **CTRL + Shift + P**, then

- Select the Board
  - Find **Arduino:Change Board Type**, and the board you have. 
- Set Baud Rade 
  - Find **Arduino:Baud Rate**, and set the value, such as 9600
- Set Serial Port
  - Be sure that the Arduino device is connected to your computer in order to set the serial port
  - Find **Arduino:Select Serial Port**, and select the port 

## Initialize and Configure Arduino Project 

Open VS Command Palette, **CTRL + Shift + P**, then

- Initialize Arduino 
  - Select **Arduino:Initialize**, this will generate default configurations:
    - arduino.json
      - In this file, you can define/change scetch name, serial port number, etc.. 
    - c_cpp.properties.json
      - in this file you can have C++ related configuration, such as libaries paths, intellisense configuration. 

- Selecting output folder for caching:
  - Open ./vscode/arduino.json, and add the following code:
    ```json
    "output": "build"
    ```

- Fixing intellisense error for Serial, and some other methods 
  - see this for more details: https://github.com/microsoft/vscode-arduino/issues/808
  - Open .vscode/c_cpp_properties.json, and add the following line:
    ```json
    "defines": ["USBCON"]
    ```
    If you already have a value under "defines", then just add "USBCON".



## Hello world 

After installing the applications, open VS Code, create a file named main.ino






## 