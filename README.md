# PrepareImage - Custom Your Our Image Dataset
 Flexible and Easy. We perform a package that help you build your own image dataset. Specially, it's easy to add your own prepare function 

`mode` in `["split", "combine", "line", "pos", "all", "gray", "look_alike", "without_edge"]`:
- combine: combine input, output images, then split to train/validation/test set
- line: add line to input images
- all: line then combine

1. Run on Terminal
```python
python3 prepare_data.py
```
```
python prepare_data.py --image_dir ../training_data/lhq_256 --caffemodel hed_pretrained_bsds.caffemodel --mode all --pos2_dir ../training_data/new_data/pos2 --pos 2 --grayscale_dir ../training_data/new_data/grayscale --line_dir ../training_data/new_data/edge --train_dir ../training_data/new_data/train --test_dir ../training_data/new_data/test --val_dir ../training_data/new_data/val --output_dir ../training_data/new_data/grayscale --combine_dir ../training_data/new_data/combine
```

Split Data:
```
python prepare_data.py --mode split --train_dir ../training_data/new_data/train --test_dir ../training_data/new_data/test --val_dir ../training_data/new_data/val --combine_dir ../training_data/new_data/combine
```

2. Run on Jupyter Notebook
```python
%%bash
python3 combine.py
```