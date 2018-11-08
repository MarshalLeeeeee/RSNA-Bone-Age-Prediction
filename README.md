<h1> RSNA-Bone-Age-Prediction </h1>
<p>Correctly identify the age of a child from an X-ray of their hand.</p>

<h3> Details </h3>
<p>This repo refers to Yichen Wang's work which refers to the framework by <a href = "http://ip.chinaz.com/"><b> Kevin Mader </b></a> who uses pre-trained VGG16 to extract the feature map of raw images. Attention network is used in the architecture, which is probably inspired by that only certain bones contribute to age prediction.</p>
<p> We further notice that the significance of bones differs in gender. Therefore, we add an auxiliary network whose input is gender to the original framework, which results in lower mean absolute deviation (MAD). </p> 
<p> We experimented the influence of different pre-trained models, convolution kernel size and gender feature size. <b> VGG16 + convolution kernel size = 1 + gender feature size = 64 </b> is the best combination. </p>

<h3> Requirements </h3>
- keras
- pandas
- numpy

<h3> Training </h3>
<p> Train the network