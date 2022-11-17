# Train a random forest model to classify seqeunces
##### Consists of 2 notebooks
1. RF_prepare_data.ipynb - for preparing data for the random forest training or use.
2. RF_train.ipynb - train a 2 step random forest model using the prepared data.

This notebook uses the [LightGBM](https://lightgbm.readthedocs.io) package.

In order to use these files, you first need to extract them, using
```
cat NGS_w_entire_sequence_space.tar.gz.* | tar xzvf -
cat sequence_space_annotated.tar.gz.* | tar xzvf -
tar xzvf *.gz
```

These notebooks require the following packages to run:
- lightgbm (3.2.1)
- matplotlib (3.1.1)
- numpy (1.20.2)
- pandas (1.2.3)
- seaborn (0.11.1)
- sklearn (0.0)
- tqdm (4.59.0)
