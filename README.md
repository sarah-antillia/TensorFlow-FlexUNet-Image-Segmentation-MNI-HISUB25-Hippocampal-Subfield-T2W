<h2>TensorFlow-FlexUNet-Image-Segmentation-MNI-HISUB25-Hippocampal-Subfield-T2W (2026/04/07)</h2>
Sarah T. Arai<br>
Software Laboratory antillia.com<br><br>
This is the first experiment of Image Segmentation for <b>MNI-HISUB25-T2W</b>
 based on 
our <a href="./src/TensorFlowFlexUNet.py">TensorFlowFlexUNet</a>
 (<b>TensorFlow Flexible UNet Image Segmentation Model for Multiclass</b>), and a 512x512 pixels PNG
 <a href="https://drive.google.com/file/d/1ImUGZWNXdlt8wj808SLrXIaOts7rGyf6/view?usp=sharing">
MNI-HISUB25-T2W-ImageMask-Dataset.zip</a> 
(<a href="https://creativecommons.org/licenses/by-nc-sa/3.0/legalcode.en">
CC BY-NC-SA 3.0</a>), which was derived by us from <br><br>
<a href="https://www.nitrc.org/projects/mni-hisub25">
<b>Multi-contrast and submillimetric 3-Tesla hippocampal subfield segmentation protocol and dataset (MNI-HISUB25)</b>
</a>
<br><br>
<hr>
<b>Actual Image Segmentation for MNI-HISUB25-T2W Images of 512x512 pixels</b><br>
As shown below, the inferred masks predicted by our segmentation model trained by the dataset appear similar to the 
ground truth masks.
<br><br>
<b>class_color_map ={Subiculum:blue, CA1-3:green, CA4-DG:red } </b>
<br><br>
<table>
<tr>
<th>Input: image</th>
<th>Mask (ground_truth)</th>
<th>Prediction: inferred_mask</th>
</tr>
<tr>
<td><img src="./projects/TensorFlowFlexUNet/MNI-HISUB25-T2W/mini_test/images/10002_123.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/MNI-HISUB25-T2W/mini_test/masks/10002_123.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/MNI-HISUB25-T2W/mini_test_output/10002_123.png" width="320" height="auto"></td>
</tr>

<tr>
<td><img src="./projects/TensorFlowFlexUNet/MNI-HISUB25-T2W/mini_test/images/10007_154.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/MNI-HISUB25-T2W/mini_test/masks/10007_154.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/MNI-HISUB25-T2W/mini_test_output/10007_154.png" width="320" height="auto"></td>
</tr>

<tr>
<td><img src="./projects/TensorFlowFlexUNet/MNI-HISUB25-T2W/mini_test/images/10008_178.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/MNI-HISUB25-T2W/mini_test/masks/10008_178.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/MNI-HISUB25-T2W/mini_test_output/10008_178.png" width="320" height="auto"></td>
</tr>
</table>
<hr>
<br>

<br>
<h3>1. Dataset Citation</h3>
The dataset used here was taken from <br><br>
<a href="https://www.nitrc.org/projects/mni-hisub25">
<b>Multi-contrast and submillimetric 3-Tesla hippocampal subfield segmentation protocol and dataset (MNI-HISUB25)</b>
</a>
<br><br>
The following explanation was taken from the above web site.
<br><br>
<b>About Dataset</b><br>
The MNI-HISUB25 dataset contains manual hippocampal subfield labels and associated high-resolution MRI 
data (submillimetric T1- and T2-weighted images, detailed sequence information, 
and stereotaxic probabilistic anatomical maps) based on 25 healthy subjects. <br>
Data were acquired on a 3-Tesla MRI system using a 32 phased-array head coil. <br><br>
The protocol divided the hippocampal formation into three subregions: <br>
<b>subicular complex, <br>
Cornu Ammonis 1, 2 and 3 (CA1-3),<br> 
and CA4-dentate gyrus (CA4-DG). <br>
</b>
<br>
Segmentation was guided by consistent intensity and morphology characteristics of the densely 
myelinated molecular layer together with few geometry-based boundaries flexible to overall mesiotemporal 
anatomy, and achieved excellent intra-/inter-rater reliability (Dice index ≥90/87%). <br>
The dataset can inform neuroimaging assessments of the mesiotemporal lobe and help to develop segmentation 
algorithms relevant for basic and clinical neurosciences.

<br><br>

<b>License</b><br>
<a href="https://creativecommons.org/licenses/by-nc-sa/3.0/legalcode.en">
Creative Commons Attribution-NonCommercial-ShareAlike 3.0 Unported (CC BY-NC-SA 3.0)
</a>
<br>
<br>
<h3>
<a id="2">
2 MNI-HISUB25-T2W ImageMask Dataset
</a>
</h3>
<h3>2.1 Download ImageMask Dataset</h3>
 If you would like to train this MNI-HISUB25-T2W Segmentation model by yourself,
 please download the dataset from the google drive  
 <a href="https://drive.google.com/file/d/1ImUGZWNXdlt8wj808SLrXIaOts7rGyf6/view?usp=sharing">
MNI-HISUB25-T2W-ImageMask-Dataset.zip</a> (
<a href="https://creativecommons.org/licenses/by-nc-sa/3.0/legalcode.en">
CC BY-NC-SA 3.0</a>)
, expand the downloaded ImageMaskDataset and put it under <b>./dataset</b> folder to be
<br>
<pre>
./dataset
└─MNI-HISUB25-T2W
    ├─test
    │   ├─images
    │   └─masks
    ├─train
    │   ├─images
    │   └─masks
    └─valid
        ├─images
        └─masks
</pre>
<br>
<b>MNI-HISUB25-T2W Statistics</b><br>
<img src ="./projects/TensorFlowFlexUNet/MNI-HISUB25-T2W/MNI-HISUB25-T2W_Statistics.png" width="512" height="auto"><br>
<br><br>
As shown above, the number of images of train and valid datasets is not so large to use for the
 training set of our segmentation model.
<br><br>
<h3>2.2 Derivation of MNI-HISUB25-T2W </h3>
The folder structure of the orginal mri_dataset of MNI-HISUB25 is the following.<br> 
<pre>
./mri_dataset
├─s01
│  ├─s01_hippolabels_hres_L_MNI.nii.gz
│  ├─s01_hippolabels_hres_R_MNI.nii.gz
│  ├─s01_hippolabels_t1w_standard_L_MNI.nii.gz
│  ├─s01_hippolabels_t1w_standard_R_MNI.nii.gz
│  ├─s01_t1w_hires_defaced_MNI.nii.gz
...
│  └─s01_t2w_hires_defaced_MNI.nii.gz

├─s02
...

└─s25
│  ├─s25_hippolabels_hres_L_MNI.nii.gz
│  ├─s25_hippolabels_hres_R_MNI.nii.gz
│  ├─s25_hippolabels_t1w_standard_L_MNI.nii.gz
│  ├─s25_hippolabels_t1w_standard_R_MNI.nii.gz
│  ├─s25_t1w_hires_defaced_MNI.nii.gz
...
│  └─s25_t2w_hires_defaced_MNI.nii.gz
...
</pre>
We used a simple Python script and the following class-color mapping table to generate our PNG dataset with colorized masks
from <b>s*_hippolabels_hres_L_MNI.nii.gz, s*_hippolabels_hres_R_MNI.nii.gz and s*_t2w_hires_defaced_MNI.nii.gz 
</b> NIfTI files.<br><br>
<table>
<tr><th>Index</th><th>Class</th><th>Color </th><th>RGB triplet</th></tr>
<tr>
<td>1</td><td>Subiculum</td><td>blue</td><td>(0,0,255)</td><tr>
<td>2</td><td>CA1-3</td><td>green</td><td>(0,255,0)</td><tr>
<td>3</td><td>A4-DG</td><td>red</td><td>(255,0,0)</td><tr>
</table>
<br>
<br>
<h3>2.3 Train Image and SmoothedMask Saｍples</h3>
<b>Train_images_sample</b><br>
<img src="./projects/TensorFlowFlexUNet/MNI-HISUB25-T2W/asset/train_images_sample.png" width="1024" height="auto">
<br>
<b>Train_masks_sample</b><br>
<img src="./projects/TensorFlowFlexUNet/MNI-HISUB25-T2W/asset/train_masks_sample.png" width="1024" height="auto">
<br>
<h3>
3 Train TensorFlowFlexUNet Model
</h3>
 We trained MNI-HISUB25-T2W TensorFlowFlexUNet Model by using the 
<a href="./projects/TensorFlowFlexUNet/MNI-HISUB25-T2W/train_eval_infer.config"> <b>train_eval_infer.config</b></a> file. <br>
Please move to ./projects/TensorFlowFlexUNet/MNI-HISUB25-T2W and run the following bat file.<br>
<pre>
>1.train.bat
</pre>
, which simply runs the following command.<br>
<pre>
>python ../../../src/TensorFlowFlexUNetTrainer.py ./train_eval_infer.config
</pre>
<hr>

<b>Model parameters</b><br>
Defined a small <b>base_filters = 16 </b> and large <b>base_kernels = (11,11)</b> for the first Conv Layer of Encoder Block of 
<a href="./src/TensorFlowFlexUNet.py">TensorFlowFlexUNet.py</a> 
and a large num_layers (including a bridge between Encoder and Decoder Blocks).
<pre>
[model]
;You may specify your own UNet class derived from our TensorFlowFlexModel
model         = "TensorFlowFlexUNet"
image_width    = 512
image_height   = 512
image_channels = 3
input_normalize = True
normalization  = False
num_classes    = 4
base_filters   = 16
base_kernels   = (11,11)
num_layers     = 8
dropout_rate   = 0.04
dilation       = (1,1)
</pre>
<b>Learning rate</b><br>
Defined a small learning rate.  
<pre>
[model]
learning_rate  = 0.00007
</pre>
<b>Loss and metrics functions</b><br>
Specified "categorical_crossentropy" and <a href="./src/dice_coef_multiclass.py">"dice_coef_multiclass"</a>.<br>
<pre>
[model]
loss           = "categorical_crossentropy"
metrics        = ["dice_coef_multiclass"]
</pre>
<b>Dataset class</b><br>
Specifed <a href="./src/ImageCategorizedMaskDataset.py">ImageCategorizedMaskDataset</a> class.<br>
<pre>
[dataset]
class_name    = "ImageCategorizedMaskDataset"
</pre>
<br>
<b>Learning rate reducer callback</b><br>
Enabled learing_rate_reducer callback, and a small reducer_patience.
<pre> 
[train]
learning_rate_reducer = True
reducer_factor     = 0.4
reducer_patience   = 4
</pre>
<b>Early stopping callback</b><br>
Enabled early stopping callback with patience parameter.
<pre>
[train]
patience      = 10
</pre>
<b>RGB Color map</b><br>
Specifed rgb color map dict for MNI-HISUB25-T2W 1+3 classes.<br>
<pre>
[mask]
mask_datatyoe    = "categorized"
mask_file_format = ".png"
;MNI-HISUB25-T2W rgb color map dict for 1+3 classes.
;                      Subiculum,  CA1-3,	CA4-DG
rgb_map = {(0,0,0):0, (0,0,255):1,(0,255,0):2,(255,0,0):3 }
</pre>
<b>Epoch change inference callback</b><br>
Enabled <a href="./src/EpochChangeInferencer.py">epoch_change_infer callback</a></b>.<br>
<pre>
[train]
epoch_change_infer       = True
epoch_change_infer_dir   =  "./epoch_change_infer"
num_infer_images         = 6
</pre>
By using this callback, on every epoch_change, the inference procedure can be called
 for 6 images in <b>mini_test</b> folder. This will help you confirm how the predicted mask changes 
 at each epoch during your training process.<br> 
<br> 
<!--
As shown below, early in the model training, the predicted masks from our UNet segmentation model showed 
discouraging results.
 However, as training progressed through the epochs, the predictions gradually improved. 
-->
 <br> 
<br>
<b>Epoch_change_inference output at starting (epoch 1,2,3)</b><br>
<img src="./projects/TensorFlowFlexUNet/MNI-HISUB25-T2W/asset/epoch_change_infer_at_start.png" width="1024" height="auto"><br>
<br>
<b>Epoch_change_inference output at middlepoint (epoch 31,32,33)</b><br>
<img src="./projects/TensorFlowFlexUNet/MNI-HISUB25-T2W/asset/epoch_change_infer_at_middle.png" width="1024" height="auto"><br>
<br>

<b>Epoch_change_inference output at ending (epoch 64,65,66)</b><br>
<img src="./projects/TensorFlowFlexUNet/MNI-HISUB25-T2W/asset/epoch_change_infer_at_end.png" width="1024" height="auto"><br>
<br>

In this experiment, the training process was stopped at epoch 66 by EarlyStopping callback.<br><br>
<img src="./projects/TensorFlowFlexUNet/MNI-HISUB25-T2W/asset/train_console_output_at_epoch66.png" width="1024" height="auto"><br>
<br>

<a href="./projects/TensorFlowFlexUNet/MNI-HISUB25-T2W/eval/train_metrics.csv">train_metrics.csv</a><br>
<img src="./projects/TensorFlowFlexUNet/MNI-HISUB25-T2W/eval/train_metrics.png" width="520" height="auto"><br>

<br>
<a href="./projects/TensorFlowFlexUNet/MNI-HISUB25-T2W/eval/train_losses.csv">train_losses.csv</a><br>
<img src="./projects/TensorFlowFlexUNet/MNI-HISUB25-T2W/eval/train_losses.png" width="520" height="auto"><br>
<br>
<h3>
4 Evaluation
</h3>
Please move to <b>./projects/TensorFlowFlexUNet/MNI-HISUB25-T2W</b> folder, 
and run the following bat file to evaluate TensorFlowUNet model for MNI-HISUB25-T2W.<br>
<pre>
./2.evaluate.bat
</pre>
This bat file simply runs the following command.
<pre>
python ../../../src/TensorFlowFlexUNetEvaluator.py ./train_eval_infer_aug.config
</pre>

Evaluation console output:<br>
<img src="./projects/TensorFlowFlexUNet/MNI-HISUB25-T2W/asset/evaluate_console_output_at_epoch66.png" width="1024" height="auto">
<br><br>Image-Segmentation-MNI-HISUB25-T2W

<a href="./projects/TensorFlowFlexUNet/MNI-HISUB25-T2W/evaluation.csv">evaluation.csv</a><br>
The loss (categorical_crossentropy) to this <b>MNI-HISUB25-T2W/test</b> was very low, and dice_coef_multiclass very high as shown below.
<br>
<pre>
categorical_crossentropy,0.0015
dice_coef_multiclass,0.9993
</pre>
<br>
<h3>
5 Inference
</h3>
Please move to a <b>./projects/TensorFlowFlexUNet/MNI-HISUB25-T2W</b> folder, and run the following bat file to infer segmentation regions for images by the Trained-TensorFlowUNet model for MNI-HISUB25-T2W.<br>
<pre>
./3.infer.bat
</pre>
This simply runs the following command.
<pre>
python ../../../src/TensorFlowFlexUNetInferencer.py ./train_eval_infer_aug.config
</pre>
<hr>
<b>mini_test_images</b><br>
<img src="./projects/TensorFlowFlexUNet/MNI-HISUB25-T2W/asset/mini_test_images.png" width="1024" height="auto"><br>
<b>mini_test_mask(ground_truth)</b><br>
<img src="./projects/TensorFlowFlexUNet/MNI-HISUB25-T2W/asset/mini_test_masks.png" width="1024" height="auto"><br>
<hr>
<b>Inferred test masks</b><br>
<img src="./projects/TensorFlowFlexUNet/MNI-HISUB25-T2W/asset/mini_test_output.png" width="1024" height="auto"><br>
<br>
<hr>
<b>Enlarged images and masks of MNI-HISUB25-T2W Images of 512x512 pixels</b><br>
As shown below, the inferred masks predicted by our segmentation model trained by the dataset appear similar to the
ground truth masks.
<br><br>
<b>class_color_map ={Subiculum:blue, CA1-3:green, CA4-DG:red } </b>
<br><br>
<table>
<tr>
<th>Image</th>
<th>Mask (ground_truth)</th>
<th>Inferred-mask</th>
</tr>
<tr>
<td><img src="./projects/TensorFlowFlexUNet/MNI-HISUB25-T2W/mini_test/images/10001_118.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/MNI-HISUB25-T2W/mini_test/masks/10001_118.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/MNI-HISUB25-T2W/mini_test_output/10001_118.png" width="320" height="auto"></td>
</tr>

<tr>
<td><img src="./projects/TensorFlowFlexUNet/MNI-HISUB25-T2W/mini_test/images/10002_180.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/MNI-HISUB25-T2W/mini_test/masks/10002_180.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/MNI-HISUB25-T2W/mini_test_output/10002_180.png" width="320" height="auto"></td>
</tr>

<tr>
<td><img src="./projects/TensorFlowFlexUNet/MNI-HISUB25-T2W/mini_test/images/10007_154.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/MNI-HISUB25-T2W/mini_test/masks/10007_154.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/MNI-HISUB25-T2W/mini_test_output/10007_154.png" width="320" height="auto"></td>
</tr>

<tr>
<td><img src="./projects/TensorFlowFlexUNet/MNI-HISUB25-T2W/mini_test/images/10017_159.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/MNI-HISUB25-T2W/mini_test/masks/10017_159.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/MNI-HISUB25-T2W/mini_test_output/10017_159.png" width="320" height="auto"></td>
</tr>

<tr>
<td><img src="./projects/TensorFlowFlexUNet/MNI-HISUB25-T2W/mini_test/images/10018_150.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/MNI-HISUB25-T2W/mini_test/masks/10018_150.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/MNI-HISUB25-T2W/mini_test_output/10018_150.png" width="320" height="auto"></td>
</tr>

<tr>
<td><img src="./projects/TensorFlowFlexUNet/MNI-HISUB25-T2W/mini_test/images/10020_112.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/MNI-HISUB25-T2W/mini_test/masks/10020_112.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/MNI-HISUB25-T2W/mini_test_output/10020_112.png" width="320" height="auto"></td>
</tr>
</table>
<hr>
<br>
<h3>
References
</h3>
<b>1. Multi-contrast submillimetric 3 Tesla hippocampal subfield segmentation protocol and dataset</b><br>
Jessie Kulaga-Yoskovitz, Boris C. Bernhardt, Seok-Jun Hong, Tommaso Mansi, Kevin E. Liang, <br>
Andre J.W. van der Kouwe, Jonathan Smallwood, Andrea Bernasconi & Neda Bernasconi<br>
<a href="https://www.nature.com/articles/sdata201559">https://www.nature.com/articles/sdata201559</a>
<br><br>
<b>2. A paired dataset of multi-modal MRI at 3 Tesla and 7 Tesla with manual hippocampal subfield segmentations</b><br>
Lei Chu, Baoqiang Ma, Xiaoxi Dong, Yirong He, Tongtong Che, Debin Zeng, Zihao Zhang & Shuyu Li<br>
<a href="https://www.nature.com/articles/s41597-025-04586-9?fromPaywallRec=false">
https://www.nature.com/articles/s41597-025-04586-9?fromPaywallRec=false</a>
<br><br>
<b>3. A novel deep learning based hippocampus subfield segmentation method</b><br>
JoséV. Manjón, José E. Romero & Pierrick Coupe<br>
<a href="https://www.nature.com/articles/s41598-022-05287-8.pdf">https://www.nature.com/articles/s41598-022-05287-8.pdf</a>
<br><br>
<b>4. DSnet: a new dual‑branch network for hippocampus subfield segmentation</b><br>
Hancan Zhu, Wangang Cheng, Keli Hu & Guanghua He<br>
<a href="https://www.researchgate.net/publication/381961150_DSnet_a_new_dual-branch_network_for_hippocampus_subfield_segmentation">
https://www.researchgate.net/publication/381961150_DSnet_a_new_dual-branch_network_for_hippocampus_subfield_segmentation</a>
<br><br>
<b>5. TensorFlow-FlexUNet-Image-Segmentation-Model</b><br>
Toshiyuki Arai <br>
<a href="https://github.com/sarah-antillia/TensorFlow-FlexUNet-Image-Segmentation-Model">
TensorFlow-FlexUNet-Image-Segmentation-Model
</a>
<br>
<br>
