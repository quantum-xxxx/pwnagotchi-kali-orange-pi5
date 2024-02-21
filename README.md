## Hardware
1. Orange Pi 5 4G RAM
2. TP-Link Archer T2U PLUS [RTL8821AU] (__2357:0120 TP-Link Archer T2U PLUS [RTL8821AU]__)
3. USB GN-803G (u-Blox 8) (__GPS on /dev/ttyACM0__)  (__1546:01a8 U-Blox AG [u-blox 8]__)
4. Noname Bluetooth 5.1 + EDR USB adapter (__0bda:a725 Realtek Semiconductor Corp. Bluetooth Radio__)
5. [PowerBank Baseus PPCXZ10](https://www.baseus.com/products/magnetic-foldable-power-bank-20w-10000mah)
6. The case is https://www.thingiverse.com/thing:6363862

## OS
[Kali Linux](https://github.com/leeboby/kali-images)

## Base
based on https://github.com/jayofelony/pwnagotchi-bookworm


## Run

run `ansible-playbook ansible/main.yaml --connection=local -e pwn_user=${USER}`


## Issues

1. Looks like wlan0mon is created for pwngrid-peer but not working. The bettercap and pwnagotchi are using wlan0 in monitor mode directly
2. Chrony don't sync from GPS, but from Bluetooth Tethering time sync is ok.
