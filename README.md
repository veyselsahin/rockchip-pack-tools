The files are for RK3188 radxa rock pro. 



Tools for packing a Linux firmware(aka update.img) for rockchip platform.

Firstly make the device working. Unbrick and make it working via nand if it's not working. Then, execute the command to make it working on SD card. 

The update.img can be found here: 
https://drive.google.com/file/d/1xdKH9Fsic8moZ6AIdZbf54_0t9hJ50gr/view?usp=sharing

```
sudo ./upgrade_tool DI -p parameter   -s RK3188Loader\(L\)_V2.19.bin -b sdboot_rk3188.img -m update.img   package-file
```

Push the image into the device

```
sudo ./upgrade_tool UF  update.img
```

### How to use it
#### Prepare kernel and rootfs
Run

    ./getimage.sh    # Download the kernel and rootfs from dl.radxa.com
Or

    mkdir Linux

Put your [boot.img](http://wiki.radxa.com/Rock/Booting_Linux) as name `boot-linux.img` and [rootfs](http://wiki.radxa.com/Rock/ubuntu) as name `rootfs.img` under Linux folder

#### Pack the image     
Run

    ./mkupdate.sh    # Pack the image


