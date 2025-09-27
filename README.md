# Open-Vocabulary Prohibited Item Detection for Real-World X-Ray Security Inspection
To support the research on the task of open-vocabulary prohibited item detection, we contribute the first X-ray security inspection OVOD evaluation benchmark, named PIXray Caption dataset, which contains 15 common categories and 5,046 image-caption pair annotations. The complete dataset is updated.
## Download
Download the entire PIXray Caption dataset from Google Drive [![Download Dataset](https://img.shields.io/badge/Download-Dataset-blue)](https://drive.google.com/file/d/1tkjVBSUP1AfpwgqDPLIPDss3kNfBVvZ4/view?usp=sharing)
## Data Preparation
Prepare data following [MMDetection](https://github.com/open-mmlab/mmdetection). 
### Data Split
Obtain the json files for OVOD task from [here](https://drive.google.com/drive/folders/1rPMt7gGr8stSZLIl1SMfu6M8Z2AvcWkW?usp=sharing) and put them under `data/pixray/ovod`. The data structure looks like:
```
data/
├── pixray
│   ├── annotations
│   │   ├── pixray_train.json
│   │   ├── pixray_test.json
│   ├── captions
│   │   ├── pixray_caption_train.json
│   │   ├── pixray_caption_test.json
│   ├── ovod
│   │   ├── pixray_train_base.json
│   │   ├── pixray_val_base.json
│   │   ├── pixray_val_novel.json
│   │   ├── pixray_captions_train_allcaps.json
│   ├── train
│   ├── test
```
The json file `pixray_captions_train_allcaps.json` for caption supervision is obtained following [Detic](https://github.com/facebookresearch/Detic/blob/main/datasets/README.md).
### Class Embeddings
Obtain the class embeddings [here](https://drive.google.com/file/d/1g6rwkd6_m6SDtyoDiN5SEEScJ1trUH0n/view?usp=sharing).
### CLIP Checkpoints
We use CLIP's ViT-B-32 model for the implementation of our method. Obtain the state_dict of the model from [here](https://drive.google.com/file/d/1Pp9PZW3FOqO1YZiV6wT54MMcs1hcLjZP/view?usp=sharing).
## Citation
If you find this dataset useful for your research, please cite:
```bibtex
@ARTICLE{11095302,
  author={Lin, Shuyang and Jia, Tong and Wang, Hao and Ma, Bowen and Li, Mingyuan},
  journal={IEEE Transactions on Information Forensics and Security}, 
  title={Open-Vocabulary Prohibited Item Detection for Real-World X-Ray Security Inspection}, 
  year={2025},
  volume={20},
  number={},
  pages={7469-7481},
  keywords={Location awareness;Accuracy;Annotations;Interference;Object detection;Detectors;Inspection;Public security;Security;X-ray imaging;X-ray security inspection;prohibited item detection;open-vocabulary object detection},
  doi={10.1109/TIFS.2025.3586492}}
