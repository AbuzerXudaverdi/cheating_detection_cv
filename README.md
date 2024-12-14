Overview

This class is designed to handle video input, process frames through an external FrameHandler object, and detect segments of interest based on pose estimations or other criteria. Once processed, the results can be exported to a CSV file or represented as subtitles for convenient review.
Features

    Video Processing: Reads an input video file and processes its frames.
    Suspicious Frame Detection: Integrates with FrameHandler (to be implemented separately) for identifying suspicious frames.
    Timestamping: Converts frame timestamps into human-readable formats for display in subtitles or logs.
    Subtitle Generation (SRT): Generates SRT subtitle files highlighting suspicious periods in the video.
    CSV Export: Outputs detailed results (timestamps, frame states, poses) to a CSV file.

Prerequisites

    Python 3.7+
    OpenCV (cv2) for video capture and frame manipulation.
    pandas for CSV export.
    FrameHandler class which must define a process_video method and return processed frame results. (This code references FrameHandler, which should be defined in another file.)
