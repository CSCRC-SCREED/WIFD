<h1 align="center">
  <br>
  <a href=""><img src="./assets/logos/warwick-logo.png" alt="WIFD" width="200"></a>
  <br>
  WARWICK IMAGE FORENSICS DATASET
  <br>
</h1>

<h4 align="center">A comprehensive dataset for advancing digital forensic research.</h4>

<p align="center">
    <a href="#about">About</a> •
    <a href="#cameras">Cameras</a> •
    <a href="#instructions">How To Use</a> •
    <a href="#citations">Citations</a> •
    <a href="#license">License</a>
</p>

## About
The Warwick Image Forensics Dataset is crafted to address the evolving challenges in the field of digital forensics, specifically for device fingerprinting involving sensor pattern noise (SPN). As digital photography advances, particularly in consumer-level mobile devices, the need for sophisticated analysis tools becomes crucial. This dataset responds to the shifting landscape caused by innovations in camera parameter flexibility and the rise of multi-frame photography techniques like high dynamic range (HDR) imaging.

Featuring over 58,600 images from 14 different digital cameras, each carefully captured under varied exposure settings, this dataset is designed to facilitate in-depth research on device fingerprinting. It provides a rich resource for exploring how different exposure settings affect forensic analysis, making it an ideal tool for developing and testing new computational photography algorithms.

More detailed information can be found in our original paper [Warwick Image Forensics Dataset for Device Fingerprinting in Multimedia Forensics](https://ieeexplore.ieee.org/abstract/document/9102783).

## Cameras
Details of the cameras used in the Warwick Image Forensics Dataset are crucial for understanding the diversity and capability of data acquisition methods employed. The dataset utilizes 14 different digital cameras, each offering unique features that contribute to the depth and variability of the dataset. Below is a summary table of the cameras used:

| No. | Camera             | Resolution | Sensor Format | Sensor Dimensions | CFA Type     | Lens            |
|-----|--------------------|------------|---------------|-------------------|--------------|-----------------|
| 1   | Canon EOS 6D       | 3648 x 5472| 35 mm         | 35.8 x 23.9 mm²   | Bayer Filter | Interchangeable |
| 2   | Canon EOS 6D Mark II | 4160 x 6240 | 35 mm       | 35.9 x 24 mm²     | Bayer Filter | Interchangeable |
| 3   | Canon EOS 80D      | 4000 x 6000| APS-C         | 22.5 x 15 mm²     | Bayer Filter | Interchangeable |
| 4   | Canon EOS M6       | 4000 x 6000| APS-C         | 22.3 x 14.9 mm²   | Bayer Filter | Interchangeable |
| 5   | Fujifilm X-A10.1   | 3264 x 4896| APS-C         | 23.6 x 15.6 mm²   | Bayer Filter | Interchangeable |
| 6   | Fujifilm X-A10.2   | 3264 x 4896| APS-C         | 23.6 x 15.6 mm²   | Bayer Filter | Interchangeable |
| 7   | Nikon D7200        | 4000 x 6000| APS-C         | 23.5 x 15.6 mm²   | Bayer Filter | Interchangeable |
| 8   | Panasonic Lumix DC-TZ90.1 | 3888 x 5184 | 1/2.3" | 6.16 x 4.62 mm² | Bayer Filter | Fixed          |
| 9   | Panasonic Lumix DC-TZ90.2 | 3888 x 5184 | 1/2.3" | 6.16 x 4.62 mm² | Bayer Filter | Fixed          |
| 10  | Olympus E-M10 Mark II | 3456 x 4608 | Four Thirds | 17.3 x 13 mm²   | Bayer Filter | Interchangeable |
| 11  | Sigma Sd Quattro    | 3616 x 5424| Foveon X3    | 23.4 x 15.5 mm²   | NA           | Interchangeable |
| 12  | Sony Alpha 68       | 4000 x 6000| APS-C         | 23.5 x 15.6 mm²   | Bayer Filter | Interchangeable |
| 13  | Sony RX100.1        | 3648 x 5472| 1”            | 13.2 x 8.8 mm²    | Bayer Filter | Fixed           |
| 14  | Sony RX100.2        | 3648 x 5472| 1”            | 13.2 x 8.8 mm²    | Bayer Filter | Fixed           |

This comprehensive array of cameras allows researchers to study various aspects of digital image forensics, including sensor noise, resolution impacts, and the effects of different lens and sensor configurations on image forensics.

## Instructions

### Cloning the Repository
To get started with the Warwick Image Forensics Dataset, you will first need to clone the repository. Use the following command to clone it to your local machine:
```sh
git clone https://github.com/your-username/warwick-image-forensics-dataset.git
```

### Dataset Structure
The dataset is divided into device folders, and within each device folder, there are subfolders for reference images, SDR images, and scenes (1-21). Each scene folder contains images categorized by ISO settings and further organized by extension type.
```
dataset/
├── device_1/
│   ├── reference/
│   │   ├── img_0001.jpg
│   │   ├── img_0002.jpg
│   │   └── ...
│   ├── sdr_image/
│   │   ├── img_0001.jpg
│   │   ├── img_0002.jpg
│   │   └── ...
│   └── scene_01/
│       ├── AEB/
│       │   ├── ISO100/
│       │   │   ├── jpg/
│       │   │   │   ├── img_0001.jpg
│       │   │   │   ├── img_0002.jpg
│       │   │   │   └── ...
│       │   │   ├── cr2/
│       │   │   │   ├── img_0001.cr2
│       │   │   │   ├── img_0002.cr2
│       │   │   │   └── ...
│       │   │   └── ...
│       └── Burst/
│           ├── ISO100/
│           │   ├── jpg/
│           │   │   ├── img_0001.jpg
│           │   │   ├── img_0002.jpg
│           │   │   └── ...
│           │   ├── cr2/
│           │   │   ├── img_0001.cr2
│           │   │   ├── img_0002.cr2
│           │   │   └── ...
│           │   └── ...
│           └── ...
│    
└── ...

```
### Naming Conventions
**AEB (Auto Exposure Bracketing)** and **Burst** images are named using the following convention:
```
<device_name>_scene<scene_number>_ISO<iso>_<exposure_time>_<fnumber>_<sequence_number>.<extension>
```

**Reference** and **SDR (Standard Dynamic Range)** images are named using the following convention:
```
<device_name>_sdr_image_ISO<iso>_<exposure_time>_<fnumber>_<sequence_number>.<extension>
```

- `device_name`: The name of the camera device.
- `scene_number`: The scene number.
- `ISO`: The ISO setting used.
- `exposure_time`: The exposure time for the image.
- `fnumber`: The aperture value used.
- `sequence_number`: The sequence number for multiple images with the same settings, only occurs when multiples are present.
- `extension`: The file extension (e.g., jpg, tif).


## Citations
We kindly request that if you use the Warwick Image Forensic Dataset in your research or work, please cite our original paper. Here is the Bibtex entry for citation:
```
@inproceedings{quan2020warwick,
    author={Quan, Yijun and Li, Chang-Tsun and Zhou, Yujue and Li, Li},
    booktitle={2020 IEEE International Conference on Multimedia and Expo (ICME)}, 
    title={Warwick Image Forensics Dataset for Device Fingerprinting in Multimedia Forensics}, 
    year={2020},
    pages={1-6},
    doi={10.1109/ICME46284.2020.9102783}
}
```

## License

The data and code housed in this repository are released under the [MIT License](./LICENSE). This choice supports open innovation and collaboration by permitting free use, modification, and distribution of the project.

<hr>
<h4 align="center">Cyber Security Cooperative Research Centre</h4>
<div align="center" style="display: flex; justify-content: center; gap: 50px;">
    <img src="./assets/logos/warwick-logo.png" alt="Logo 1" style="width: 5%; height: 5%;">
    <img src="./assets/logos/deakin-logo.png" alt="Logo 2" style="width: 10%; height: 10%;">
    <img src="./assets/logos/cscrc-logo.png" alt="Logo 3" style="width: 3%; height: 5%;">
</div>

