# HOW to install

sudo mkdir -p /lib/modules/$(uname -r)/kernel/drivers/net/wireless/

sudo cp AX5400UA.ko /lib/modules/$(uname -r)/kernel/drivers/net/wireless/

sudo chmod 644 /lib/modules/$(uname -r)/kernel/drivers/net/wireless/AX5400UA.ko

sudo depmod -a

sudo insmod /lib/modules/$(uname -r)/kernel/drivers/net/wireless/AX5400UA.ko

# CHECK
lsmod | grep 8852cu

# IF YOU GET TROUBLE
report issue with result of "lsusb"

example
lsusb
Bus 001 Device 012: ID 0bda:c832 Realtek Semiconductor Corp. 802.11ax WLAN Adapter
To support, I need number like "0bda:c832"


thx for https://github.com/lwfinger/rtw8852cu/issues/17
