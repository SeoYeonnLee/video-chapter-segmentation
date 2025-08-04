# TwinSeg: Temporal Window-based Video Chapter Segmentation

TwinSeg is a novel approach for video chapter segmentation that effectively utilizes temporal contextual information through a window-based self-attention mechanism.

<img src="https://github.com/user-attachments/assets/026b0ca2-d454-4016-8f4c-9d1a9ae3ecb7">
<br>
<br>


## Installation
```
pip install -r requirements.txt
```
<br>

## Dataset Preparation
1. Download video frames and extract them to ```./youtube_video_frame_dataset/```
2. Prepare subtitle files in ```./dataset/```
3. Ensure the dataset structure follows:
   ```
   TwinSeg/
    ├── youtube_video_frame_dataset/
    │   ├── video_id_1/
    │   │   ├── 00001.jpg
    │   │   ├── 00002.jpg
    │   │   └── ...
    │   └── video_id_2/
    ├── dataset/
    │   ├── all_in_one_with_subtitle_final.csv
    │   ├── final_train.txt
    │   ├── final_validation.txt
    │   └── subtitle_files/
    └── ...
   ```
<br>

## Training
```
python train_video_segment.py \
    --clip_frame_num 16 \
    --window_size 1 \
```
<br>

## Test
```
python test_video_segment.py \
    --clip_frame_num 16 \
    --window_size 1 \
```
