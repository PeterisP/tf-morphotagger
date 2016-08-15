# tf-morphotagger

Tensorflow based morphological tagger experiment for Latvian

Appendix to the paper "Deep neural learning approaches for Latvian morphological tagging" at [Baltic HLT](http://hlt2016.tilde.eu/)

# Prerequisites
python 3
tensorflow (0.10 was used)
numpy and gensim libraries
jypyter

Download the [wordform embeddings](https://dl.dropboxusercontent.com/u/9455117/lvnews2.c0p0d0.shuf.txt.we216-200-ssg-w5-m10.20160516233643.bin) and place in the embeddings/ folder - they are necessary to fully replicate the main result, but can be disabled in experiment parameters (input_features['wordform_embeddings']=False).

# Experiment replication
Launch the jupyter platform (e.g. "nohup jupyter notebook &")

Open the notebook tagger.ipynb and run all the cells in order.
The training data is included, but training the default network for 20 epochs takes 1 hour 40 minutes on a TitanX GPU.

The default configuration is for the full system described in the paper. Additional parameters can be configured in the initial parts of the notebook.
Layout of the network inner layers are currently defined in code function _prepare_graph() and can be altered there, I may make it more configurable later.
