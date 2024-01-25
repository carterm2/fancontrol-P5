# FanControl for HexFanCase P5 on Printables.com

## Fan idle until 50C CPU temperature, ramps to 100% speed at 80C.

1.  Download fancontrol-P5.py and fancontrol-P5.service (home directory or subfolder)

2.  Edit fancontrol-P5.service file to point to /home/{username}/fancontrol-P5.py
    
3.  Move "fancontrol-P5.service" to /etc/systemd/system

4.  To start boot service: execute in shell
    
                          sudo systemctl daemon-reload
                          sudo systemctl restart fancontrol-P5.service


### Wiring Fan to Pi5



![pi-GPIO](https://github.com/carterm2/fancontrol-P5/assets/11826844/726ef399-13b2-41d4-975e-7275f8ee6469)
![HexCase-FanWiringLow](https://github.com/carterm2/fancontrol-P5/assets/11826844/245cbf54-08c0-4f5f-af06-896680aab7b6)
