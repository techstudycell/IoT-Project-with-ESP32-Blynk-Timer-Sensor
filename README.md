# IoT-Project-with-ESP32-Blynk-Timer-Sensor
Make IoT-based Home Automation using ESP32 Google Assistant Blynk with timer, sensor, and IR remote control relay with real-time feedback.

## Tutorial Video on IoT Project using ESP32 & Blynk

Video Link: https://youtu.be/VNeT5QgH-IM

In the tutorial video, I have shown all the steps to make this Blynk home automation system.

### This Blynk ESP32 control smart relay has the following features:

1. Control home appliances with WiFi (Blynk IoT App).
2. Control home appliances with Google Assistant.
3. Control home appliances with DHT11 Sensor and Timer.
4. Control home appliances with IR remote.
5. Control home appliances with manual switches or push buttons.
6. Monitor real-time room temperature in the Blynk IoT App
7. Monitor real-time feedback in the Blynk IoT App.
8. Control appliances without WiFi.

## Required components for the ESP32 Project

So, you can easily make this home automation project at home just by using an ESP32 and relay module. Or you can also use a custom-designed PCB for this project.

1. ESP32 DevKIT V1
2. 4-channel 5V SPDT Relay Module
3. DHT11 Sensor
4. TSOP1838 IR Receiver (with metallic case)
5. Switches or Pushbuttons
6. Any IR Remote

## Circuit Diagram of the ESP32 IoT Project

The circuit is very simple, I have used the GPIO pins D23, D22, D21 & D19 to control the 4 relays.

And the GPIO pins D13, D12, D14 & D27 are connected with switches to control the 4 relays manually.

I used the INPUT_PULLUP function in Arduino IDE instead of the pull-up resistors.

IR remote receiver (TSOP1838) connected with D35. And the DHT11 sensor is connected with RX2.

I have used a 5V mobile charger to supply the smart relay module.

Please take proper safety precautions while working with high voltage.

## Blynk & Google Assistant Control Relay Using ESP32

If the ESP32 is connected with WiFi, then you can control the home appliances from Blynk IoT App.

You also use multiple smartphones to control the appliances with Blynk App. For that, you have to log in same Blynk account from all the smartphones.

In this way, all smartphones will be in the sink to the Blynk server. You can control, and monitor the real-time status of the relays, room temperature & humidity from anywhere in the world in the Blynk IoT App.

You can also ask Google Assistant to turn on and off the appliances.

## Sensor & Timer Control Relay Using ESP32

In this IoT project, you can also control the relays with sensors and Timer using Blynk Automation.

Here, I have controlled the 3rd relay with temperature and the 4th relay with the predefined time schedule.

## IR Remote & Manual Switch Control Relay Using ESP32

You can always control the relays from the IR remote or switches. For this project, you can use any IR remote.

You can monitor the real-time feedback in the Blynk IoT App.

I have explained how to get the IR codes (HEX codes) from any remote in the following steps.

Please refer to the circuit diagram to connect the pushbuttons or switches.

## Design the PCB for This Smart Home System

To make the circuit compact and give a professional look, I designed the PCB after testing all the features of the smart relay module.

You can download the PCB Gerber, BOM, and "pick and place" files of this ESP32 control relay PCB from the following link:

GitHub link to Download PCB Gerber File:
https://github.com/techstudycell/IoT-Project-with-ESP32-Blynk-Timer-Sensor/tree/main/PCB_Gerber

For this project, I have the JLC SMT Service while ordering the PCB.

## Why you should use JLC SMT Service?

On JLCPCB's one-stop online platform, customers enjoy low-cost & high-quality & fast SMT service at an $8.00 setup fee($0.0017 per joint).

$27 New User coupon & $24 SMT coupons every month.

Visit https://jlcpcb.com/RAB

JLCPCB SMT Parts Library 200k+ in-stock components (689 Basic components and 200k+ Extended components)

Parts Pre-Order service https://support.jlcpcb.com/article/164-what-is-jlcpcb-parts-pre-order-service

Build a Personal library Inventory, save parts for now or the future

Assembly will support 10M+ parts from Digikey, mouser.

## Steps to Order the PCB Assembly from JLCPCB
1. Visit https://jlcpcb.com/RAB and Sign in / Sign up.
2. Click on the QUOTE NOW button.
3. Click on the "Add your Gerber file" button. Then browse and select the Gerber file you have downloaded.
4. Set the required parameter like Quantity, PCB masking color, etc.
5. Select the Assemble side and SMT Quantity.
6. Now upload the BOM and PickAndPlace files.
7. Now confirm all the components which you want to be soldered by SMT services.
8. Click on SAVE TO CART button.
9. Type the Shipping Address.
10. Select the Shipping Method suitable for you.
11. Submit the order and proceed with the payment.

You can also track your order from the JLCPCB.
My PCBs took 3 days to get manufactured and arrived within a week using the DHL delivery option.
PCBs were well packed and the quality was really good at this affordable price.

##Create Blynk Cloud FREE Account & Blynk Template

For this smart house project, I have used the Blynk IoT Cloud Free plan.

Click on the following link to create a Blynk Cloud account.

https://blynk.cloud/dashboard/register

1. Enter your email ID, then click on "Sign Up".
2. You will receive a verification email.
3. Click on Create Password in the email, Then set the password, and click on Next.
4. Enter your first name, and click on Done.

After that Blynk cloud dashboard will open.
Create a New Template in Blynk Cloud

First, you have to create a template in the Blynk cloud.

1. Click on New Template.
2. Enter a template name, select the hardware as ESP32, and the connection type will be WiFi.
3. Then click on DONE.

You will get the BLYNK_TEMPLATE_ID and BLYNK_DEVICE_NAME after creating the temple.

## Create a Datastream in Blynk Cloud
After that, you have to create Datastreams. Here I will control 4 relays, so I have to create 4 Datastreams.

1. Go to the Datastreams tab.
2. Click on New Datastream and select Virtual Pin.
3. Enter a name, select the virtual pin V1, and the datatype will be Integer.
4. Then click on Create.
In a similar way, create 4 datastreams with virtual pin V1 to V4. And 1 datastream (V5) to turn off all the relays.

And for the Temperature and humidity, I have used V6, & V7 (Please refer to the picture or tutorial video).

## Define Automation in Blynk Cloud

After that go to the Automation tab and define which Datastreams will be available in Automation actions and conditions (Please refer to picture or tutorial video).

Only Virtual Pin, Enumerable, and Location Datastreams are supported.

## Set Up Blynk Cloud Web Dashboard

Now go to the Web Dashboard tab.

Drag and drop 4 Switch widgets and 2 Level widgets.

Go to the settings of each widget, and select a Datastream.

Please refer to the tutorial video for more details.

Then click on Save to save the template.

## Add Device Using Template in Blynk IoT

Steps to add a device in the Blynk IoT cloud:

1. First, go to Device, then click on "New Device".
2. Click on "From template".
3. Select the Template, and give the device name.
4. Click on Create.
Then in the device info tab, you will get the Blynk Auth Token, Template ID, and Device Name. All these details will be required in the code.

## Source codes for this Blynk ESP32 IoT Project
Download link: https://github.com/techstudycell/IoT-Project-with-ESP32-Blynk-Timer-Sensor/tree/main/Code

## Get the IR Codes (HEX Code) From Remote
Now, to get the HEX codes from the remote, first, we have to connect the IR receiver output pin with GPIO D35.

And give the 5V across the VCC and GND. The IR receiver must have a metallic casing, otherwise, you may face issues.

Then follow the following steps to get the HEX codes.

1. Install the IRremote library in Arduino IDE
2. Download the attached code, and upload it to ESP32.
3. Open Serial Monitor with Baud rate 9600.
4. Now, press the IR remote button.
5. The respective HEX code will populate in the serial monitor.
Save all the HEX codes in a text file.

## Program the ESP32 for This Blynk Project

For programming the ESP32 on PCB, I have used another ESP32 development board.

Download and install the following libraries in Arduino IDE

1. Blynk Library (1.0.1): https://github.com/blynkkk/blynk-library
2. AceButton Library (1.9.2): https://github.com/bxparks/AceButton
3. IRremote Library (3.6.1): https://github.com/Arduino-IRremote/Arduino-IRremote
4. DHT Library (1.4.3): https://github.com/adafruit/DHT-sensor-library
Now open the main sketch (code).

5. In the code, you have to update the BLYNK_TEMPLATE_ID, BLYNK_DEVICE_NAME, Auth Token, WiFi Credentials.
6. Then update the HEX codes of the IR remote as shown in the tutorial video.
7. After that, select the DOIT ESP32 DEVKIT V1 board and proper PORT.
8. Then upload the code to ESP32 Board.

While uploading the code to ESP32, if you use the PCB then you will see the "Connecting....__ " text, then press and hold the BOOT button and then press the EN button, after that release both the buttons.

## Install Blynk IoT App to Configure Mobile Dashboard

1. Install the Blynk IoT app from Google Play Store or App Store. Then log in.
2. Go to Developer Mode.
3. Tap on the template that you have already made.
4. Now go to the Widget box (on the right) to add widgets.
5. Add 5 Button widgets and 2 Gauge widgets from Widget Box.
6. Go to Button widget settings.
7. Enter the name, select Datastream, Mode will be Switch. Then exit.
8. After setting all the Buttons tap on exit.

## Add Automation for Sensors and Timer
Now, you can define the automation in the Blynk IoT app according to your requirements.

In this project, I have added to total 3 Automations to the 3rd and 4th relay with DHT11 sensor and Timer.

In the tutorial video I have shown all the steps to add automation in Blynk IoT App.

## Connect Google Assistant With Blynk IoT Using IFTTT

To connect the Google Assistant with Blynk IoT I have used IFTTT.

Create an IFTTT account, then log in.

https://ifttt.com/

In the FREE plan, you can create 5 Applets. To control each relay you need 2 Applets, so to control 2 relays you need 4 Applets.

For each applet, you have to define a trigger and related action. In this project, if you say any pre-define commands in Google assistant, then the related Webhook request will be sent to the Blynk Cloud server.

Steps to add Google Assistant Trigger in Applet

1. Click on Create (on the top).
2. Click on Add.
3. Search for "Google Assistant" and click on it.
4. Click on "Say a Simple phrase".
5. Click on Connect and give the required permission.
6. Then enter "What you want to say" and "response" for Google 7. Assistant (as shown in the picture).
8. Click on "Create trigger".

## Steps to add Webhooks Action for Applet

Here in the action, we will add Webhooks to send web-request to update the Datastream value in the Blynk server.

1. Now click on the next Add button.
2. Search for Webhooks and click on it.
3. In Webhooks you have to mention the Blynk API URL
Please refer to the following Blynk API URL syntax to update the Datastream value.

Syntax: https://{server_address}/external/api/update?token={token}&{pin}={value}

1. fra1.blynk.cloud – Frankfurt
2. lon1.blynk.cloud – London
3. ny3.blynk.cloud – New York
4. sgp1.blynk.cloud – Singapore
5. blr1.blynk.cloud – Bangalore
The server region could be found in the right bottom corner of the web interface.

You can get the Auth Token from the Device Info tab. (Refer to tutorial video on top)

Now, enter the related Blynk URL to update the Datastream value. The method will be "GET". Keep other details as it is. (Refer to the picture)

1. Click on Create Action.
2. Click on Continue.
3. Click on Finish.
Our first Applet is created. In a similar way, you have to create the next 3 Applets. Please refer to the tutorial video.

## Finally!! the Blynk Smart Home System Is Ready

Now you can control your home appliances in a smart way.

I hope you have liked this new Blynk home automation project. I have shared all the required information for this project.

I will really appreciate it if you share your valuable feedback. Also if you have any queries please write in the comment section.

Thank you & Happy Learning.
