<p align="center">
<img src="files/hand.png" class="centerImage" height="300" width="300"  />
</p>
<br/>

In the present repository you can find the source code of the Attention! A Lightweight 2D Hand Pose Estimation Approach paper
<br/>
<br/>
<br/>
# Abstract
---
<p align="center">
</p>
 Vision based human pose estimation is an non-invasive technology for human-computer interaction (HCI). Direct use of the hand as an input device provides an attractive interaction method, with minimum need for specialized equipment, such as exoskeletons, gloves etc, but a camera and a processing platform. Various applications exploit algorithms which have the capability of estimating a hand's pose. Such applications include control of robotics systems, video games, computer-generated imagery (CGI) etc. In this letter, we present a novel Convolutional Neural Network architecture, reinforced with a Self-Attention module that it could be deployed on an embedded system, due to its lightweight nature, with just <B><i>1,9 Million</i></B> parameters.


<br />
<p align="center">
<a href="https://ieeexplore.ieee.org/abstract/document/9171866" ><font size="10">[Paper] </font></a>
<p>
<br />
<br />

# Method Overview
---
<p align="center">

The presented architecture is based on the very successful
idea of DenseNets. In a DenseNet, each layer obtains
additional inputs from all preceding ones and propagates its
own feature-maps to all subsequent layers, by a channel-wise
concatenation.
 </div>
<p>
<br />
<p align="center">
<img src="files/densenet.png" class="centerImage" height="140" width="600"  />
<p>
<p align="center">
<figcaption>Dense Block with growth rate <i>k</i></figcaption>
<p>
<br />

<p align="center">

We implement the <i>inverted bottleneck block</i>,
enhanced by an <i>Attention Augmented Convolutional layer</i>,
which output is added to the product of the Depthwise Separable Convolutional layer, as shown to the following figure.

<p>

<br />
<p align="center">
<img src="files/aaib.png" class="centerImage" height="220" width="280"  />
 <figcaption>Attention Augmented Inverted Bottleneck Layer</figcaption>
<p>
<br />

# Results
---
<p align="center">
<center>
<div class="masonry">
  <img src="files/pck.png" width="32%"  alt>
  <img src="files/pck_h.png" width="32%" alt>
  <img src="files/pck_all.png" width="32%"  alt>
</div>
</center>


<br />
<br />
<br />

<table class="tg" align='center'>
  <tr>
    <th class="tg-c3ow" rowspan="2"></th>
    <th class="tg-9wq8" rowspan="2">AUC</th>
    <th class="tg-c3ow" colspan="2">EPE (px)</th>
  </tr>
  <tr>
    <td class="tg-c3ow">Mean</td>
    <td class="tg-c3ow">Median</td>
  </tr>
  <tr>
    <td class="tg-7btt" colspan="4">MPII+NZSL Dataset</td>
  </tr>
  <tr>
    <td class="tg-c3ow">Zimm. et al. (ICCV 2017)</td>
    <td class="tg-c3ow">0.17</td>
    <td class="tg-c3ow">59.4</td>
    <td class="tg-c3ow">-</td>
  </tr>
  <tr>
    <td class="tg-c3ow">Bouk. et al. (CVPR 2019)<br></td>
    <td class="tg-c3ow">0.50</td>
    <td class="tg-c3ow">18.95</td>
    <td class="tg-c3ow">-</td>
  </tr>
  <tr>
    <td class="tg-c3ow">Ours<br></td>
    <td class="tg-7btt">0.55</td>
    <td class="tg-7btt">16.1</td>
    <td class="tg-7btt">11</td>
  </tr>
  <tr>
    <td class="tg-7btt" colspan="4">LSMV Dataset</td>
  </tr>
  <tr>
    <td class="tg-c3ow">Gomez-Donoso et al.</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">10</td>
    <td class="tg-c3ow">-</td>
  </tr>
  <tr>
    <td class="tg-c3ow">Li et al.</td>
    <td class="tg-c3ow">-</td>
    <td class="tg-c3ow">8</td>
    <td class="tg-c3ow">-</td>
  </tr>
  <tr>
    <td class="tg-wh93">Ours</td>
    <td class="tg-o57c">0.89</td>
    <td class="tg-wh93">3.3</td>
    <td class="tg-o57c">2.5</td>
  </tr>
  <tr>
    <td class="tg-7btt" colspan="4">Stereo Hand Pose Dataset</td>
  </tr>
  <tr>
    <td class="tg-c3ow">Zimm et al. (ICCV 2017)</td>
    <td class="tg-c3ow">0.81</td>
    <td class="tg-c3ow">5</td>
    <td class="tg-c3ow">5.5</td>
  </tr>
  <tr>
    <td class="tg-7btt">Ours</td>
    <td class="tg-7btt">0.92</td>
    <td class="tg-7btt">2.2</td>
    <td class="tg-7btt">1.8</td>
  </tr>
  <tr>
    <td class="tg-7btt" colspan="4">FreiHand Dataset</td>
  </tr>
  <tr>
    <td class="tg-c3ow">Ours</td>
    <td class="tg-c3ow">0.87</td>
    <td class="tg-c3ow">4</td>
    <td class="tg-c3ow">3.1</td>
  </tr>
</table>

<br />
<br />


<table class="tg">
<thead>
  <tr>
    <th class="tg-c3ow"></th>
    <th class="tg-7btt">Arch 1</th>
    <th class="tg-7btt">Arch 2</th>
    <th class="tg-7btt">Arch 3</th>
    <th class="tg-7btt">Arch 4</th>
    <th class="tg-7btt">Arch 5</th>
    <th class="tg-7btt">Arch 6</th>
    <th class="tg-7btt">Arch 7</th>
    <th class="tg-7btt">Arch 8</th>
    <th class="tg-7btt">Arch 9</th>
    <th class="tg-7btt">Arch 10</th>
    <th class="tg-7btt">Arch 11</th>
    <th class="tg-7btt">Arch 12</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-mqa1">Attention module</td>
    <td class="tg-wp8o">*</td>
    <td class="tg-wp8o">-</td>
    <td class="tg-wp8o">-</td>
    <td class="tg-wp8o">*</td>
    <td class="tg-wp8o">*</td>
    <td class="tg-wp8o">-</td>
    <td class="tg-wp8o">*</td>
    <td class="tg-wp8o">-</td>
    <td class="tg-wp8o">-</td>
    <td class="tg-wp8o">*</td>
    <td class="tg-wp8o">-</td>
    <td class="tg-wp8o">*</td>
  </tr>
  <tr>
    <td class="tg-mqa1">Pooling Method</td>
    <td class="tg-wp8o">Blur</td>
    <td class="tg-wp8o">Blur</td>
    <td class="tg-wp8o">Average</td>
    <td class="tg-wp8o">Average</td>
    <td class="tg-wp8o">Blur</td>
    <td class="tg-wp8o">Average</td>
    <td class="tg-wp8o">Average</td>
    <td class="tg-wp8o">Blur</td>
    <td class="tg-wp8o">Max</td>
    <td class="tg-wp8o">Max</td>
    <td class="tg-wp8o">Max</td>
    <td class="tg-wp8o">Max</td>
  </tr>
  <tr>
    <td class="tg-7btt">Activation Function</td>
    <td class="tg-c3ow">Mish</td>
    <td class="tg-c3ow">Mish</td>
    <td class="tg-c3ow">Mish</td>
    <td class="tg-c3ow">Mish</td>
    <td class="tg-c3ow">ReLU</td>
    <td class="tg-c3ow">ReLU</td>
    <td class="tg-c3ow">ReLU</td>
    <td class="tg-c3ow">ReLU</td>
    <td class="tg-c3ow">Mish</td>
    <td class="tg-c3ow">Mish</td>
    <td class="tg-c3ow">ReLU</td>
    <td class="tg-c3ow">ReLU</td>
  </tr>
</tbody>
</table>
<br />
<br />
<center>
<div class="masonry">
<img src="files/radars/MPII+NZSL_Dataset.png" width="24%" alt>
<img src="files/radars/FreiHand_Dataset.png" width="24%" alt>
<img src="files/radars/LSMV_Dataset.png" width="24%" alt>
<img src="files/radars/SHP_Dataset.png" width="24%" alt>

</div>
</center>
<br />


<center>
<div class="masonry">
<img src="files/radars/t_MPII+NZSL_Dataset.png" width="24%" alt>
<img src="files/radars/t_FreiHand_Dataset.png" width="24%" alt>
<img src="files/radars/t_LSMV_Dataset.png" width="24%" alt>
<img src="files/radars/t_SHP_Dataset.png" width="24%" alt>

</div>
</center>
<p>

<br />
<br />

# Citation
---
If you find this paper useful in your research, please consider citing:

	@article{
          author={N. {Santavas} and I. {Kansizoglou} and L. {Bampis} and E. {Karakasis} and A. {Gasteratos}},
          journal={IEEE Sensors Journal},
          title={Attention! A Lightweight 2D Hand Pose Estimation Approach},
          year={2020},


