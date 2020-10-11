Hardware Support Status
=======================

This is a project to estimate status of hardware support (PCI only) in Linux with the help of
[lists of supported device IDs](https://github.com/linuxhw/Drivers) taking into account [popularity of devices](https://github.com/linuxhw/DevicePopulation)
and [list of devices with bad Linux-compatibility](https://github.com/linuxhw/HWInfo). Storage controllers are not analysed
in this report because device population is based on workstations that have successfully installed Linux.

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
| Card reader                  | 8032    | 100%    |
| Communication controller     | 33611   | 98%     |
| Dma controller               | 103     | 99.03%  |
| Encryption controller        | 6492    | 87.75%  |
| Firewire controller          | 7173    | 99.99%  |
| Flash memory                 | 455     | 37.80%  |
| **Graphics card**            | 78096   | 97.94%  |
| Input device controller      | 240     | 100%    |
| Ipmi smic interface          | 110     | 100%    |
| Modem                        | 288     | 89.24%  |
| Multimedia controller        | 1724    | 86.83%  |
| **Net/ethernet**             | 49021   | 99.91%  |
| Net/other                    | 9558    | 99.78%  |
| **Net/wireless**             | 37431   | 99.82%  |
| Non-essential instrumenta... | 3562    | 100%    |
| **Sd host controller**       | 9041    | 100%    |
| Serial bus controller        | 9196    | 99.82%  |
| Serial controller            | 4058    | 99.88%  |
| Signal processing controller | 31543   | 97.04%  |
| Smbus                        | 54625   | 99.93%  |
| **Sound**                    | 90010   | 99.95%  |
| Tv card                      | 845     | 100%    |
| Usb controller               | 191591  | 100%    |

Avg. hardware support is: 99.24%