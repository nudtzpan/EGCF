This is the code for our paper in Sensors: [Efficient Graph Collaborative Filtering via Contrastive Learning](https://www.mdpi.com/1424-8220/21/14/4666).

## Environment Requirement

The code runs well under python 3.7.7. The required packages are as follows:

- Tensorflow-gpu == 1.15.0
- numpy == 1.19.1
- scipy == 1.5.2
- pandas == 1.1.1
- cython == 0.29.21

## Quick Start
**Firstly**, compline the evaluator of cpp implementation with the following command line:

```bash
python setup.py build_ext --inplace
```

If the compilation is successful, the evaluator of cpp implementation will be called automatically.
Otherwise, the evaluator of python implementation will be called.

**Note that the cpp implementation is much faster than python.**

Further details, please refer to [NeuRec](https://github.com/wubinzzu/NeuRec/)

**Secondly**, specify dataset and recommender in configuration file *NeuRec.properties*.

Model specific hyperparameters are in configuration file *./conf/SGL.properties*.

Some important hyperparameters:

### yelp2018 dataset
```
ssl_lambda=8
ssl_reg=0.05
```

### amazon-book dataset
```
ssl_lambda=8
ssl_reg=0.05
```

**Finally**, run [main.py](./main.py) in IDE or with command line:

```bash
python main.py
```
