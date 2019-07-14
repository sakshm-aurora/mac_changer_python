A python script to change mac address of your system.

# Why change the MAC Address?
1. Increase anonymity.
2. Impersonate other devices.
3. Bypass filters.

# Algorithm
Goal → To change the mac address of the system.
Setps:
1. Let user specify the interface and new mac address as options while executing the python script.
2. The system has to run the following commands:
  3. ifconfig <interface> down
  4. ifconfig <interface> hw ether <new_mac>
  5. ifconfig <interface> up
6. I used the module "systemprocess" to execute these system commands and another module "optparser" to take user input as options while executing the script.

# Conclusion
1. Users can run the script as :
2. ./mac_changer.py --interface eth0 --mac 11:22:33:44:55:66
3. or
4. ./mac_changer.py -i eth0 -m 11:22:33:44:55:66
and this will automatically change the mac address for the given interface as the new given mac address.
5. Use ./mac_changer.py --help  or ./mac_changer.py -h for more details.
