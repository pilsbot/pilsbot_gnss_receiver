For testing purposes, soft-link the corresponding ttyACM0 device to /dev/ttyGPS.
To find out which device it is, either look at dmesg output, or ask `gpsctl`.

For use in docker env, also change permissions.

```bash
export gps_dev=ttyACM0
sudo chmod o+rw /dev/$gps_dev
sudo ln -s /dev/$gps_dev /dev/ttyGPS
```