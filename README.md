# VideoHandler Class

The `VideoHandler` class provides functionality to process a given video file, detect suspicious frames (based on logic defined in a `FrameHandler` class), and produce outputs such as CSV logs and SRT subtitles.

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Prerequisites](#prerequisites)


## Overview

This class is designed to handle video input, process frames through an external `FrameHandler` object, and detect segments of interest based on pose estimations or other criteria. Once processed, the results can be exported to a CSV file or represented as subtitles for convenient review. It's developed to estimate head poses and track eye gaze to detect cheating in online exams.

## Features

- **Video Processing**: Reads an input video file and processes its frames.
- **Suspicious Frame Detection**: Integrates with `FrameHandler` (to be implemented separately) for identifying suspicious frames.
- **Timestamping**: Converts frame timestamps into human-readable formats.
- **Subtitle Generation (SRT)**: Generates SRT subtitle files highlighting suspicious periods in the video.
- **CSV Export**: Outputs detailed results (timestamps, frame states, poses) to a CSV file.

## Prerequisites

- **Python 3.7+**
- **OpenCV (cv2)** for video capture and frame manipulation.
- **pandas** for CSV export.
- **FrameHandler class** which must define a `process_video` method. This code references `FrameHandler`, so it must be provided separately.

Install prerequisites via:
```bash
pip install opencv-python pandas
