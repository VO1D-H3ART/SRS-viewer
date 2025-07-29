# SRS-viewer
A simple webviewer for steaming to SRS 

--- July 27th --- 

This is an ultra simple webviewer for RTMP streams from OBS.

## To use this on a windows machine do the following steps

Step 1: Install the windows release of SRS found here: https://github.com/ossrs/srs/releases/tag/v5.0-r3 

Step 2: Run srs.exe as admin. Without this step OBS will fail to connect to the srs server.

Step 3: Use a custom stream link and make the stream key whatever you want 
  Ex) rtmp:// YOUR IP HERE!!!/live

Step 4: Edit this .HTML file with the IP in the server and you are good to go.

## Tips

- If you are getting issues make sure to make a TCP 8080 rule on the windows fire wall. To do this you need to press Win+R and then run wf.msc from there under inbound rules you need to make a new TCP rule and allow it on all networks. This tip applies if you are on older versions of windows like Windows 10 version 1809 (Good times).

- Do not forget to change the IP line in the index.html file or else you will not see anything, only a stream buffering nothing

- DO NOT USE GITHUB PAGES!! Look under **Local Hosting** for more info on how to host this thing.

- Make sure you are on the same LAN/subnet to deploy this solution optimally



## Local Hosting

To make this solution work you MUST be on the same network or subnet. The solution I am using is [TailScale](https://tailscale.com/) its free and allows for a mesh network which means any device connected to TailScale network can "talk" to each other. Basically acting as a VPN (Virtual Private Network). So if there are diffrent subnets on your network this will help make sure you can connect to any access point and the viewer will still work

GitHub pages will not work with this solution because it uses HTTPS while SRS uses HTTP. The diffrence is that HTTPS is that it's more secure therefore causes more issues in configuring the stream to work. Security should generally not be an issue because this is run locally.

## Using HTTP and Not HTTPS (GitHub Pages)

To bypass the use of HTTPS we host the viewer.html on the SRS server itself. In order to do this Right click on the SRS desktop shortcut -> open file location -> objs -> nginx -> html and paste the viewer.html in this folder. To open this folder in the broswer you have to do **http**:// YOUR IP HERE/viewer.html DO NOT FORGET TO USE **HTTP**



