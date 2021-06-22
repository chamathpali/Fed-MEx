# Fed-MEx 🏃‍♂️
**Fed-MEx is the Federated Version** of the MEx Human Activity Recognition dataset. Pressure mat subset is used in this dataset.

[MEx](https://archive.ics.uci.edu/ml/datasets/MEx) is a publicly available exercise recognition dataset collected with 30 subjects performing 7 different physiotherapy exercises. The MEx dataset has 934 data samples from the pressure mat subset of the MEx dataset. Each client has a random amount of samples for only 2 exercise classes. A pressure mat data sample contains a sequence of heat maps (size 5 x 16 x 16) recorded for 5 seconds with 1Hz frequency. 
MEx has previously been used for personalised activity recognition research(1) and forms an interesting contrast to the other image and text datasets.

## Setup
To generate the dataset use the ```pm``` folder from the downloaded [MEx](https://archive.ics.uci.edu/ml/datasets/MEx) dataset and copy it to the root directory.

## Usage
This dataset is compatible with the [FedProx](https://github.com/litian96/FedProx), FedSim implemenations. If you are using the same experiment setup simply add the following into the main.py,

```python
DATASETS = [....., 'mex']

MODEL_PARAMS = {
    ..... , 
    'mex.mclr': (7,), 
    'mex.cnn': (7,), 
}

```

Reference models are availble in the FedSim implementation here.

#### MEx References

1 - WIJEKOON, A., WIRATUNGA, N., COOPER, K. and BACH, K. 2020. Learning to recognise exercises for the self-management of low back pain. In Barták, R. and Bell, E. (eds.). Proceedings of the 33rd International Florida Artificial Intelligence Research Society (FLAIRS) 2020 conference (FLAIRS-33), 17-20 May 2020, Miami Beach, USA. Palo Alto: AAAI Press [online], pages 347-352. 

[UCI ML Repository](https://archive.ics.uci.edu/ml/datasets/MEx)

[GitHub](https://github.com/anjanaw/mex)
