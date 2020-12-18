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
| Card reader                  | 10870   | 100%    |
| Communication controller     | 44546   | 98.28%  |
| Dma controller               | 125     | 99.20%  |
| Dvb card                     | 88      | 100%    |
| Encryption controller        | 9702    | 89.16%  |
| Firewire controller          | 8843    | 99.97%  |
| Flash memory                 | 497     | 37.83%  |
| **Graphics card**            | 100143  | 98.13%  |
| Input device controller      | 279     | 100%    |
| Ipmi smic interface          | 215     | 100%    |
| Modem                        | 332     | 89.46%  |
| Multimedia controller        | 2720    | 89.85%  |
| **Net/ethernet**             | 62340   | 99.92%  |
| Net/other                    | 12254   | 99.80%  |
| **Net/wireless**             | 49324   | 99.79%  |
| Non-essential instrumenta... | 6249    | 99.98%  |
| **Sd host controller**       | 11691   | 100%    |
| Serial bus controller        | 15375   | 99.82%  |
| Serial controller            | 5797    | 99.86%  |
| Signal processing controller | 44220   | 97.34%  |
| Smbus                        | 70658   | 99.92%  |
| **Sound**                    | 116477  | 99.95%  |
| Tv card                      | 961     | 100%    |
| Usb controller               | 238607  | 100%    |

Avg. hardware support is: 99.28%