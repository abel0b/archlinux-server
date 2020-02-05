# Archlinux image
Build a custom archlinux image for Headless Server using archiso.

- Enable the ssh daemon
- Disable password login
- Add `admin` user
- Add a ssh key
- Install packages ufw, docker, docker-compose, vim
- Setup firewall

### Usage
```build
./build.sh -v
```
The modified boot image is now ready in out/archlinux-xxxxxxxx.iso.

### Create a bootable USB
Find the name of your drive with `lsblk`.

Run the following command, replacing /dev/sdx with your drive.
```bash
dd bs=4M if=path/to/archlinux.iso of=/dev/sdx status=progress oflag=sync
```

### Links
- [Archiso wiki article](https://wiki.archlinux.org/index.php/Archiso)
- [USB flash installation media](https://wiki.archlinux.org/index.php/USB_flash_installation_media)
