## 🖼Results
 - ### 
 ![image](/file/5.jpg)
 # SpectralTrack 
##  UPDATING ~ The PyTorch Implementation for [SpectralTrack and SpectralTrack+](https://www.sciencedirect.com/science/article/pii/S0924271624000856).
- ♪ Hopefully something good will happen for all of us ♪
<!---
- Red --> Our SpectralTrack and SpectralTrack+. Blue --> Ground Truth. The Rest --> Compared Arts
<!---
- ![image](/fig/duck.gif)
- ![image](/fig/leaf.gif)
- ![image](/fig/rain.gif)
-->
<!---
--------------------------------------------------------------------------------------
:running:Keep Updating:running:: More detailed tracking results for SpectralTrack and SpectralTrack+ have been released.
| Benchmark (Metrics)          | SpectralTrack and SpectralTrack+          | Results                                                                   |
| ---------------------------- | --------------- | ------------------------------------------------------------------------- |
| [HOTC20test](https://www.hsitracking.com/) (Pre / Suc)       |  0.971 / 0.758  | https://github.com/YZCU/SpectralTrack and SpectralTrack+/tree/main/tracking_results/hotc2020        |
| [HOTC23val_NIR](https://www.hsitracking.com/) (Pre / Suc)    |  0.947 / 0.754  | https://github.com/YZCU/SpectralTrack and SpectralTrack+/tree/main/tracking_results/hotc2023_nir    |
| [HOTC23val_RedNIR](https://www.hsitracking.com/) (Pre / Suc) |  0.755 / 0.613  | https://github.com/YZCU/SpectralTrack and SpectralTrack+/tree/main/tracking_results/hotc2023_rednir |
| [HOTC23val_VIS](https://www.hsitracking.com/) (Pre / Suc)    |  0.915 / 0.720  | https://github.com/YZCU/SpectralTrack and SpectralTrack+/tree/main/tracking_results/hotc2023_vis    |
| [HOTC24val_NIR](https://www.hsitracking.com/) (Pre / Suc)    |  0.949 / 0.763  | https://github.com/YZCU/SpectralTrack and SpectralTrack+/tree/main/tracking_results/hotc2024_nir    |
| [HOTC24val_RedNIR](https://www.hsitracking.com/) (Pre / Suc) |  0.750 / 0.581  | https://github.com/YZCU/SpectralTrack and SpectralTrack+/tree/main/tracking_results/hotc2024_rednir |
| [HOTC24val_VIS](https://www.hsitracking.com/) (Pre / Suc)    |  0.721 / 0.561  | https://github.com/YZCU/SpectralTrack and SpectralTrack+/tree/main/tracking_results/hotc2024_vis    |
| [MSSOT](https://www.sciencedirect.com/science/article/pii/S0924271623002551) (Pre / Suc)            |  0.857 / 0.602  | https://github.com/YZCU/SpectralTrack and SpectralTrack+/tree/main/tracking_results/mssot           |
| [MSVT](https://www.sciencedirect.com/science/article/pii/S0924271621002860) (Pre / Suc)             |  0.967 / 0.754  | https://github.com/YZCU/SpectralTrack and SpectralTrack+/tree/main/tracking_results/msvt            |
-->
--------------------------------------------------------------------------------------

##  Install
```
git clone https://github.com/YZCU/SpectralTrack and SpectralTrack+.git
```
## Environment
 > * CUDA 11.8
 > * Python 3.9.18
 > * PyTorch 2.0.0
 > * Torchvision 0.15.0
 > * numpy 1.25.0 
 - Please check the `requirement.txt` for more env details.

## Usage
- Download the RGB/Hyperspectral training/test datasets: [LaSOT](https://cis.temple.edu/lasot/), [GOT-10K](http://got-10k.aitestunion.com/downloads), [COCO](http://cocodataset.org), [HOTC](https://www.hsitracking.com/hot2022/), [MSSOT](https://github.com/Chenlulu1993/SMT), [MSVT](https://github.com/polwork/HOMG), and [TrackingNet](https://tracking-net.org/#downloads).
- Please train the SpectralTrack and SpectralTrack+'s [foundation model~updating](https://pan.baidu.com) (code: SpectralTrack and SpectralTrack+) on the LaSOT, GOT-10K, COCO, and TrackingNet datasets.
- We will release the well-trained model of [SpectralTrack and SpectralTrack+~updating](https://pan.baidu.com/) (code: SpectralTrack and SpectralTrack+).
- The generated model will be saved to the path of `output/train/SpectralTrack and SpectralTrack+/SpectralTrack and SpectralTrack+_model/`.
- Please test the model. The results will be saved in the path of `output/results/SpectralTrack and SpectralTrack+/`.
- For evaluation, please download the evaluation benchmark [Toolkit](http://cvlab.hanyang.ac.kr/tracker_benchmark/) and [vlfeat](http://www.vlfeat.org/index.html) for more precision performance evaluation.
- Refer to [HOTC](https://www.hsitracking.com/hot2022/) for evaluation.
- Evaluation of the SpectralTrack and SpectralTrack+ tracker. Run `\tracker_benchmark_v1.0\perfPlot.m`
- Relevant tracking results are provided in `SpectralTrack and SpectralTrack+\tracking_results\hotc20test`. More evaluation results are provided in a `SpectralTrack and SpectralTrack+\tracking_results`.
<!---
## Results
- Performance evaluation with hyperspectral arts on the HOTC20’s hyperspectral modality. (a) Precision plot. (b) Success plot.
 ![image](/fig/hotc20.jpg)

- Accuracy-speed trade-off of SOTA hyperspectral arts on the HOTC20 benchmark.
 ![image](/fig/fps.jpg)

-  Subfigures (a) through (f) represent precision plots for NIR23, RedNIR23, VIS23, NIR24, RedNIR24, and VIS24 benchmarks, respectively, while (g) through (l) illustrate corresponding success plots across the same benchmarks.
 ![image](/fig/hotc23-24.jpg)

- Performance evaluation with hyperspectral arts and RGB arts on the MSSOT benchmark. (a) Precision plot. (b) Success plot.
 ![image](/fig/mssot.jpg)

- Performance evaluation with hyperspectral arts and RGB arts on the MSVT benchmark. (a) Precision plot. (b) Success plot. 
 ![image](/fig/msvt.jpg)

- Comprehensive attribute-level and overall success plots of hyperspectral arts and RGB arts on the MSVT benchmark. 
 ![image](/fig/msvt_attr.jpg)

- Visual comparisons, arranged from top to bottom, covering a diverse set of benchmarks: HOTC20 (toy2), VIS23 (cards16), NIR24 (rider14), RedNIR24 (rainystreet12), VIS24 (heartsurgery2), MSSOT (car-16), and MSVT (triple).
 ![image](/fig/vis.jpg)

- Overlap curves and tracking samples of SpectralTrack and SpectralTrack+ are presented in various complex scenarios.
 ![image](/fig/curve.jpg)
-->

:heart:  :heart:

## Contact
If you have any questions or suggestions, feel free to contact me.  
Email: yuzeng_chen@whu.edu.cn 

:heart:  :heart: We sincerely appreciate the insightful feedback provided by the editors and reviewers. :heart:  :heart:

