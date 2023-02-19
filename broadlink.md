# Configure Broadlink RM Remote without application.

1. ```pip3 install broadlink ```
1. For each remote press reset button untill it start flashing frequently. Then release and press reset button again - untill it start flashing 3 or 4 times in a row
1. start python
1. Connect to one of the following open networks : BradlinkProv, Universal Remote, BroadLink_WiFi_Device
1. run following code in the python console: 
```
import broadlink
broadlink.setup('your-ssid', 'your-password',4)
```

After setup, the 3-4 long flashes occurs, indicating that remote is connecting your wifi. When LED stops flashing, the remote is connected

Please note, that remote must be unlocked : refer python-broadlink manual. HomeAssistant will unlock it for you.
