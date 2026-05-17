# Exp-9 – Implementation of Erosion and Dilation

# Name : Harini S
# Reg no: 212224240049

## Aim

To implement Erosion and Dilation using Python and OpenCV.

---

## Algorithm

 Step 1: Import the necessary libraries such as OpenCV (`cv2`), NumPy (`numpy`), and Matplotlib (`matplotlib.pyplot`) for image processing and display.

 Step 2: Create a blank image using NumPy and add text to the image using `cv2.putText()` with suitable font style, size, color, and thickness.

 Step 3: Create a structuring element (kernel) using `cv2.getStructuringElement()` for performing morphological operations.

 Step 4: Apply the erosion operation using `cv2.erode()` to shrink the white regions and remove small noises from the image.

 Step 5: Apply the dilation operation using `cv2.dilate()` to enlarge the white regions and enhance image features.

 Step 6: Convert the images from BGR to RGB format using `cv2.cvtColor()` for proper display in Matplotlib.

 Step 7: Display the original, eroded, and dilated images using `plt.imshow()` with titles and axis settings.

### Program
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = np.zeros((500, 500, 3), dtype=np.uint8)
```
## Add text on the image
```
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'Hello World', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)
```
## Display the input image
```
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB for displaying
plt.title("Input Image with Text")
plt.axis('off')
```
## Erosion (shrinking effect)
```
eroded_image = cv2.erode(image, kernel, iterations=1)
plt.imshow(cv2.cvtColor(eroded_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Eroded Image")
plt.axis('off')
```
## Dilation (expanding effect)
```
dilated_image = cv2.dilate(image, kernel, iterations=1)
plt.imshow(cv2.cvtColor(dilated_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Dilated Image")
plt.axis('off')
```
## Output

## Input image
<img width="744" height="442" alt="image" src="https://github.com/user-attachments/assets/669c07ee-b429-4f61-b814-83f42a668b97" />

## Eroded image
<img width="817" height="445" alt="image" src="https://github.com/user-attachments/assets/f6802987-a444-4b1e-95ea-47b3341e30b3" />

## Dilated image
<img width="824" height="434" alt="image" src="https://github.com/user-attachments/assets/88aad4f7-0fbc-484e-8a66-e2913ca7d60b" />

## Result

Thus, the Erosion and Dilation operations were successfully implemented using Python and OpenCV. The eroded image reduced the thickness of the text, while the dilated image increased the thickness of the text.
