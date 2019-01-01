# VGGFace2AgeLabel

Add age label to VGGFace2 Dataset from IMDB pretrained model

## Requirement

Python2.7/3.0

Caffe

## Estimated Metadata

`identity_meta_with_estimated_age.csv`

## Estimation Tutorial

### Download pretrained model

Download Caffemodel

`python download_model.py`

This script download age estimation model created from IMDB

https://data.vision.ee.ethz.ch/cvl/rrothe/imdb-wiki/

Caffemodel : https://data.vision.ee.ethz.ch/cvl/rrothe/imdb-wiki/static/dex_imdb_wiki.caffemodel

Prototxt : https://data.vision.ee.ethz.ch/cvl/rrothe/imdb-wiki/static/age.prototxt

### Download dataset

Download vggface2_test.tar.gz and vggface2_train.tar.gz and identity_meta.csv

http://www.robots.ox.ac.uk/~vgg/data/vgg_face2/

identity_meta.csv includes these format

`Class_ID, Name, Sample_Num, Flag, Gender`

### Estimate age

`python estimate_age.py`

This script add age label to identity_meta.csv

`Class_ID, Name, Sample_Num, Flag, Gender, Age`

