# Assignment: Automatic Hand Tracking

**Goal:** Build an automatic pipeline that tracks hand movements in a video.  
**Tools**: cv2, Google MediaPipe, SAM 2

# Preliminaries

### Data

Download the video [test.mp4](https://drive.google.com/file/d/1rHbzU3CSQbqtzPcevcnA6ZRd0nNDYb08/view?usp=drive_link).

### Environment Set Up

* `conda create -n sam2 python=3.12`  
* `conda activate sam2`  
* `pip3 install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu118`  
  * May take a bit.  
  * See [PyTorch installation](https://pytorch.org/get-started/locally/) if this doesn’t work.  
* Follow the instructions for setting up SAM 2 [here](https://github.com/facebookresearch/sam2)  
* Install **mediapipe** with `pip install -q mediapipe`  
* And **cv2** with `pip install opencv-python`

# Part 1: Detect Hands in the First Frame

References: [Google MediaPipe](https://ai.google.dev/edge/mediapipe/solutions/vision/hand_landmarker), [Google Colab Sample](https://colab.research.google.com/github/googlesamples/mediapipe/blob/main/examples/hand_landmarker/python/hand_landmarker.ipynb)

Using the references above, write code that can output information on hand location(s) in an image (represented however you wish \- e.g., numpy array). This instruction is intentionally vague. Your goal is to return an output that can be used as a SAM 2 prompt (e.g., clicks, bounding boxes). Feel free to look into [SAM 2 Video Predictor Example](https://github.com/facebookresearch/sam2/blob/main/notebooks/video_predictor_example.ipynb) for example prompts.

# Part 2: Use Part 1 and SAM 2 to Track Hands

References: [SAM 2 Repo](https://github.com/facebookresearch/sam2), [SAM 2 Video Predictor Example](https://github.com/facebookresearch/sam2/blob/main/notebooks/video_predictor_example.ipynb)

Write a function that uses SAM 2 and the results from Part 1 to generate masks for every frame of the video.

* There can be multiple masks per frame.  
* The results from Part 1 are your *input prompts* into SAM 2\.  
* Ideally, the parameters of this function are an input and output path. The function will write a new video with the masks to the output path.

# Deliverables

1) **Link to Github code**: code style and organization are important and will be evaluated\! Include a README / pip requirements file for set up.  
2) **Output video demo**: an output video with the masked hands