# Smartthings-for-Broadlink-RM-Pro
Smartthings Handler for Broadlink RM Pro using RM Plugin, RM Bridge &amp; Home Automation

I refered to the below.

http://thingsthataresmart.wiki/index.php?title=URI_Switch

https://github.com/beckyricha/Broadlink-RM-SmartThings-Alexa


If you set up one of RM Plugin(with HTTP Bridge), RM Bridge and HA(Home Assistant), you can controll the Broadlink RM Pro with HTTP POST or GET method.

You can controll the Broadlink device with this handler at the Smarttings using the API. This hadler doesn't use a smartapp and you can input device URI information at a PC and your phone.(I recommand you to use the PC)


Copy the contents(Broadlink Virtual Switch.groovy) and create new device handler at Smartthings IDE web.
Paste it to 'From code' and save.
(If you are using the RM Bridge, you have to change the both methods from "POST" to "GET" in the code for On and Off)
Publish it 'for me'
Go to my device.
Create a device with '+ New Device'
Input Name, Label, Device Network ID as you want.
Select the 'Broadlink Virtual Switch' at the Type
Select the Location and Hub then click the 'Create'

Click the 'Preference(edit)'
You can input the information about the devices what you want to control

If you are using the RM Plugin,
Usually ON and Off command URI is like the below.
http://192.168.0.33:9876/send?deviceMac=aabbccddeeff&codeId=11 (If you don't set up a Authentication)
http://yourID:yourPassword@192.168.0.33:9876/send?deviceMac=aabbccddeeff&codeId=11 (If you set up a Authentication)

ID & PW for RM Plugin or RM Bridge(Optional) : yourID:yourPassword (If you don't set up a Authentication, you may leave it as blank)
IP for RM Plugin or RM Bridge or HA(Required for all) : 192.168.0.33
Port(Required for all) : 9876
On Path(Required for all) : /send?deviceMac=aabbccddeeff&codeId=11
Off Path(Optional) : /send?deviceMac=aabbccddeeff&codeId=12 (If you don't want to use the off command, you can leave it as blank)
Entity ID of Body Data for HA(Required for HA) : Leave it as blank


