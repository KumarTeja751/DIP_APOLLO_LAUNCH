# DIP_APOLLO_LAUNCH

## Code:
```python
import cv2
import matplotlib.pyplot as plt

image = cv2.imread('Chichubuddi.jpg', cv2.IMREAD_GRAYSCALE)

height, width = image.shape
print(f'Width: {width}, Height: {height}')

plt.figure(figsize=[10, 10])
plt.imshow(image, cmap='gray')
plt.axis('on')  
plt.show()
cv2.imwrite('Apollo-11-launch.png', image)

import cv2
import matplotlib.pyplot as plt

image = cv2.imread('Chichubuddi.jpg')

text = 'Apollo 11 Saturn V Launch, July 16, 1969'
font_face = cv2.FONT_HERSHEY_PLAIN
font_scale = 3
font_thickness = 3
text_color = (255, 255, 255)  

text_size, _ = cv2.getTextSize(text, font_face, font_scale, font_thickness)
text_x = (image.shape[1] - text_size[0]) // 2  
text_y = image.shape[0] - 50  

cv2.putText(image, text, (text_x, text_y), font_face, font_scale, text_color, font_thickness)

magenta = (255, 0, 255)  
image_rectangle = cv2.rectangle(image, (700, 60), (500, 630), magenta, thickness=3, lineType=cv2.LINE_8)

plt.figure(figsize=[12, 12])
plt.imshow(cv2.cvtColor(image_rectangle, cv2.COLOR_BGR2RGB))
plt.axis('on')
plt.show()
```
```Python
import cv2
import matplotlib.pyplot as plt
image = cv2.imread('Apollo.jpg')
height=720
width=1280
print(f"Width: {width}, Height: {height}")
plt.figure(figsize=(10, 10))
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.show()
cv2.imwrite('Apollo-11-Launch.png', image)
x, y, a, b = 250, 250, 250, 250
cropped_img = img[y:y+b, x:x+a]
resized_img = cv2.resize(cropped_img,None, fx=2, fy=2)
flipped_img = cv2.flip(resized_img, 1)
plt.figure(figsize=[5, 5])
plt.imshow(flipped_img[:, :, ::-1])
plt.title("Cropped, Resized, and Flipped Image")
plt.show()
img = cv2.imread('newzealand.jpg', cv2.IMREAD_COLOR)
print(img.shape)
plt.figure(figsize=[3, 3])
plt.imshow(img[:, :, ::-1])
plt.title("Original Image")
plt.show()
gray_image = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)
print("Grayscale Image Shape:", gray_image.shape)
plt.figure(figsize=(10, 10))
plt.imshow(gray_image)
plt.axis('off')
plt.title("Grayscale Image")
plt.show()
```
## OUTPUT:
![image](https://github.com/user-attachments/assets/b857ad3e-d361-4229-86bb-ee0a85301c8a)
![image](https://github.com/user-attachments/assets/19da1d1f-90cd-42d2-a283-2f6833998479)
![image](https://github.com/user-attachments/assets/deaaab1e-b0ae-415e-b752-b9b0caa895d4)
![image](https://github.com/user-attachments/assets/985518ea-7ca5-40b4-bda5-f41ec675d0c8)

