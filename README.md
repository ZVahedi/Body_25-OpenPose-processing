This project processes CSV files containing body pose keypoints data (exported from OpenPose) and applies a low-pass Butterworth filter to smooth the data. Each CSV file is processed independently, and the corresponding video duration is calculated for each file to accurately apply the filter. The project also interpolates missing values and filters out low-confidence keypoints.

## Features

- **Keypoint Extraction:** Processes keypoints from the upper body and other parts defined in OpenPose's Body25 model.
- **Butterworth Filtering:** Applies a Butterworth low-pass filter to smooth the pose keypoints based on each video's frame rate.
- **Confidence-Based Filtering:** Filters keypoints with low confidence (confidence ≤ 0.69) by setting their values to NaN.
- **Interpolation:** Performs interpolation on NaN values to ensure continuous data after filtering.
- **Video Duration Calculation:** The duration of each video is calculated separately to properly adjust the filtering process.
