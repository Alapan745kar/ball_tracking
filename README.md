
# CourtCheck - Automatic Tennis IN/OUT Detector

<img src="https://github.com/Alapan745kar/ball_tracking" alt="logo" width="80"/>

A super cool computer vision project that watches tennis videos and says if the ball is IN or OUT by itself!

![demo](https://github.com/AggieSportsAnalytics/CourtCheck/blob/main/images/game9_processed_10s.gif)

## What it do
- Find the court lines automatic  
- Track the tiny yellow ball (even when it go very fast)  
- Show clean 2D top view of court + ball moving  
- Draw nice yellow trail behind the ball  

## How it works (simple version)

1. **Court Detection**  
   → Used Detectron2 to find 17 important points on court  
   → Trained on Google Colab because my laptop cried

2. **Make court flat**  
   → Turn the 3D-looking court into perfect 2D rectangle (homography magic)

3. **Ball Tracking**  
   → Used TrackNet model (thank you yastrebksv!!)  
   → Model looks at 3 frames and guess where ball is

4. **Final video**  
   → Left = normal video with lines + ball trail  
   → Bottom-right = mini 2D court (like hawk-eye on TV)


## Easiest way to run (Google Colab - FREE GPU)
Click here → https://colab.research.google.com/drive/11wkF5_nDDkTFaKCEX-e7doO-I55bn3NW

Just upload your tennis video and press play all!

## Or run on your PC (need good GPU)
```bash
git clone https://github.com/AggieSportsAnalytics/CourtCheck.git
cd CourtCheck
pip install -r requirements.txt
