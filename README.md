# UA-SISM
This is the official code for UA-SISM.

# Installation

```pip install -r requirements.txt```

# Framework

![1](1.png)

# Visualization on WHU-Stereo dataset
![2](2.png)

(a) left image. (b) disparity ground truth. (c) SGM. (d) PSMNet. (e) GwcNet. (f) HMSMNet. (g) DLNR. (h) PCV. (i) Ours.

# Visualization on US3D dataset
![3](3.png)

(a) left image. (b) disparity ground truth. (c) SGM. (d) PSMNet. (e) GwcNet. (f) HMSMNet. (g) DLNR. (h) PCV. (i) Ours.


# Dataset Preparation
* [WHU-Stereo](https://github.com/Sheng029/WHU-Stereo)
* [US3D](https://ieee-dataport.org/open-access/data-fusion-contest-2019-dfc2019)
  
  Note：If you want to use our preprocessed US3D dataset, please download：

# Comparsion WHU-Stereo dataset
The best score for each metric is marked in **bold**.
|Method       |  EPE(Px)  |  D1(%) |
|-------------|-----------|--------|
|SGM          |  4.989    |  36.22 |
|PSMNet       |  2.183    |  21.95 |
|GwcNet       |  2.265    |  22.80 |
|HMSMNet      |  2.040    |  19.00 |
|DLNR         |  1.864    |  16.56 |
|PCV          |  1.918    |  17.31 |
|Ours         |**1.739**  |**14.71**|

# Comparsion on US3D dataset
The best score for each metric is marked in **bold**.
|Method       |  EPE(Px)  |  D1(%) |
|-------------|-----------|--------|
|SGM          |  2.398    |  19.93 |
|PSMNet       |  1.499    |  9.22 |
|GwcNet       |  1.406    |  8.08 |
|HMSMNet      |  1.473    |  9.17 |
|DLNR         |  1.389    |  8.03 |
|PCV         |  1.488    |  9.46 |
|Ours         |**1.352**  |**7.67**|

## Test
Please download weight: https://pan.baidu.com/s/1AJEuKonLPkbojP7Pks4dxQ?pwd=9aja

Download and extract it, and place it in the root directory.

For WHU:
``` python evaluate_stereo.py --mode 16bit --max_disp 64 --min_disp -128 --test_left_dir WHU/left --test_right_dir WHU/right --test_disp_dir WHU/disp --test_save_path results/whu```
The results will be saved at "results/whu"

For US3D:
``` python evaluate_stereo.py --mode 8bit --max_disp 96 --min_disp -96 --test_left_dir US3D/left --test_right_dir US3D/right --test_disp_dir US3D/disp --test_save_path results/US3D```
The results will be saved at "results/US3D"

## Thank you！
