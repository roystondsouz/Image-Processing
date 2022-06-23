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

  
**3. develop a program to perform linear transformation. Rotation**<BR>
  import cv2<BR>
from PIL import Image
img=Image.open("plant4.jpg")<BR>
img=img.rotate(180)<BR>
img.show()<BR>
cv2.waitKey(0)<BR>
cv2.destroyAllWindows()<BR>

  **OUTPUT**<BR>
  ![174042633-31ed2a88-33e8-4f3e-9a90-0a1a721187b8](https://user-images.githubusercontent.com/98145297/175275653-ab0b3810-d5e9-4edb-865c-d00aff10d598.png)<BR>
  
**4. Develop a program to convert colour string to RGB color values.**<BR>
  
  from PIL import ImageColor<BR>
img1=ImageColor.getrgb("Yellow")<BR>
print(img1)<BR>
img2=ImageColor.getrgb("red")<BR>
print(img2)<BR>
 
 **OUTPUT**<BR>
(255, 255, 0)<BR>
(255, 0, 0) <BR>
  
**5. Write a program to create Image using programs.**  <BR>
  
  from PIL import Image<BR>
img=Image.new('RGB',(200,400),(255,255,0))<BR>
img.show()<BR>
  
**OUTPUT**<BR>
  
  ![174046289-402f6aa6-9029-4efc-97d7-09f1cfa62f2c](https://user-images.githubusercontent.com/98145297/175276686-a802ba7b-ea22-4d22-8a68-7b1eaca0c2ae.png)<BR>


**6. Develop a program to visualize the image using various color space.**<BR>
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
 
  **OUTPUT**
  
  ![174046770-58ad4a03-36f0-47ed-bb0b-2aa87b9b6147](https://user-images.githubusercontent.com/98145297/175281940-dfad1a6a-4509-4cf5-b642-eb50a6ca9901.png)
**<BR>![174046727-aa05f644-2482-4671-925f-b6f5ed75d095](https://user-images.githubusercontent.com/98145297/175281920-c7b6672d-0b1d-4b9a-bd91-72bcf1a5289f.png)

  
  
![174046823-471827fe-7b38-4614-879c-16660c9c7990](https://user-images.githubusercontent.com/98145297/175280792-bfd9c63b-0acd-4100-885d-8c93373150ae.png)

**7. Write a program to display the image attributes.**<BR>
  
  from PIL import Image<BR>
image=Image.open('plant4.jpg')<BR>
print("FileName: ",image.filename)<BR>
print("Format: ",image.format)<BR>
print("Mode: ",image.mode)<BR>
print("Size: ",image.size)<BR>
print("Width: ",image.width)<BR>
print("Height: ",image.height)<BR>
image.close();<BR>
**OUTPUT**<BR>
FileName: plant4.jpg<BR>
Format: JPEG<BR>
Mode: RGB<BR>
Size: (480, 720)<BR>
Width: 480<BR>
Height: 720<BR>
  
**8. Resize the original image.**<BR>
  
 import cv2<BR>
img=cv2.imread('flower5.jpg')<BR>
print('origial image length width',img.shape)<BR>
cv2.imshow('original image',img)<BR>
cv2.waitKey(0)<BR>
#to show the resized image<BR>
imgresize=cv2.resize(img,(150,160))<BR>
cv2.imshow('Resized image',imgresize)<BR>
print('Resized image length, width',imgresize.shape)<BR>
cv2.waitKey(0)<BR>
<BR>**OUTPUT**<BR>
origial image length width (640, 960, 3)<BR>
Resized image lenght width (160, 150, 3)<BR>
<BR>  
**9. Convert the original image to gray scale and then to binary.**<BR>
import cv2<BR>
#read the image file<BR>
img=cv2.imread('butterfly3.jpg')<BR>
cv2.imshow("RGB",img)<BR>
cv2.waitKey(0)<BR>

#Grayscale<BR>
<BR>
img=cv2.imread('butterfly3.jpg',0)<BR>
cv2.imshow("Gray",img)<BR>
cv2.waitKey(0)<BR>

#Binary image<BR>

ret,bw_img=cv2.threshold(img,127,255,cv2.THRESH_BINARY)<BR>
cv2.imshow("Binary",bw_img)<BR>
cv2.waitKey(0)<BR>
cv2.destroyAllWindows()<BR>
**OUTPUT**
  
![174048120-9fc7d698-0466-459c-a2bf-38816501be12](https://user-images.githubusercontent.com/98145297/175283116-69ecad53-cd8f-41e4-a13b-c1be6d5638ad.png)

  
![174048200-092e4aca-f297-492e-8af8-010b96b689dc](https://user-images.githubusercontent.com/98145297/175283136-84d6df80-1b53-4cb5-8bf3-6023078ae241.png)

  
![174048342-35f42e3d-bccf-4d8b-8b8f-44b19dd6182a](https://user-images.githubusercontent.com/98145297/175282802-fa368b84-bab0-4323-9203-9356ff8e3369.png)

**13.Develop the program to change the image to different color spaces.**<BR>
  
#Develop the program to change the image to different color spaces.<BR>
import cv2<BR>
img=cv2.imread("flower5.jpg")<BR>
gray=cv2.cvtColor(img,cv2.COLOR_BGR2GRAY)<BR>
hsv=cv2.cvtColor(img,cv2.COLOR_BGR2HSV)<BR>
lab=cv2.cvtColor(img,cv2.COLOR_BGR2LAB)<BR>
hls=cv2.cvtColor(img,cv2.COLOR_BGR2HLS)<BR>
yuv=cv2.cvtColor(img,cv2.COLOR_BGR2YUV)<BR>
cv2.imshow("GRAY image",gray)<BR>
cv2.imshow("HSV image",hsv)<BR>
cv2.imshow("LAB image",lab)<BR>
cv2.imshow("HLS image",hls)<BR>
cv2.imshow("YUV image",yuv)<BR>
cv2.waitKey(0)
cv2.destroyAllWindows()<BR>
  
**OUTPUT**<BR>
  

  
![175270342-85783a7b-7426-4963-8c35-cca4c75c8fe9](https://user-images.githubusercontent.com/98145297/175286867-c28e0b73-de7a-449b-aba5-5854d4d1d91b.png)<BR>
  
  
  ![175270746-5ea73ee1-aa46-4d09-9529-cf6ca35b1e35](https://user-images.githubusercontent.com/98145297/175286891-a32b7990-e0f5-4b9d-aa2e-864634d0c690.png)
![175270930-87dbe99b-4ce4-4300-a996-cfcb3ce2d7f0](https://user-images.githubusercontent.com/98145297/175286907-68b36de2-500a-4542-9a7a-89d4471f57df.png)<BR>

  
  
![175271007-9e6cc280-f7c2-494b-9fa4-0f70b0671b04](https://user-images.githubusercontent.com/98145297/175286918-d52dd7d9-e4cc-42fc-b9e9-870d66e33b69.png)<BR>
  

  ![175271082-f7c92ce4-161d-477f-8b4c-78a15af54dd2](https://user-images.githubusercontent.com/98145297/175286924-1587f0c3-fa1f-4cf8-9749-895d95abba36.png)<BR>

**14.Program to create an image using 2D array**.<BR>
import cv2 as c<BR>
import numpy as np<BR>
from PIL import Image<BR>
array=np.zeros([100,200,3],dtype=np.uint8)<BR>
array[:,:100]=[255,130,0]<BR>
array[:,100:]=[0,0,255]<BR>
img=Image.fromarray(array)<BR>
img.save('flower5.jpg')<BR>
img.show()<BR>
c.waitKey(0)<BR>

  **OUTPUT**<BR>
  ![175271426-a7f9f364-377a-4390-96df-e286e4bed715](https://user-images.githubusercontent.com/98145297/175287003-95572f56-12a1-421b-bcdf-2621846740b1.png)

  
