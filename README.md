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

    Sn - support status of the device (1 - supported, 0 - not supported)

    Tn - total number of device samples

Everyone can contribute to this report by uploading probes of their computers by
the [hw-probe](https://github.com/linuxhw/hw-probe) tool:

    sudo -E hw-probe -all -upload

### Results

Devices - total devices,
Support - supported in Linux.

| PCI Class                    | Devices | Support |
|------------------------------|---------|---------|
| Card reader                  | 19657   | 100%    |
| Communication controller     | 80720   | 98.54%  |
| Dma controller               | 427     | 99.77%  |
| Dvb card                     | 124     | 100%    |
| Encryption controller        | 20371   | 91.53%  |
| Firewire controller          | 13826   | 99.97%  |
| Flash memory                 | 620     | 37.74%  |
| **Graphics card**            | 170802  | 99.01%  |
| Input device controller      | 389     | 100%    |
| Ipmi smic interface          | 553     | 100%    |
| Modem                        | 490     | 91.02%  |
| Multimedia controller        | 7336    | 93.05%  |
| **Net/ethernet**             | 106336  | 99.91%  |
| Net/other                    | 18283   | 99.79%  |
| **Net/wireless**             | 88417   | 99.82%  |
| Non-essential instrumenta... | 13957   | 99.97%  |
| Parallel controller          | 51      | 58.82%  |
| **Sd host controller**       | 20744   | 100%    |
| Serial bus controller        | 40815   | 99.94%  |
| Serial controller            | 12546   | 99.88%  |
| Signal processing controller | 87504   | 97.80%  |
| Smbus                        | 127632  | 99.91%  |
| **Sound**                    | 202774  | 99.93%  |
| Tv card                      | 1263    | 100%    |
| Usb controller               | 387885  | 100%    |

Avg. hardware support is: 99.43%