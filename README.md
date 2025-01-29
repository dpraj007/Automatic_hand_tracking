# Automatic Hand Tracking with SAM 2

This project implements automatic hand tracking in videos using MediaPipe for hand detection and Segment Anything Model 2 (SAM 2) for segmentation.

## Setup

1. Clone this repository:
```
git clone https://github.com/your-username/automatic-hand-tracking.git
cd automatic-hand-tracking
```

2. Create a virtual environment (optional but recommended):
```
python -m venv venv
source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
```

3. Install the required packages:
```
pip install -r requirements.txt
```

4. Download the SAM 2 checkpoint:
```
wget https://dl.fbaipublicfiles.com/segment_anything/sam_vit_h_4b8939.pth
```

## Usage

1. Place your input video file in the project directory.

2. Run the script:
```
python hand_tracking.py
```

3. The processed video will be saved as `output.mp4` in the same directory.

## Requirements

Create a file named `requirements.txt` with the following content:

```
mediapipe
opencv-python
numpy
torch
git+https://github.com/facebookresearch/segment-anything.git
```

## Notes

- This script is optimized for GPU usage. If you're using Google Colab, it will automatically utilize the available GPU.
- The script processes the entire video, which may take some time depending on the video length and your hardware.
- Adjust the `max_num_hands` and `min_detection_confidence` parameters in the `detect_hands` function if needed.

## License

This project is licensed under the MIT License - see the LICENSE file for details.

