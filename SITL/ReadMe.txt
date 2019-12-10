1. open 3 tabs 
2. 

Terminal 1 - Start SITL: 
dronekit-sitl copter --home=7.086271,80.038264,0,0

Terminal 2 - Start MavProxy:
mavproxy --master tcp:127.0.0.1:5760 --out udp:127.0.0.1:14550 --out udp:127.0.0.1:14552

Now you can now opne mission planner and connect to UDP baus 921600 on port 14552

Terminal 3 - Start your code , connect to 127.0.0.1:14550
python .\Hover_and_Land.py  --connect 127.0.0.1:14550