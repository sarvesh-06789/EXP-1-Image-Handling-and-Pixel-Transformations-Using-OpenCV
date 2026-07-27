# EXP-1-Image-Handling-and-Pixel-Transformations-Using-OpenCV
# Aim:

To perform basic image handling and pixel transformation operations using OpenCV in Python, including loading an image, displaying it, drawing shapes, adding text, resizing, rotating, flipping, cropping, and saving the modified image.
# Software Required:
Anaconda - Python 3.7

Jupyter Notebook (for interactive development and execution)
# Algorithm:
Step1:

Load an image from your local directory and display it.

Step2:

o Draw a line from the top-left to the bottom-right of the image.

o Draw a circle at the center of the image. 

o Draw a rectangle around a specific region of interest in the image. 

o Add the text "OpenCV Drawing" at the top-left corner of the image.

Step3:

o Convert the image from RGB to HSV and display it.
    
o Convert the image from RGB to GRAY and display it. 

o Convert the image from RGB to YCrCb and display it. 
    
o Convert the HSV image back to RGB and display it.

Step4:

o Access and print the value of the pixel at coordinates (100, 100). 

o Modify the color of the pixel at (200, 200) to white.

Step5:

o Resize the original image to half its size and display it.

Step6:

o Crop a region of interest (ROI) from the image (e.g., a 100x100 pixel area starting at (50, 50)) and display it.

Step7:

o Flip the original image horizontally and display it. 

o Flip the original image vertically and display it.

Step8:

o Save the final modified image to your local directory.

# Program:
```
import cv2
import matplotlib.pyplot as plt
# Read the image using OpenCV
img = cv2.imread('2.jpg', cv2.IMREAD_COLOR)
# Convert BGR (OpenCV's default) to RGB (Matplotlib's expected color order)
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
# Display the image using Matplotlib
plt.imshow(img_rgb, cmap='viridis')  # You can change 'viridis' to another cmap or use None for RGB images
plt.title("Original Image")
plt.axis('off')  # Removes axis ticks and labels
plt.show()
```

<img width="1207" height="831" alt="Screenshot 2026-07-27 140446" src="https://github.com/user-attachments/assets/0cb0e77c-796e-441a-b0df-6c50b72a8566" />




```
# Load the image
image = cv2.imread('2.jpg')
# Convert BGR (OpenCV's default) to RGB (Matplotlib's expected color order)
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
img_rgb.shape
# Draw a line from top-left to bottom-right
line_img = cv2.line(img_rgb, (0, 0), (1050, 700), (0, 255, 0), 10)
plt.imshow(line_img, cmap='viridis')  
plt.title("Image with Line")
plt.axis('on')  
plt.show()
```

<img width="1228" height="915" alt="image" src="https://github.com/user-attachments/assets/faa87284-f8a6-4d3b-844e-73bfa9c6de16" />




```
# Load the image
image = cv2.imread('Qno. 2.jpg') 

# Convert BGR (OpenCV's default) to RGB (Matplotlib's expected color order)
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
circle_img = cv2.circle(img_rgb,(300,300),100,(0,0,255),10) 
plt.imshow(circle_img, cmap='viridis')  
plt.title("Image with Circle")
plt.axis('off')  
plt.show()
```

<img width="1092" height="827" alt="image" src="https://github.com/user-attachments/assets/491bd662-d616-40f1-8e0e-b7c2fb982187" />




```
# Load the image
image = cv2.imread('Qno. 2.jpg') 

# Convert BGR (OpenCV's default) to RGB (Matplotlib's expected color order)
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
# Draw a rectangle around the Whole image
rectangle_img = cv2.rectangle(img_rgb, (0, 0), (750, 500), (0, 0, 255), 10)  # cv2.rectangle(image, start_point, end_point, color, thickness)
plt.imshow(rectangle_img, cmap='viridis')  
plt.title("Image with Rectangle")
plt.axis('on')  
plt.show()

```

<img width="1400" height="878" alt="image" src="https://github.com/user-attachments/assets/73d9b9dd-566b-4a96-bc3d-d5493794ac35" />




```
# Load the image
image = cv2.imread('Qno. 2.jpg') 

# Convert BGR (OpenCV's default) to RGB (Matplotlib's expected color order)
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
# Add text to the image
text_img = cv2.putText(img_rgb, "SHARVESH", (20, 30), cv2.FONT_HERSHEY_SIMPLEX, 1, (255, 255, 255), 10)  ## cv2.putText(image, text, position, font, font_scale, color, thickness
plt.imshow(text_img, cmap='viridis')  
plt.title("Image with Text")
plt.axis('off')  
plt.show()

```


<img width="1391" height="831" alt="image" src="https://github.com/user-attachments/assets/e85cece2-6a42-46fa-9590-153b690c70a3" />



```
# Load the image
image = cv2.imread('2.jpg')
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
# Original RGB Image
plt.imshow(image_rgb)
plt.title("Original RGB Image")
plt.axis("off")
```

<img width="777" height="742" alt="image" src="https://github.com/user-attachments/assets/217dbb37-c496-4652-be0f-c2d1b2f132cf" />



```
# Convert RGB to HSV
image_hsv = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2HSV)
# HSV Image
plt.imshow(image_hsv)
plt.title("HSV Image")
plt.axis("off")
```

<img width="840" height="690" alt="image" src="https://github.com/user-attachments/assets/675058c4-148a-47c1-a830-a7a68eb9f4ec" />



```
# Convert RGB to GRAY
image_gray = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2GRAY)
# Grayscale Image
plt.imshow(image_gray, cmap='gray')
plt.title("Grayscale Image")
plt.axis("off")
```

<img width="935" height="685" alt="image" src="https://github.com/user-attachments/assets/12e5d779-138d-4b07-b1a8-381a105499ef" />




```
# Convert RGB to YCrCb
image_ycrcb = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2YCrCb)
# YCrCb Image
plt.imshow(image_ycrcb)
plt.title("YCrCb Image")
plt.axis("off")


```
<img width="851" height="695" alt="image" src="https://github.com/user-attachments/assets/47c8cc76-8b6a-49f6-9802-f6d43ee69b6b" />




```
# Convert HSV back to RGB
image_hsv_to_rgb = cv2.cvtColor(image_hsv, cv2.COLOR_HSV2RGB)
plt.imshow(image_hsv_to_rgb)
plt.title("HSV to RGB Image")
plt.axis("off")
```

<img width="853" height="661" alt="image" src="https://github.com/user-attachments/assets/edbf767f-7541-41b0-82fe-6b5f0593c5d1" />




```
# Modify a block of pixels (300x300) to white, starting from (200, 200)
image[200:500, 200:500] = [255, 255, 255]  # Rows: 200-499, Columns: 200-499
# Convert BGR to RGB for displaying with Matplotlib
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
# Display the modified image
plt.imshow(image_rgb)
plt.title("Image with 300x300 White Block")
plt.axis("off")
plt.show()
```

<img width="952" height="732" alt="image" src="https://github.com/user-attachments/assets/aab30ff5-6c46-4042-b688-8d5e0fc132ec" />



```
# Load the image
image = cv2.imread('2.jpg')
image.shape
# Resize the image to half its size
resized_image = cv2.resize(image, (768 // 2, 600 // 2))  # (new_width, new_height)
# Convert BGR to RGB for displaying with Matplotlib
resized_image_rgb = cv2.cvtColor(resized_image, cv2.COLOR_BGR2RGB)
resized_image_rgb.shape
# Display the resized image
plt.imshow(resized_image_rgb)
plt.title("Resized Image (Half Size)")
plt.axis("off")
plt.show()
```

<img width="837" height="943" alt="image" src="https://github.com/user-attachments/assets/49b75a75-0371-4522-bfbf-61b159285100" />




```
# Load the image
image = cv2.imread('2.jpg')
image.shape
# Crop a 300x300 region starting from (50, 50)
roi = image[50:350, 50:350]  # Rows: 50-349, Columns: 50-349
# Convert BGR to RGB for displaying with Matplotlib
roi_rgb = cv2.cvtColor(roi, cv2.COLOR_BGR2RGB)
# Display the cropped region (ROI)
plt.imshow(roi_rgb)
plt.title("Cropped Region of Interest (ROI)")
plt.axis("off")
plt.show()
```

<img width="753" height="952" alt="image" src="https://github.com/user-attachments/assets/3698ec49-40e4-4c9d-aebe-30e94669c1b2" />




```
# Load the image
image = cv2.imread('2.jpg')
# Flip the image horizontally (left-right)
flipped_horizontally = cv2.flip(image, 1)
# Convert BGR to RGB for displaying with Matplotlib
flipped_horizontally_rgb = cv2.cvtColor(flipped_horizontally, cv2.COLOR_BGR2RGB)
# Horizontal flip
plt.imshow(flipped_horizontally_rgb)
plt.title("Flipped Horizontally")
plt.axis("off")
```

<img width="907" height="825" alt="image" src="https://github.com/user-attachments/assets/6332c406-3bcb-46cd-894a-15fbb3f091bd" />




```
# Flip the image vertically (up-down)
flipped_vertically = cv2.flip(image, 0)
# Convert BGR to RGB for displaying with Matplotlib
flipped_vertically_rgb = cv2.cvtColor(flipped_vertically, cv2.COLOR_BGR2RGB)# Vertical flip
plt.imshow(flipped_vertically_rgb)
plt.title("Flipped Vertically")
plt.axis("off")
```

<img width="1003" height="772" alt="image" src="https://github.com/user-attachments/assets/9e7ee901-4ed9-4cf5-ab0e-e5051a191d02" />


# Result:
Thus, the images were read, displayed, brightness and contrast adjustments were made, and bitwise operations were performed successfully using the Python program.
