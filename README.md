# Deepfake Detection

This repository contains a comprehensive implementation of a deepfake detection system. The project leverages computer vision and machine learning techniques to analyze video streams, detect potential deepfake frames, and highlight suspicious activity.

## Project Overview

The goal of this project is to analyze video data to:

- Detect frames that are likely to be deepfakes.
- Evaluate facial similarity across consecutive frames to identify inconsistencies.
- Provide actionable feedback by marking frames as real or suspicious.
- Output a processed video highlighting detected deepfakes.

## Detection Steps

1. **Video Input**: Load the video for analysis.
2. **Face Detection**: Use a pre-trained MTCNN model to detect faces in frames.
3. **Feature Extraction**: Extract facial embeddings using the InceptionResnetV1 model.
4. **Similarity Calculation**: Compute cosine similarity between consecutive frame embeddings.
5. **Deepfake Classification**: Compare similarity scores against thresholds to classify frames as real or deepfake.
6. **Output Video**: Generate a video with visual markers indicating detected deepfakes.

## Key Features

- **Threshold-based Detection**: Adjustable thresholds for similarity scores and deepfake frame counts.
- **Frame-by-Frame Analysis**: Process and classify every frame at defined intervals.
- **Real-time Feedback**: Highlights frames with detected deepfakes.
- **Efficiency**: Optimized processing with frame skipping based on FPS.

## Tools and Libraries

- **Python**: Programming language used for implementation.
- **OpenCV**: For video processing and manipulation.
- **Facenet-PyTorch**: For face detection and embedding extraction.
- **Torchvision**: For preprocessing and tensor manipulation.
- **NumPy**: For numerical operations and similarity calculations.

## How to Use

1. Clone the repository and navigate to the project directory.
2. Install the required dependencies listed in the `requirements.txt` file.
3. Run the detection script using the command:

   ```bash
   python deepfake_detection.py --input_video <path_to_input_video> --output_video <path_to_output_video>
   ```

4. Review the output video for frames marked as deepfakes.

## Insights and Recommendations

- **Accuracy Tuning**: Adjust the thresholds for facial similarity and frame counts to improve detection accuracy.
- **Scalability**: The framework can be extended to handle real-time video streams.
- **Improvement**: Integrate additional models or techniques to enhance detection robustness.

## Applications

- **Content Moderation**: Detect and flag deepfake content on social media platforms.
- **Forensics**: Assist law enforcement in analyzing suspect video evidence.
- **Authentication**: Enhance video-based security systems by detecting manipulated footage.

