# Image Recognizer

This application uses TensorFlow.js and the COCO-SSD model to perform object detection on images. It processes an input image, detects objects, and outputs the results with confidence scores.

## Features
- Object detection using the COCO-SSD model.
- Image preprocessing with `sharp`.
- Outputs detected objects and their confidence levels.

## Prerequisites
- Node.js (v16 or later recommended)
- npm (Node Package Manager)

## Installation
1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd image-process
   ```
2. Install dependencies:
   ```bash
   npm install
   ```

## Usage
1. Place the image you want to process in the `image/` directory or provide the path to any image on your system.
2. Run the application:
   ```bash
   node recognize.js <image-path>
   ```
   Replace `<image-path>` with the path to your image file. For example:
   ```bash
   node recognize.js image/image1.jpg
   ```

## Example Output
```
Loading model...
Model loaded!
Detecting objects...
[
  {
    class: 'person',
    score: 0.98,
    bbox: [120, 80, 200, 300]
  },
  {
    class: 'dog',
    score: 0.87,
    bbox: [300, 200, 400, 500]
  }
]

Detected Objects:
1. person - Confidence: 98.00%
2. dog - Confidence: 87.00%
```

## Dependencies
- `@tensorflow-models/coco-ssd`
- `@tensorflow/tfjs`
- `@tensorflow/tfjs-node`
- `jpeg-js`
- `sharp`
