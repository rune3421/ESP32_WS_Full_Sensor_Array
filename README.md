# ESP32_WS_Full_Sensor_Array
All of the sensors are now attached to the Biomedical Wireless Baby Monitor. 

Hello and welcome to another edition of Karl Fiddles Around™. 

Last time we got the client side hooked up with an SD card to log the data coming in from the server, and although there was a sizeable degradation in the data, it wasn’t yet enough to completely freeze the system, so we’re going to forge ahead and try to wire the last component; an analog pH sensor. 

This wiring will complete the server’s workload, so getting to this point will be a proof of concept, that the ESP32 chipset is able to handle all the components. Once we get the pH wired and working, the next step will be to optimize the code for the needed sample rate of each sensor, and calibrate the sensors for the cleanest possible data. 

So here we go! First step is to wire the pH sensor, and then run a sample Analog Read/Serial print to see if just having the other wires hooked up will be a problem. 

So far, so good! The sensor seems a bit finicky when it’s not in contact with its intended analyte, and it’s a proof of concept prototype only so there’s some refining of the hardware to do too, but that’s a task for another project. It’s reading reasonable values for now, which is the main goal. 

So now it’s time to add this analog signal into the code for the server to see if it plays well with the other sensors. 

And it works!

Analog readings, it turns out, adds very little load to the system. With that, it’s time to document the full circuit schematic for the server and the client, and document the code. So even though this was a relatively short exercise as far as adding in components and troubleshooting, this is a milestone in the development cycle of this circuit. We have passed the wiring integration and bare-bones function stage of the process, and now it’s time for debugging and optimizing. Woohoo!

Here’s the wiring diagrams:

Server/Sensor Circuit:

Client/Display Circuit:

And code is in the attached files. 
