
# 👋 Automatic Hand Tracking with SAM 2 🖐️

This project implements automatic hand tracking in videos 🎬 using MediaPipe for hand detection 🔍 and Segment Anything Model 2 (SAM 2) for segmentation 🧠.

## 🛠️ Setup

1. Clone this repository: ⬇️
   ```bash
   git clone https://github.com/dpraj007/Automatic_hand_tracking.git
   cd Automatic_hand_tracking
   ```

2. Create a virtual environment (optional but recommended):  virtual environment isolates project dependencies 📦
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Linux/macOS 🍎
   venv\Scripts\activate  # On Windows 🪟
   ```

3. Install the required packages: ⚙️ dependencies listed in `requirements.txt`
   ```bash
   pip install -r requirements.txt
   ```

4. Download the SAM 2 checkpoint: 💾 SAM model weights for segmentation
   ```bash
   wget https://dl.fbaipublicfiles.com/segment_anything/sam_vit_h_4b8939.pth
   ```

## 🚀 Usage

1. Place your input video file 📂 in the project directory.

2. Open and run the Jupyter Notebook 📓 `Automatic_Hand_Tracking_03.ipynb`. You can use Jupyter Lab or Google Colab ☁️.

3. The processed video with hand masks ✨ will be saved as `output_final.mp4` in the same directory. 🎉



## 📝 Notes

- This script is optimized for GPU usage 🚀. If you're using Google Colab, it will automatically utilize the available GPU 💡.
- The script processes the entire video frame by frame ⏳, which may take some time depending on the video length and your hardware 💻.
- Adjust the `max_num_hands` and `min_detection_confidence` parameters in the `detect_hands` function within the notebook 📓 if needed to fine-tune hand detection.

## 📜 License

This project is licensed under the MIT License ⚖️ - see the LICENSE file for details. 📄

