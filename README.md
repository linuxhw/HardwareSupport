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
| Card reader                  | 14093   | 100%    |
| Communication controller     | 57545   | 98.42%  |
| Dma controller               | 171     | 99.42%  |
| Dvb card                     | 110     | 100%    |
| Encryption controller        | 13506   | 90.32%  |
| Firewire controller          | 10858   | 99.97%  |
| Flash memory                 | 550     | 37.82%  |
| **Graphics card**            | 126746  | 98.29%  |
| Input device controller      | 331     | 100%    |
| Ipmi smic interface          | 341     | 100%    |
| Modem                        | 414     | 90.58%  |
| Multimedia controller        | 4098    | 91.39%  |
| **Net/ethernet**             | 79911   | 99.92%  |
| Net/other                    | 13881   | 99.78%  |
| **Net/wireless**             | 63714   | 99.78%  |
| Non-essential instrumenta... | 9221    | 99.99%  |
| **Sd host controller**       | 15101   | 100%    |
| Serial bus controller        | 23175   | 99.87%  |
| Serial controller            | 8232    | 99.85%  |
| Signal processing controller | 58917   | 97.62%  |
| Smbus                        | 93885   | 99.91%  |
| **Sound**                    | 148842  | 99.98%  |
| Tv card                      | 1117    | 100%    |
| Usb controller               | 296736  | 100%    |

Avg. hardware support is: 99.34%