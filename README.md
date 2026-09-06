# Record-Erosion-and-Dilation

## Name
Thamizh S

## Register Number
212224040350

## Objective

Implement and compare different morphological image processing techniques using OpenCV.

The techniques used are:

- Erosion
- Dilation

## Requirements

- Python 3
- OpenCV (`cv2`)
- NumPy
- Matplotlib

## Methodology

1. Import the required Python libraries.
2. Create a blank image using NumPy.
3. Add the text `THAMIZH` to the image using `cv2.putText()`.
4. Display the input image.
5. Create a `3 × 3` kernel for morphological operations.
6. Apply Erosion using `cv2.erode()` to shrink the text.
7. Apply Dilation using `cv2.dilate()` to expand the text.
8. Display the input, eroded, and dilated images for comparison.

## Implementation

```python
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create a blank image
image = np.zeros((500, 500, 3), dtype=np.uint8)

# Add text on the image
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(
    image,
    'THAMIZH',
    (100, 250),
    font,
    1,
    (0, 255, 255),
    2,
    cv2.LINE_AA
)

# Display the input image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title("Input Image with Text")
plt.axis('off')
plt.show()

# Create a simple square kernel (3x3)
kernel = np.ones((3, 3), np.uint8)

# Apply erosion (shrinking effect)
eroded_image = cv2.erode(image, kernel, iterations=1)

# Display the eroded image
plt.imshow(cv2.cvtColor(eroded_image, cv2.COLOR_BGR2RGB))
plt.title("Eroded Image")
plt.axis('off')
plt.show()

# Apply dilation (expanding effect)
dilated_image = cv2.dilate(image, kernel, iterations=1)

# Display the dilated image
plt.imshow(cv2.cvtColor(dilated_image, cv2.COLOR_BGR2RGB))
plt.title("Dilated Image")
plt.axis('off')
plt.show()
```
## Output

### Input Image

<img width="468" height="488" alt="image" src="https://github.com/user-attachments/assets/3ff64eb5-3789-4187-a04d-071b5d08c5a2" />

### Eroded Image

<img width="450" height="475" alt="image" src="https://github.com/user-attachments/assets/84f36791-de76-4d0a-b335-6c48913f0369" />

### Dilated Image

<img width="475" height="500" alt="image" src="https://github.com/user-attachments/assets/f2022c34-8deb-480f-9972-54e69f18fcd5" />
