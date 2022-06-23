**IMAGE PROCESSING**<BR>

**1. Develop a program to display grayscale image using read and write operation.**<BR>
pip install opencv-python<BR>
import cv2<BR>
img=cv2.imread('flower5.jpg',0)<BR>
cv2.imshow('image',img)<BR>
cv2.waitKey(0)<BR>
cv2.destroyAllWindows()<BR>

**OUTPUT**<BR>

![174041726-df4b96be-11b2-4f5a-b4b9-aee932a7be26](https://user-images.githubusercontent.com/98145297/175274035-294e0072-cbfe-401a-9071-261287760dfd.png)<BR>

**2. Develop a program to display the image using matplotlib.**<BR>
  import matplotlib.image as mping<BR>
import matplotlib.pyplot as plt<BR>
img=mping.imread('plant4.jpg')<BR>
plt.imshow(img)<BR>
  
  **OUTPUT**<BR>
  ![174042162-a75f11ae-0ea3-4885-ae30-ff9720232530](https://user-images.githubusercontent.com/98145297/175275091-97edf2c2-ee5d-4fdf-b351-93f8fa21e849.png)<BR>

  
** 3. develop a program to perform linear transformation. Rotation**<BR>
  import cv2<BR>
from PIL import Image
img=Image.open("plant4.jpg")<BR>
img=img.rotate(180)<BR>
img.show()<BR>
cv2.waitKey(0)<BR>
cv2.destroyAllWindows()<BR>

  **OUTPUT**<BR>
  ![174042633-31ed2a88-33e8-4f3e-9a90-0a1a721187b8](https://user-images.githubusercontent.com/98145297/175275653-ab0b3810-d5e9-4edb-865c-d00aff10d598.png)<BR>
  
**  4. Develop a program to convert colour string to RGB color values.**<BR>
  
  from PIL import ImageColor<BR>
img1=ImageColor.getrgb("Yellow")<BR>
print(img1)<BR>
img2=ImageColor.getrgb("red")<BR>
print(img2)<BR>
 
 **OUTPUT**<BR>
(255, 255, 0)<BR>
(255, 0, 0) <BR>
  
** 5. Write a program to create Image using programs. **  <BR>
  
  from PIL import Image<BR>
img=Image.new('RGB',(200,400),(255,255,0))<BR>
img.show()<BR>
  
**OUTPUT**<BR>
  
  ![174046289-402f6aa6-9029-4efc-97d7-09f1cfa62f2c](https://user-images.githubusercontent.com/98145297/175276686-a802ba7b-ea22-4d22-8a68-7b1eaca0c2ae.png)<BR>


** 6. Develop a program to visualize the image using various color space.**<BR>
  import cv2<BR>
import matplotlib.pyplot as plt<BR>
import numpy as np<BR>
img=cv2.imread('butterfly3.jpg')<BR>
plt.imshow(img)<BR>
plt.show()<BR>
img=cv2.cvtColor(img,cv2.COLOR_BGR2RGB)<BR>
plt.imshow(img)<BR>
plt.show()<BR>

img=cv2.cvtColor(img,cv2.COLOR_RGB2HSV)<BR>
plt.imshow(img)<BR>
plt.show()<BR>
 
  **OUTPUT**<BR>
  ![174046727-aa05f644-2482-4671-925f-b6f5ed75d095](https://user-images.gith![174046770-58ad4a03-36f0-47ed-bb0b-2aa87b9b6147](https://user-images.githubusercontent.com/98145297/175280757-6f0e6593-9583-4fee-b229-c514f1bfa9da.png)
ubusercontent.com/98145297/175280738-8b872350-de2f-47a8-a6ba-8c06cc62de53.png)<BR>

![174046823-471827fe-7b38-4614-879c-16660c9c7990](https://user-images.githubusercontent.com/98145297/175280792-bfd9c63b-0acd-4100-885d-8c93373150ae.png)

