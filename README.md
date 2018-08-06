# Tracking Football Players
### Third Year Project 2017-2018
### Sarah Akerman

The aim of this project is to produce a system which will detect, track and identify football players from low quality amateur footage from a single static camera. 
The system will contain 3 main components:
- Detection: a HOG detector trained on the INRIA person dataset (pedestrians)
- Tracking: subsequent detections of the same person will be linked into 'tracklets' using temporal coherance and Kalman filtering
- Identification: the tracklets will be run through a K-NN classifier trained on SIFT features to identify the player in each tracklet.

The resulting tracking and identification information will be displayed over the original video footage by drawing bounding boxes aorund each tracked player:
- White bounding boxes will indicate an identified player, and will have a label attached to the bounding box
- Red bounding boxes will indicate that a player has been tracked, but has not been successfully identified.

To compile and run the tracker, run:
```bash
cd src
./compileTracker
./runTracker
```

For more information on optional parameters, run:
```bash
cd src
./tracker -h
```

A task board for this project with a breakdown of tasks and progress is available on [Trello](https://trello.com/b/TefN0YgJ/tracking-football-players-third-year-project).