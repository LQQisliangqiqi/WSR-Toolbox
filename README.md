<div align="center">
  <a href="https://react.seas.harvard.edu//">
    <img align="left" src="figs/lab_logo.png" width="150" alt="REACT Lab and WiTech Lab">
  </a>
  <a href="https://react.seas.harvard.edu/communication-sensor">
    <img align="center" src="figs/toolbox_logo.png" width="300" alt="WSR Toolbox">
  </a>
  <a href="https://www.seas.harvard.edu/">
    <img align="right" src="figs/university_logo.png" width="150" alt="SEAS Harvard and CMU">
  </a>
</div>
<p>&nbsp;</p>

# WiFi-Based  Relative  Bearing  Sensor

WiFi-Sensor-for-Robotics (WSR) toolbox is an open source library, that enables robots in a team to obtain relative bearing to each other by analyzing the phase of their communicated wireless signals as they traverse the environment. Importantly, this capability can be used in non-line-of-sight (NLOS) or visually degraded environements to recover relative spatial positioning information between robots with implications for localization, networking and security amongst others. This toolbox is designed for distributed deployment and real-time operation on robotic platforms using commodity hardware.

![Paper](figs/Paper_logo.png)

### Requirements
1. Wireless channel data collected by both signal transmitting and receiving robots. Refer the wiki [WiFi Driver and Firmware for Wireless channel data (CSI) collection](https://github.com/Harvard-REACT/WSR-Toolbox/wiki/WiFi-Driver-and-Firmware-for-Wireless-channel-data-(CSI)-collection) for details about software and hardware requirements and installation steps.
2. Local displacement of the signal receiving robot. Any pose estimation sensor can be used as long as the input is provided in csv file in the following format:
```
{sec,nsec,x,y,z,yaw,pitch}
``` 
where sec and nsec refer the local timestamp in seconds and nanoseconds respectively; {x,y,z} are the position coordinates.

The installation intructions can be found in the [wiki page: WSR Toolbox cpp](https://github.com/Harvard-REACT/WSR-Toolbox/wiki/WSR-Toolbox-cpp).

### Architecture

![Testbed map](figs/toolbox_architecture.png)


## Relevant code repositories:
1. The core C++ library: [WSR-Toolbox-cpp] (https://github.com/Harvard-REACT/WSR-Toolbox-cpp). 
2. Intel 5300 modified wifi driver and firmware : [WSR-WifiDriver](https://github.com/Harvard-REACT/WSR-WifiDriver)
3. Supplementary tool: [WSR-Toolbox-linux-80211n-csitool-supplementary](https://github.com/Harvard-REACT/WSR-Toolbox-linux-80211n-csitool-supplementary)

The wifidriver and supplementary tool repositories are a modified version of code released as part [Linux 802.11n CSI Tool](http://dhalperi.github.io/linux-80211n-csitool/). A detailed explanation of design decision behind the modifications (i.e support for channel reprocity, handling packet collision) can be found in the publication [**Toolbox  Release:  A  WiFi-Based  Relative  Bearing  Sensor  for  Robotics**]()

## Open-Source Datasets
These dataset are collected for indoor environments in LOS and NLOS for different robot trajectories
1. [WSR-Toolbox-Dataset](https://github.com/Harvard-REACT/WSR-Toolbox-Dataset)


## Performance Evaluation


## Citation
- [1] Jadhav Ninad*, Weiying Wang*, Diana Zhang, O. Khatib, Swarun Kumar and Stephanie Gil. [**WSR: A WiFi Sensor for Collaborative Robotics**](https://arxiv.org/abs/2012.04174)

```bibtex
@article{Jadhav2020WSRAW,
  title={WSR: A WiFi Sensor for Collaborative Robotics},
  author={Ninad Jadhav and Weiying Wang and Diana Zhang and O. Khatib and Swarun Kumar and Stephanie Gil},
  journal={ArXiv},
  year={2020},
  volume={abs/2012.04174}
}
```

- [2] Jadhav Ninad, Weiying Wang, Diana Zhang, Swarun Kumar and Stephanie Gil. [**Toolbox  Release:  A  WiFi-Based  Relative  Bearing  Sensor  for  Robotics**]().
 

## Acknowledgments
We  gratefully  acknowledge  funding  support  through  the NSF and MIT Lincoln Laboratories. Experiments were conducted in the the REACT Lab.

## License

[BSD License](LICENSE.BSD)