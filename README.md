### [**SpectralTrack**](https://www.sciencedirect.com/science/article/)

The official implementation for "**Hyperspectral Video Tracking with Spectral-Spatial Fusion and Memory Enhancement**", IEEE Transactions on Image Processing, 2025.

--------------------------------------------------------------------------------------

:running:Keep updating:running:: We have released the code and result of SpectralTrack and SpectralTrack+.

--------------------------------------------------------------------------------------
- Authors:
[Yuzeng Chen](https://yzcu.github.io/),
[Qiangqiang Yuan](http://qqyuan.users.sgg.whu.edu.cn/),
[Hong Xie](http://hts.sgg.whu.edu.cn/teachers/44.html),
[Yuqi Tang](https://faculty.csu.edu.cn/yqtang/zh_CN/zdylm/66781/list/index.htm),
[Yi Xiao](https://github.com/XY-boy),
Jiang He,
Renxiang Guan,
[Xinwang Liu](https://xinwangliu.github.io/),
[Liangpei Zhang](http://www.lmars.whu.edu.cn/prof_web/zhangliangpei/rs/index.html),
--------------------------------------------------------------------------------------

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

## Usage
- Training: Download the RGB/Hyperspectral training/test datasets: [LaSOT](https://cis.temple.edu/lasot/), [GOT-10K](http://got-10k.aitestunion.com/downloads), [COCO](http://cocodataset.org), [HOTC](https://www.hsitracking.com/hot2022/), [MSSOT](https://github.com/Chenlulu1993/SMT), [MSVT](https://github.com/polwork/HOMG), and [TrackingNet](https://tracking-net.org/#downloads).
- Fast Training: Please download the [pre-trained model](https://pan.baidu.com)(code: yzcu) of SpectralTrack and SpectralTrack+'s. Please Put the pre-trained model into <pretrained_models>.
- Run <tracking/0train_SpectralTrack.py> and <tracking/0train_SpectralTrack+.py> to train SpectralTrack. SpectralTrack+--><tracking/0train_SpectralTrack+.py>
- The trained SpectralTrack model will be saved in <output/train/yzcu/yzcu/yzcu_ep0030.pth.tar>. SpectralTrack+--><output/train/yzcu/yzcu+/yzcu_ep0030.pth.tar>
- We have also released the trained [SpectralTrack](https://pan.baidu.com)(code: yzcu) and [SpectralTrack+](https://pan.baidu.com)(code: yzcu) tracking models.
- Testing: Run <tracking/1test_SpectralTrack+.py>. <tracking/1test_SpectralTrack+.py>--><output/results/yzcu/yzcu+>
- For evaluation, please download the evaluation benchmark [Toolkit](http://cvlab.hanyang.ac.kr/tracker_benchmark/) and [vlfeat](http://www.vlfeat.org/index.html) for more precision performance evaluation.
- Refer to [HOTC](https://www.hsitracking.com/hot2022/) for evaluation.
- Evaluation of the SpectralTrack and SpectralTrack+ tracker. Run `\tracker_benchmark_v1.0\perfPlot.m`
- Relevant tracking results are provided in `SpectralTrack and SpectralTrack+\tracking_results\hotc20test`.

:heart:  :heart:

## Contact
If you have any questions or suggestions, feel free to contact me.  
Email: yzchen1006@163.com

:heart:  :heart: We sincerely appreciate the insightful feedback provided by the editors and reviewers. :heart:  :heart:

