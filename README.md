# Genshin_Obeject_Detection

Train test video download link:
链接：https://pan.baidu.com/s/1H_3bgvUAEmxFNJ63sYtbDg 
提取码：1234 
--来自百度网盘超级会员V5的分享

```bash
!git clone https://github.com/ultralytics/yolov5  # clone
%cd yolov5
!pip install -r requirements.txt  # install
```

```bash
import torch
from yolov5 import utils
display = utils.notebook_init()
```

```bash
yaml_text = """train: ./data/Genshin/train/
val: ./data/Genshin/test/
nc: 8
names: ['没用的薄荷','没用的甜甜花','神里绫龟','蓝矿石','紫矿石','白铁矿石','丘丘人','NTR']"""
with open("data/Genshin.yaml", 'w') as file:
    file.write(yaml_text)
```

```bash
!python train.py --img 600 --data data/Genshin.yaml --cfg models/yolov5s.yaml --weights weights/yolov5m.pt --batch 8 --epochs 100 --name Genshin --workers 4
!python detect.py --weights runs\train\Genshin3\weights\best.pt --source Train test video download link
```
