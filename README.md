# Auto-detection of campus spot with sound recognition
Using digital signal as training data and build a deep learning model that is able to identify the campus spot through the background sound. The preprocessing skills of digital signal are performed to turn the pre-recorded sound to structured data in order to build to detecting model.

Main skills to use:
- Turning digital signal into structured data
- Building neural network model for time series prediction like LSTM, CNN

## Data source
  The project uses pre-recorded sound from three different spots in the campus, including gym, river side and bus stop. The sample rate and resolution is 44.1kHz and 24 Bit. At each spot, we recorded six-minutes sound with at different times of the day with condenser microphone.
<div>
<img src="https://github.com/mickeysun0104/Auto-detection-of-campus-spot-with-sound-recognition/blob/main/pics/246699610_l.jpg" width='40%' height='40%'/><img src='https://github.com/mickeysun0104/Auto-detection-of-campus-spot-with-sound-recognition/blob/main/pics/bus.jpg'>
</div>

## Preprocessing
  To convert digital signal into structured data, we present the feature of each spot with Mel-Frequency Cepstral Coefficient(MFCC). The lenth of each frame is 25ms, the number of samples between each window is 10ms and the dimension of features is 32.
  
## Model
  We use three differnet models to predict and compare the result of each model. Sine the digital signal is continuous, randomly spliting data is not apropriate. At the same time, our model need to be able to cosider the information from several frames. As a result, DNN, CNN and LSTM are models used in the project. A 5-fold corss validation is performed for tuning model. The structure of CNN and LSTM is shown below:
<div align='center'>
<img src="https://github.com/mickeysun0104/Auto-detection-of-campus-spot-with-sound-recognition/blob/main/pics/CNN.png" ><img src="https://github.com/mickeysun0104/Auto-detection-of-campus-spot-with-sound-recognition/blob/main/pics/LSTM.png" >
</div>

## Result
- LSTM has achieved the best performance with accuracy 0.98
- MFCC is effective of converting digital signal to structured data

