**IMAGE PROCESSING**<BR>

**1. Develop a program to display grayscale image using read and write operation.**<BR>
pip install opencv-python<BR>
import cv2<BR>
img=cv2.imread('flower5.jpg',0)<BR>
cv2.imshow('image',img)<BR>
cv2.waitKey(0)<BR>
cv2.destroyAllWindows()<BR>

**OUTPUT**

![174041726-df4b96be-11b2-4f5a-b4b9-aee932a7be26](https://user-images.githubusercontent.com/98145297/175274035-294e0072-cbfe-401a-9071-261287760dfd.png)

**2. Develop a program to display the image using matplotlib.**
  import matplotlib.image as mping
import matplotlib.pyplot as plt
img=mping.imread('plant4.jpg')
plt.imshow(img)
  
  **OUTPUT**
  ![174042162-a75f11ae-0ea3-4885-ae30-ff9720232530](https://user-images.githubusercontent.com/98145297/175275091-97edf2c2-ee5d-4fdf-b351-93f8fa21e849.png)

  
** 3. develop a program to perform linear transformation. Rotation**
  import cv2
from PIL import Image
img=Image.open("plant4.jpg")
img=img.rotate(180)
img.show()
cv2.waitKey(0)
cv2.destroyAllWindows()

  **OUTPUT**
  ![174042633-31ed2a88-33e8-4f3e-9a90-0a1a721187b8](https://user-images.githubusercontent.com/98145297/175275653-ab0b3810-d5e9-4edb-865c-d00aff10d598.png)
  

  
  
  

 
  
