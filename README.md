This project is an Intelligent Video Surveillance System that uses a custom database created from various videos downloaded from the internet. The system is trained on a dataset of normal events captured in different locations, such as malls and streets. The trained model aims to detect abnormal events in real-time video streams.

## Table of Contents

1. [Project Name](#project-name)
2. [Table of Contents](#table-of-contents)
3. [Project Demo](#project-demo)
4. [Badges](#badges)
5. [Installation](#installation)
6. [Usage](#usage)
7. [Configuration](#configuration)
8. [Contributing](#contributing)
9. [License](#license)
10. [Acknowledgments](#acknowledgments)
11. [Documentation](#documentation)

## Project Demo
### Result Demo
A demo video showcasing the Intelligent Video Surveillance System in action can be found at 
[Demo Video](https://drive.google.com/file/d/18YfjUhzyBxU5xdh4nZ4FvNKyILVYerDV/view?usp=sharing).

## Badges

[![License](https://img.shields.io/badge/license-MIT-green)](https://opensource.org/licenses/MIT)

## Installation

To run this project, you need to have the following libraries installed:

- OpenCV (cv2)
- NumPy
- Keras
- Imutils

You can install the required libraries using pip:

```bash
pip install opencv-python
pip install numpy
pip install keras
pip install imutils
```

## Usage

The code uses a pre-trained neural network model (`saved_model.h5`) to detect abnormal events in video streams. The main logic of the code is as follows:

1. Load the pre-trained neural network model using Keras.
2. Read video frames from the specified video file.
3. Process each frame to extract features for anomaly detection.
4. Calculate the mean squared loss (MSE) between the original and reconstructed frames obtained from the model.
5. Temporal smoothing: To reduce noise, apply a smoothing factor to the loss values.
6. Dynamically adjust the threshold for anomaly detection based on past scores.
7. An abnormal event is detected if the smoothed loss exceeds the threshold.

The code continuously processes video frames and displays the video with detected abnormal events marked.
### frontend 
1. The front end provides a simple user interface to upload a video file for analysis. Follow these steps to use the Intelligent Video Surveillance System frontend:
2. The front end provides a simple user interface to upload a video file for analysis. Follow these steps to use the Intelligent Video Surveillance System frontend:
3. Click the "Choose File" button to select a video file (supported formats are .mp4 and .avi).
4. Click the "Choose File" button to select a video file (supported formats are .mp4 and .avi).
5. The video will be played in the player, and the analysis result overlay will be displayed.
6. The resulting overlay will indicate whether the video contains an "Abnormal Event Detected" or "No Abnormal Event Detected."

   
## Configuration

1. Replace the `path` variable with the path to the video file you want to analyze.

2. Fine-tune the `threshold`, `alpha`, and other parameters to optimize the system's performance based on your specific use case.

## Contributing

I want you to know that contributions to this project are welcome. If you have any issues or suggestions for improvement, feel free to open a pull request or create an issue on the GitHub repository.

## License

This open-source project is licensed under the [MIT License](LICENSE). You can use, modify, and distribute the code, but please provide proper attribution.

## Acknowledgments

The Intelligent Video Surveillance System is a project that will demonstrate anomaly detection in video streams using neural networks and computer vision techniques. The project utilizes a custom database of regular events in various locations to train the model.

## Documentation

To use the Intelligent Video Surveillance System, follow these steps:

1. Install the required libraries mentioned in the [Installation](#installation) section.

2. Prepare your video file for analysis and update the `path` variable in the code with the correct file path.

3. Fine-tune the threshold and other parameters based on your specific use case in the `threshold` and `alpha` variables.

4. Run the script in a Python environment.

The script will process the video frames, detect abnormal events, and display the video stream with any detected abnormal events marked. You can adjust the threshold and other parameters for optimal anomaly detection performance for different scenarios.

