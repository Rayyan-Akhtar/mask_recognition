# Mask Recognition

## Table of Contents

- [About](#about)
- [Getting Started](#getting_started)
- [Usage](#usage)
- [Contributing](../CONTRIBUTING.md)

## About <a name = "about"></a>

Face Mask Recognition using PyTorch.

It creates a bounding box around the face of the person present in the image and put a text
at the top of the bounding box shows probability of mask on the face.

## Getting Started <a name = "getting_started"></a>


### Prerequisites

```
pytorch >= 1.2.0
torchvision >= 0.3.0
```

### Installing

It can be easily installed by the pypi package.

```
pip install mask-recognition
```

## Usage <a name = "usage"></a>

```
from mask_recognition import MaskRecognition

import cv2 as cv

mr = MaskRecognition(device=0)  # -1 for cpu, 0 for gpu

frame = mr.recognize(frame, color="rgb")    # color="bgr" for BGR color scheme. frame is the RGB image.

########################## To use webcam ##########################

mr.cam_capture(device_id=0)     # 0 for default or 1, 2, 3, if more than one webcam

## press esc to stop    
```