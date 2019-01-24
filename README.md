# ESP32

model: €SPRESSIF ESP32-WROOM-32

## Set up micropython firmware

```shell
pip install esptool
pip3 install rshell
```

<http://micropython.org/download>

> Program your board using the esptool.py program, and put the firmware starting at address 0x1000. For example: esptool.py --chip esp32 --port /dev/ttyUSB1 write_flash -z 0x1000 esp32-20180511-v1.9.4.bin. If you are putting MicroPython on for the first time then you should first erase the entire flash using esptool.py --chip esp32 erase_flash. 

```shell
esptool.py --port /dev/ttyUSB0 erase_flash
esptool.py --chip esp32 --port /dev/ttyUSB0 write_flash -z 0x1000 ./esp32-20180511-v1.9.4.bin 
```

## Use micropython

```shell
rshell --buffer-size=30 -p /dev/ttyUSB0
```
