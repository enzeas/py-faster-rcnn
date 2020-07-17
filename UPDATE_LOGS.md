# Update logs

### 1. 一些小改动，使代码能在python3环境中运行。
- xrange -> range
- iteritems -> items
- cPickle -> pickle
- has_key -> in
- print -> print()
- string.format


### 2. 一些代码fix，使代码能正常运行。

- add import
	- lib/fast_rcnn/train.py
	- ```import google.protobuf.text_format```

- some import location
	- lib/datasets/pascal_voc.py
	- ```import datasets.voc_eval as voc_eval```
	- lib/pycocotools/coco.py
	- ```import pycocotools.mask as mask```
	- lib/pycocotools/cocoeval.py
	- ```import pycocotools.mask as mask```
	- lib/rpn/anchor_target_layer.py
	- ```from rpn.generate_anchors import generate_anchors```
	- lib/rpn/proposal_layer.py
	- ```from rpn.generate_anchors import generate_anchors```

- fix
	- lib/pycocotools/cocoeval.py
	- ```gtind = [ind for (ind, g) in sorted(enumerate(gt), key=lambda g: g['_ignore']) ]```
	- lib/rpn/proposal_target_layer.py
	- ```start = int(start)```
	- ```end = int(end)```
	- ```fg_rois_per_this_image = int(fg_rois_per_this_image)```
	- ```bg_rois_per_this_image = int(bg_rois_per_this_image)```
