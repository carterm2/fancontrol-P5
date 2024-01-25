
#Fan Control for the Raspberry Pi 5 HexCase on Printables.com
1.  Put "fancontrol-P5.py" into a folder called "fancontrol" under your user directory ie: /home/'username'/**fancontrol-Pi5.py**
2.  Copy "fancontrol-P5.service" to /etc/systemd/system
3.  To start boot service: execute in shell...  
  sudo systemctl daemon-reload\
  sudo systemctl restart fancontrol-P5.service



#Wiring Fan to Pi5



![pi-GPIO](https://github.com/carterm2/fancontrol-P5/assets/11826844/726ef399-13b2-41d4-975e-7275f8ee6469)
