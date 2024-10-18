# HOW to install

sudo mkdir -p /lib/modules/$(uname -r)/kernel/drivers/net/wireless/

sudo cp AX5400UA.ko /lib/modules/$(uname -r)/kernel/drivers/net/wireless/

sudo chmod 644 /lib/modules/$(uname -r)/kernel/drivers/net/wireless/AX5400UA.ko

sudo depmod -a

sudo insmod /lib/modules/$(uname -r)/kernel/drivers/net/wireless/AX5400UA.ko

# CHECK
lsmod | grep 8852cu




thx for https://github.com/lwfinger/rtw8852cu/issues/17
