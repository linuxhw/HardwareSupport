Hardware Support Status
=======================

This is a project to estimate status of hardware support (PCI only) in Linux with the help of
lists of supported device IDs [1] taking into account popularity of devices [2] and list of
devices with bad Linux-compatibility [3]. Storage controllers are not analysed in this report
because device population is based on workstations that have successfully installed Linux.

* [1] Lists of supported device IDs (https://github.com/linuxhw/Drivers)
* [2] Popularity of devices (https://github.com/linuxhw/DevicePopulation)
* [3] List of devices with bad Linux-compatibility (https://github.com/linuxhw/HWInfo)

We determine support status by the following formula:

    Status = (S1*T1 + S2*T2 + ... + Sn*Tn) / (T1 + T2 + ... + Tn)

    Sn — support status of the device (1 — supported, 0 — not supported)

    Tn — total number of device samples

Everyone can contribute to this report by uploading probes of their computers by
the [hw-probe](https://github.com/linuxhw/hw-probe) tool:

    sudo -E hw-probe -all -upload

### Results

Devices — total devices,
Support — supported in Linux.

| PCI Class                    | Devices | Support |
|------------------------------|---------|---------|
| Card reader                  | 9433    | 100%    |
| Communication controller     | 39144   | 98.23%  |
| Dma controller               | 115     | 99.13%  |
| Dvb card                     | 85      | 100%    |
| Encryption controller        | 8169    | 88.64%  |
| Firewire controller          | 7978    | 99.97%  |
| Flash memory                 | 469     | 37.95%  |
| **Graphics card**            | 89190   | 98.06%  |
| Input device controller      | 262     | 100%    |
| Ipmi smic interface          | 155     | 100%    |
| Modem                        | 307     | 89.58%  |
| Multimedia controller        | 2194    | 88.56%  |
| **Net/ethernet**             | 55774   | 99.92%  |
| Net/other                    | 10929   | 99.82%  |
| **Net/wireless**             | 43499   | 99.80%  |
| Non-essential instrumenta... | 5103    | 99.98%  |
| **Sd host controller**       | 10370   | 100%    |
| Serial bus controller        | 12251   | 99.80%  |
| Serial controller            | 4901    | 99.84%  |
| Signal processing controller | 37989   | 97.22%  |
| Smbus                        | 62763   | 99.92%  |
| **Sound**                    | 103406  | 99.95%  |
| Tv card                      | 902     | 100%    |
| Usb controller               | 215098  | 100%    |

Avg. hardware support is: 99.27%