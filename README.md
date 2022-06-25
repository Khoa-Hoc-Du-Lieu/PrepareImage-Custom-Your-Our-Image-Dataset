# PrepareImage - Custom Your Our Image Dataset
 Flexible and Easy. We perform a package that help you build your own image dataset. Specially, it's easy to add your own prepare function 

## Install
```
pip instal prepareImage
```
## How to use

### 1. Fork this repo and custom it!
### 2. Class dataset
Coming soon! 

This is what make this package powerful.
### 3. Run directly on file `prepare_data.py`
`mode` in `["split", "combine", "line", "pos", "all", "gray", "look_alike", "without_edge"]`:
- combine: combine input, output images, then split to train/validation/test set
- line: add line to input images
- all: line then combine

1. Run on Terminal

If you already installed the package:

```python
python3 -m prepareImage.prepare_data
```
or download file `prepare_data.py` from this repo and run:
```python
python3 prepare_data.py
```

Example:
```
python prepare_data.py --mode all \
--image_dir ../training_data/lhq_256 \ 
--caffemodel hed_pretrained_bsds.caffemodel \
--pos2_dir ../training_data/new_data/pos2 \
--pos 2 \
--grayscale_dir ../training_data/new_data/grayscale \
--line_dir ../training_data/new_data/edge \
--train_dir ../training_data/new_data/train \
--test_dir ../training_data/new_data/test \
--val_dir ../training_data/new_data/val \
--output_dir ../training_data/new_data/grayscale \
--combine_dir ../training_data/new_data/combine
```

Split Data:
```
python prepare_data.py --mode split \
--train_dir ../training_data/new_data/train \
--test_dir ../training_data/new_data/test \
--val_dir ../training_data/new_data/val \
--combine_dir ../training_data/new_data/combine
```

1. Run on Jupyter Notebook
```python
%%bash
python3 prepare_data.py
```