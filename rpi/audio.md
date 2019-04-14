=Step 2: Bluetooth Hardware
To turn off built-in Bluetooth controller (BCM43438), blacklist it:
sudo nano /etc/modprobe.d/raspi-blacklist.conf

Add lines:
blacklist btbcm
blacklist hci_uart

CTRL+X, then Y, then Enter

Reboot:
sudo reboot
