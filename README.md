# Virtual Mouse Controller using Hand Gestures

A computer vision-based virtual mouse controller that allows you to control your computer's mouse using hand gestures captured through a webcam.

## 🎯 Features

- **Cursor Movement**: Control mouse cursor by moving your index finger
- **Click Action**: Perform mouse clicks by bringing index and middle fingers together
- **Real-time Tracking**: Smooth and responsive hand tracking using MediaPipe
- **Visual Feedback**: Live video feed with hand landmarks and gesture indicators

## 🛠️ Technologies Used

- **Python** 
- **OpenCV**: For image processing and video capture
- **MediaPipe**: For hand tracking and landmark detection
- **NumPy**: For numerical operations
- **AutoPy**: For controlling mouse movements


## 📁 Project Structure

```
virtual-mouse-controller/
│
├── Virtual_Cursor.py           # Main application file
├── HandTrackingModule.py       # Hand detection and tracking module
├── README.md                   # Project documentation
└── requirements.txt            # Python dependencies
```

## 💻 Usage

1. Activate your virtual environment:
```bash
conda activate mediapipe_env
```

2. Run the main script:
```bash
python Virtual_Cursor.py
```

3. **Controls**:
   - **Move Cursor**: Raise your index finger (keep middle finger down)
   - **Click**: Raise both index and middle fingers and bring them close together

4. Press `Ctrl+C` in terminal to exit the program

## 🎮 How It Works

1. **Hand Detection**: Uses MediaPipe to detect hand landmarks in real-time
2. **Finger Tracking**: Identifies the position of index and middle finger tips
3. **Gesture Recognition**: 
   - One finger up = Movement mode
   - Two fingers up and close = Click mode
4. **Coordinate Mapping**: Maps hand position to screen coordinates
5. **Smoothing**: Applies smoothing algorithm for stable cursor movement

## ⚙️ Configuration

You can modify these parameters in `Virtual_Cursor.py`:

- `wCam, hCam`: Camera resolution (default: 640x480)
- `frameR`: Frame reduction for mapping area (default: 100)
- `smoothening`: Cursor smoothing factor (default: 7)

## 🐛 Troubleshooting

**Camera not detected:**
- Change camera index in `Virtual_Cursor.py` from `cv2.VideoCapture(0)` to `cv2.VideoCapture(1)` or `2`
- Make sure no other application is using the camera

**Module not found errors:**
- Ensure all dependencies are installed in the correct environment
- Try reinstalling packages: `pip install --upgrade opencv-python mediapipe`


## 🎓 Acknowledgments

This project was developed as part of the Computer Vision course. Special thanks to my professor for guidance and teaching the fundamentals of computer vision.


