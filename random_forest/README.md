# Train a random forest model to classify seqeunces
##### Consists of 2 notebooks
1. RF_prepare_data.ipynb - for preparing data for the random forest training or use.
2. RF_train.ipynb - train a 2 step random forest model using the prepared data.

This notebook uses the [LightGBM](https://lightgbm.readthedocs.io) package.

in order to use these files, you dirst need to extract them, using
cat NGS_w_entire_sequence_space.tar.gz.* | tar xzvf -
cat sequence_space_annotated.tar.gz.* | tar xzvf -
