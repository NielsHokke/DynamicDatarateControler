# DynamicDatarateControler

Project to write own datarate control algorithm for IEEE 802.11 (automatic selection of rate and coding scheme)

## Paper
[Cognitive WI-FI: A small step towards online self-learning data rate control](https://github.com/NielsHokke/DynamicDatarateControler/blob/master/Cognitive%20WI-FI%20A%20small%20step%20towards%20online%20self-learning%20data%20rate%20control.pdf)

## Getting Started

### Prerequisites

#### Matlab

* [Matlab WLAN System Toolbox ](https://nl.mathworks.com/products/wlan-system.html)

### Running

#### Matlab

* Adjust Rate Control Algorithm Parameters in Dynamic_data_rate.m:
```
ForceLearning = 0;     % When setting this to 1 and number of packets to multiples of 1000 it will performred a forced learning
SNRBinSize = 1;        % SNR binsize in dB
AdaptionRate = 1/3;    % How big the ifnluence of the new rate should be. 0 = not 1 = directly
LearningSpeed = 0.01;  % Percentage of time the algorithm will try another value then the know best
```
* Run code
* Run the next line to reset. If not run, code will remember previous learned data.
```
LearnedValues = ones( 10, (MaxSNR/SNRBinSize)+1)*-1;
```

## Results

![Results](https://raw.githubusercontent.com/NielsHokke/DynamicDatarateControler/master/Capture.PNG)

## Authors

* **Niels Hokke** - [NielsHokke](https://github.com/NielsHokke)
* **Jetse Brouwer** - [JetseBrouwer](https://github.com/JetseBrouwer)



