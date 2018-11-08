<h1> RSNA-Bone-Age-Prediction <a href = "https://www.kaggle.com/kmader/rsna-bone-age">↗</a></h1>
<p>Correctly identify the age of a child from an X-ray of their hand.</p>

<h3> Details </h3>
<p>This repo refers to Yichen Wang's work which refers to the framework by <a href = "http://ip.chinaz.com/"><b> Kevin Mader </b></a> who uses pre-trained VGG16 to extract the feature map of raw images. Attention network is used in the architecture, which is probably inspired by that only certain bones contribute to age prediction.</p>
<p> We further notice that the significance of bones differs in gender. Therefore, we add an auxiliary network whose input is gender to the original framework, which results in lower mean absolute deviation (MAD). </p> 
<p> We experimented the influence of different pre-trained models, convolution kernel size and gender feature size. The best combination is </p>
<ul type="circle">
  <li><b>VGG16</b></li>
  <li><b>Convolution kernel size = 3</b></li>
  <li><b>Gender feature size = 64</b></li>
</ul>

<h3> Requirements </h3>
<ul type="circle">
  <li>Keras</li>
  <li>sklearn</li>
  <li>panda</li>
  <li>numpy</li>
</ul>

<h3> Training </h3>
<p> Train the network using <b> python main.py </b>. </p>