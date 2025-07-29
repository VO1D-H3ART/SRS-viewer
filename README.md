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

- 
