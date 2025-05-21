--------------------------------------------------------------------------------------
### [**SpectralTrack**](https://ieeexplore.ieee.org/document/11007172)

- The official implementation for "**Hyperspectral Video Tracking with Spectral-Spatial Fusion and Memory Enhancement**".
- IEEE Transactions on Image Processing, 2025.

--------------------------------------------------------------------------------------

:running:Keep updating:running::
- Trained models of [SpectralTrack](https://drive.google.com/drive/folders/189muRTkQTzAKM3JQHnh3_FzOqytvmz5d?hl=zh-cn) and [SpectralTrack+](https://drive.google.com/drive/folders/189muRTkQTzAKM3JQHnh3_FzOqytvmz5d?hl=zh-cn) have been released.
- Training and testing codes of [SpectralTrack](https://github.com/YZCU/SpectralTrack/blob/main/training%20and%20testing%20codes%20of%20SpectralTrack%20and%20SpectralTrack%2B.zip) and [SpectralTrack+](https://github.com/YZCU/SpectralTrack/blob/main/training%20and%20testing%20codes%20of%20SpectralTrack%20and%20SpectralTrack%2B.zip) have been released.
- Tracking results of [SpectralTrack](https://github.com/YZCU/SpectralTrack/blob/main/rect_results%20of%20SpectralTrack%20and%20SpectralTrack%2B.zip) and [SpectralTrack+](https://github.com/YZCU/SpectralTrack/blob/main/rect_results%20of%20SpectralTrack%20and%20SpectralTrack%2B.zip) have been released.
--------------------------------------------------------------------------------------
| Benchmark                                 | SpectralTrack (Pre/Suc) | SpectralTrack+ (Pre/Suc)|
| ------------------------------            | -------------------     | -------------------     |
| [HOTC20](https://www.hsitracking.com/)   |0.954 / 0.727 | 0.954 / 0.728 |
| [NIR23](https://www.hsitracking.com/)    |0.918 / 0.715 | 0.940 / 0.743 |
| [RedNIR23](https://www.hsitracking.com/) |0.691 / 0.563 | 0.747 / 0.607 |
| [VIS23](https://www.hsitracking.com/)    |0.883 / 0.681 | 0.901 / 0.695 |
| [NIR24](https://www.hsitracking.com/)    |0.937 / 0.750 | 0.938 / 0.763 |
| [RedNIR24](https://www.hsitracking.com/) |0.705 / 0.539 | 0.692 / 0.531 |
| [VIS24](https://www.hsitracking.com/)    |0.726 / 0.575 | 0.711 / 0.551 |
| [MSSOT](https://www.sciencedirect.com/science/article/pii/S0924271623002551) |0.845 / 0.560 | 0.805 / 0.545 |
| [MSVT](https://www.sciencedirect.com/science/article/pii/S0924271621002860)  |0.975 / 0.748 | 0.963 / 0.737 |

--------------------------------------------------------------------------------------
<!--
- Authors:
[Yuzeng Chen](https://yzcu.github.io/),
[Qiangqiang Yuan](http://qqyuan.users.sgg.whu.edu.cn/),
[Hong Xie](http://hts.sgg.whu.edu.cn/teachers/44.html),
[Yuqi Tang](https://faculty.csu.edu.cn/yqtang/zh_CN/zdylm/66781/list/index.htm),
[Yi Xiao](https://github.com/XY-boy),
Jiang He,
Renxiang Guan,
[Xinwang Liu](https://xinwangliu.github.io/),
[Liangpei Zhang](http://www.lmars.whu.edu.cn/prof_web/zhangliangpei/rs/index.html).
--------------------------------------------------------------------------------------
-->

<!--
[LaSOT](https://cis.temple.edu/lasot/), [GOT-10K](http://got-10k.aitestunion.com/downloads), [COCO](http://cocodataset.org), [HOTC](https://www.hsitracking.com/hot2022/), [MSSOT](https://github.com/Chenlulu1993/SMT), [MSVT](https://github.com/polwork/HOMG), and [TrackingNet](https://tracking-net.org/#downloads).
-->

##  Install
```
git clone https://github.com/YZCU/SpectralTrack.git
```

## Environment
 > * CUDA 11.8
 > * Python 3.9.18
 > * PyTorch 2.0.0
 > * Torchvision 0.15.0
 > * numpy 1.25.0 
--------------------------------------------------------------------------------------
## Usage
- Training: Please download the hyperspectral training and testing sets: [HOTC20](https://www.hsitracking.com/hot2022/), [HOTC23](https://www.hsitracking.com/hot2022/), [HOTC24](https://www.hsitracking.com/hot2022/), [MSSOT](https://github.com/Chenlulu1993/SMT), [MSVT](https://github.com/polwork/HOMG). 

- Fast Training: Download the [pre-trained model](https://drive.google.com/drive/folders/189muRTkQTzAKM3JQHnh3_FzOqytvmz5d?hl=zh-cn) of SpectralTrack and SpectralTrack+. Put it into `<pretrained_models>`.
- Run `<tracking/0train_SpectralTrack.py>` and `<tracking/0train_SpectralTrack+.py>` to train SpectralTrack and SpectralTrack+, respectively.
- The well-trained SpectralTrack model is put into `<output/train/yzcu/yzcu/yzcu_ep0030.pth.tar>`. SpectralTrack+-->`<output/train/yzcu/yzcu+/yzcu_ep0030.pth.tar>`.
- We have also released the well-trained [SpectralTrack](https://drive.google.com/drive/folders/189muRTkQTzAKM3JQHnh3_FzOqytvmz5d?hl=zh-cn) and [SpectralTrack+](https://drive.google.com/drive/folders/189muRTkQTzAKM3JQHnh3_FzOqytvmz5d?hl=zh-cn) tracking models.
- Testing: Run `<tracking/1test_SpectralTrack+.py>` for testing, and results are saved in `<output/results/yzcu/yzcu>`. `<tracking/1test_SpectralTrack+.py>`-->`<output/results/yzcu/yzcu+>`.
- Evaluating: Please download the evaluation benchmark [Toolkit](http://cvlab.hanyang.ac.kr/tracker_benchmark/) and [vlfeat](http://www.vlfeat.org/index.html) for more accurate evaluation.
- Refer to the [Hyperspectral Object Tracking Challenge](https://www.hsitracking.com/hot2022/) for detailed evaluations.
- Evaluation of the SpectralTrack and SpectralTrack+ tracker. Run `<tracker_benchmark_v1.0\perfPlot.m>`
--------------------------------------------------------------------------------------

## Citation
- If you find our work helpful in your research, kindly consider citing it. We appreciate your support！
```
@ARTICLE{11007172,
  author={Chen, Yuzeng and Yuan, Qiangqiang and Xie, Hong and Tang, Yuqi and Xiao, Yi and He, Jiang and Guan, Renxiang and Liu, Xinwang and Zhang, Liangpei},
  journal={IEEE Transactions on Image Processing}, 
  title={Hyperspectral Video Tracking with Spectral-Spatial Fusion and Memory Enhancement}, 
  year={2025},
  volume={},
  number={},
  pages={1-1},
  keywords={Feature extraction;Hyperspectral imaging;Photonic band gap;Foundation models;Visualization;Video tracking;Tracking;Training;Transformers;Imaging;Hyperspectral video tracking;Multi-modal video tracking;Parameter-efficient fine-tuning},
  doi={10.1109/TIP.2025.3569479}}

```
--------------------------------------------------------------------------------------

## Contact
- If you have any questions or suggestions, feel free to contact me.  
- Email: yzchen1006@163.com

:heart:  :heart: We sincerely appreciate the insightful feedback provided by Editors and Reviewers. :heart:  :heart:

--------------------------------------------------------------------------------------
