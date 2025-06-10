# IU-ARS

# From Zero to High-Speed Racing: An Autonomous Racing Stack

**[Project Website & Dataset Download](https://iurl.iu.edu/ars)** 🏎️

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)
[![Paper](https://img.shields.io/badge/paper-PDF-b31b1b.svg)](https://scholarworks.iu.edu/dspace/handle/2022/29849)
[![Dataset](https://img.shields.io/badge/dataset-Download-blue.svg)](https://github.com/your-username/your-repo/releases/tag/v1.0.0)
[![Event](https://img.shields.io/badge/Event-Indy%20Autonomous%20Challenge-orange.svg)](https://www.indyautonomouschallenge.com/)

This repository contains the official code and dataset for the paper **"From Zero to High-Speed Racing: An Autonomous Racing Stack,"** from the IU Luddy Autonomous Racing team at Indiana University.

![IU Autonomous Race Car](assets/images/racecar_on_track.jpg)
*The IU Luddy Team's Dallara AV-21 on the Indianapolis Motor Speedway.*

---

## Abstract

> High-speed, head-to-head autonomous racing presents substantial technical and logistical challenges, including precise localization, rapid perception, dynamic planning, and real-time control—compounded by limited track access and costly hardware. This paper introduces the Autonomous Race Stack (ARS), developed by the IU Luddy Autonomous Racing team for the Indy Autonomous Challenge (IAC). We present three iterations of our ARS, each validated on different tracks and achieving speeds up to 260 km/h. Our contributions include: (i) the modular architecture and evolution of the ARS across ARS1, ARS2, and ARS3; (ii) a detailed performance evaluation that contrasts control, perception, and estimation across oval and road-course environments; and (iii) the release of a high-speed, multi-sensor dataset collected from oval and road-course tracks. Our findings highlight the unique challenges and insights from real-world high-speed full-scale autonomous racing.

---

## 💿 Dataset

A key contribution of this work is the release of our high-speed, multi-sensor dataset from both oval and road-course tracks. This includes data from LiDAR, cameras, GPS/IMU, and vehicle CAN bus.

You can download the dataset from our **[Releases page](https://github.com/your-username/your-repo/releases/tag/v1.0.0)**.

We provide scripts to parse and visualize the data. To visualize a log file, run:
```bash
python scripts/visualize_log.py --log_path /path/to/dataset/road_course_run_01.bag
```

---

## 📊 Software Stack (ARS)

This repository contains the implementation of **ARS3**.

### Setup

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/your-username/your-repository-name.git](https://github.com/your-username/your-repository-name.git)
    cd your-repository-name
    ```

2.  **Install dependencies:**
    This project is built on ROS 2. Please follow the instructions in the `INSTALL.md` file for detailed setup and dependency information. We provide a `requirements.txt` for Python packages.
    ```bash
    pip install -r requirements.txt
    ```

### Usage

To run a simulation of the ARS stack using our provided dataset:
```bash
ros2 launch ars_simulation simulation.launch.py log_file:=/path/to/dataset/oval_run_01.bag
```

---

## Citation

If you use our work or dataset in your research, please cite our paper:

```bibtex
@inproceedings{Jardali2025ars,
  title     = {From Zero to High-Speed Racing: An Autonomous Racing Stack},
  author    = {Jardali, Hassan and Pushp, Durgakant and Yu, Youwei and Ali, Mahmoud and Mohamed, Ihab S. and Murillo-Gonzalez, Alejandro and Coen, Paul and Khan, Md. Al-Masrur and Pulivendula, Reddy Charan and Park, Saeoul and Zhou, Lingchuan and Liu, Lantao},
  booktitle = {Indy Autonomous Challenge Proceedings},
  year      = {2025},
  publisher = {Indiana University},
  url       = {[https://scholarworks.iu.edu/dspace/handle/2022/29849](https://scholarworks.iu.edu/dspace/handle/2022/29849)}
}
```

---

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.
