                    **IMAGE PROCESSING**
  
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
  
  
  Original size

  
  
  Resized
  
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
  
10.Develop a program to readimage using URL?<br>
from skimage import io<br>
import matplotlib.pyplot as plt<br>
url='https://www.alfredapp.com/blog/tips-and-tricks/tiny-png-workflow-compress-images/tinypng-panda.png'<br>
image=io.imread(url)<br>
plt.imshow(image)<br>
plt.show()<br>

output:<br>
![image](https://user-images.githubusercontent.com/87934584/175267752-1bb4a140-4b67-4c3b-a490-0dd6a8ab7388.png)<br>
11.
import cv2<br>
import matplotlib.image as mpimg<br>
import matplotlib.pyplot as plt<br>
img=mpimg.imread('images.jpg')<br>
plt.imshow(img)<br>
plt.show()<br>

![image](https://user-images.githubusercontent.com/87934584/175288897-b09f70dc-787b-4b19-beb5-aa9b54cb04cb.png)<br>

hsv_img=cv2.cvtColor(img,cv2.COLOR_RGB2HSV)<br>
light_orange=(0,50,50)<br>
dark_orange=(10,255,255)<br>
mask=cv2.inRange(hsv_img,light_orange,dark_orange)<br>
result=cv2.bitwise_and(img,img,mask=mask)<br>
plt.subplot(2,1,1)<br>
plt.imshow(mask,cmap="gray")<br>
plt.subplot(2,1,2)<br>
plt.imshow(result)<br>
plt.show()<br>
output:<br>
![image](https://user-images.githubusercontent.com/87934584/175289105-10541db3-c382-4f66-8dab-a73fbf23faa5.png)
![image](https://user-images.githubusercontent.com/87934584/175289116-33e1fd8a-8b01-4389-81ff-299755b1ebdf.png)<br>
light_white=(0,0,200)<br>
dark_white=(145,60,255)<br>
mask_white=cv2.inRange(hsv_img,light_white,dark_white)<br>
result_white=cv2.bitwise_and(img,img,mask=mask_white)<br>
plt.subplot(1,2,1)<br>
plt.imshow(mask_white,cmap="gray")<br>
plt.subplot(1,2,2)<br>
plt.imshow(result_white)<br>
plt.show()<br>

![image](https://user-images.githubusercontent.com/87934584/175289164-cc631749-91e1-4fc6-9ad2-03f093de4ab2.png)
![image](https://user-images.githubusercontent.com/87934584/175289196-4e81d1dc-b5c5-44d5-8545-7fbc9d6817f7.png)<br><br>
final_mask=mask+mask_white<br>
final_result=cv2.bitwise_and(img,img,mask=final_mask)<br>
plt.subplot(1,2,1)<br>
plt.imshow(final_mask,cmap="gray")<br>
plt.subplot(1,2,2)<br>
plt.imshow(final_result)<br>
plt.show()<br>

![image](https://user-images.githubusercontent.com/87934584/175289261-eab81fc0-4e8e-4266-9691-6410cbccc286.png)
![image](https://user-images.githubusercontent.com/87934584/175289283-ab0a0a56-c9b8-4d92-965b-ef3fa899d725.png)<br>
blur=cv2.GaussianBlur(final_result,(7,7),0)<br>
plt.imshow(blur)<br>
plt.show()<br>

![image](https://user-images.githubusercontent.com/87934584/175289334-3e3334c1-60fa-440b-8b80-ac5b9f636260.png)







12.Write a program to perform arithmatic operations on images?<br>
import cv2<br>
import matplotlib.image as mpimg<br>
import matplotlib.pyplot as plt<br>

*/reading imsge files/*<br>
*/image should be in same size but different img/*
img1=cv2.imread('goat.jpg')<br>
img2=cv2.imread('king.jpg')<br>

*/applying NumPy addition on images/*<br>
fimg1=img1+img2<br>
plt.imshow(fimg1)<br>
plt.show()<br>

*/saving the otput image/*<br>
cv2.imwrite('output.jpg',fimg1)<br>
fimg2=img1-img2<br>
plt.imshow(fimg2)<br>
plt.show()<br>


*/saving the output image/*<br>
cv2.imwrite('output.jpg',fimg2)<br>
fimg3=img1*img2<br>
plt.imshow(fimg3)<br>
plt.show()<br>

*/saving the output image/*<br>
cv2.imwrite('output.jpg',fimg3)<br>
fimg4 = img1 / img2<br>
plt.imshow(fimg4)<br>
plt.show()<br>

*/saving the output image/*<br>
cv2.imwrite('output.jpg',fimg4)<br>
output:<br>
![image](https://user-images.githubusercontent.com/87934584/175277477-3e87a4cf-031e-4283-8e10-ce7043cf7b94.png)
<br>
![image](https://user-images.githubusercontent.com/87934584/175277567-05318f3a-8ca8-41f4-9a80-e2281f9429f0.png)<br>
![image](https://user-images.githubusercontent.com/87934584/175277618-95bed0a2-fb71-424a-acae-24e245b5f218.png)<br>
![image](https://user-images.githubusercontent.com/87934584/175277676-573d6804-5892-414f-b67c-74302224c2a0.png)<br>


13.Develop the program to change the image into different color?<br>
import cv2<br>
img=cv2.imread("car.jpg")<br>
gray=cv2.cvtColor(img,cv2.COLOR_BGR2GRAY)<br>
hsv=cv2.cvtColor(img,cv2.COLOR_BGR2HSV)<br>
lab=cv2.cvtColor(img,cv2.COLOR_BGR2LAB)<br>
hls=cv2.cvtColor(img,cv2.COLOR_BGR2HLS)<br>
yuv=cv2.cvtColor(img,cv2.COLOR_BGR2YUV)<br>
cv2.imshow("GRAY image",gray)<br>
cv2.imshow("HSV image",hsv)<br>
cv2.imshow("LAB image",lab)<br>
cv2.imshow("HLS image",hls)<br>
cv2.imshow("YUV image",yuv)<br>
cv2.waitKey(0)<br>
cv2.destroyAllWindows()<br>
Output:<br>
![image](https://user-images.githubusercontent.com/87934584/175274437-7b2f1867-0376-4aeb-9952-d4d3ae43390c.png)<br>
![image](https://user-images.githubusercontent.com/87934584/175274546-c1a28c63-5fb3-40c7-9d1c-f154104a4bf3.png)<br>
![image](https://user-images.githubusercontent.com/87934584/175274629-e9b4f270-323a-497e-8455-eb20076ca287.png)<br>
![image](https://user-images.githubusercontent.com/87934584/175274748-e60c136d-7c75-4e3d-881f-92764fb0243d.png)<br>
![image](https://user-images.githubusercontent.com/87934584/175274893-754300ef-2708-493a-9cff-1ab252328f5a.png)<br>
14.Program to create an image using 2D array?
import cv2 as c<br>
import numpy as np<br>
from PIL import Image<br>
array=np.zeros([100,200,3],dtype=np.uint8)<br>
array[:,:100]=[255,130,0]<br>
array[:,100:]=[0,0,255]<br>
img=Image.fromarray(array)<br>
img.save('img1.png')<br>
img.show()<br>
c.waitKey(0)<br>
Output:<br>
![image](https://user-images.githubusercontent.com/87934584/175275363-32b08489-6317-4b74-8bc1-ff2d4261f2fd.png)

15.write program to perform bitwise operation?<br>
import cv2<br>
import matplotlib.pyplot as plt<br>
image1=cv2.imread('mardona.jpg',1)<br>
image2=cv2.imread('mardona.jpg')<br>
ax=plt.subplots(figsize=(15,10))<br>
bitwiseAnd=cv2.bitwise_and(image1,image2)<br>
bitwiseOr=cv2.bitwise_or(image1,image2)<br>
bitwiseXor=cv2.bitwise_xor(image1,image2)<br>
bitwiseNot_img1=cv2.bitwise_not(image1)<br>
bitwiseNot_img2=cv2.bitwise_not(image2)<br>
plt.subplot(151)<br>
plt.imshow(bitwiseAnd)<br>
plt.subplot(152)<br>
plt.imshow(bitwiseOr)<br>
plt.subplot(153)<br>
plt.imshow(bitwiseXor)<br>
plt.subplot(154)<br>
plt.imshow(bitwiseNot_img1)<br>
plt.subplot(155)<br>
plt.imshow(bitwiseNot_img2)<br>
cv2.waitKey(0)<br>
output:<br>![image](https://user-images.githubusercontent.com/87934584/176419794-150537e0-33d5-40a0-9d3f-a90f0e6b8c81.png)<br>
16.Blurring image?<br>
import cv2<br>
import numpy as np<br>

image=cv2.imread('pand.jpg')<br>
cv2.imshow('original image',image)<br>

*/Gaussian blur<br>
Gaussian=cv2.GaussianBlur(image,(7,7),0)<br>
cv2.imshow('Gaussian Blurring',Gaussian)<br>


*/Median Blur<br>
median=cv2.medianBlur(image,5)<br>
cv2.imshow('MediaN Blurring',median)<br>


*/Billateral Blur<br>
bilateral=cv2.bilateralFilter(image,9,75,75)<br>
cv2.imshow('Bilateral Blurring',bilateral)<br>
cv2.waitKey(0)<br>
cv2.destroyAllWindows()<br>
output:<br>
![image](https://user-images.githubusercontent.com/87934584/176423729-31495072-a7ea-475e-964f-1b9e4387feaf.png)

![image](https://user-images.githubusercontent.com/87934584/176423387-3e9038a1-30a3-4890-90c9-e878ade379ed.png)

![image](https://user-images.githubusercontent.com/87934584/176423231-fd583b5d-3792-4d02-bfaf-8ec1a231a0e1.png)<br>

![image](https://user-images.githubusercontent.com/87934584/176422811-5f8a3ee0-3a9f-411c-8505-a8140fcfb289.png)

17.Image Enhancement?<br>
from PIL import Image<br>
from PIL import ImageEnhance<br>
image=Image.open('pand.jpg')<br>
image.show()<br>
enh_bri=ImageEnhance.Brightness(image)<br>
brightness=1.5<br>
image_brightened=enh_bri.enhance(brightness)<br>
image_brightened.show()<br>
enh_col=ImageEnhance.Color(image)<br>
color=1.5
image_colored=enh_col.enhance(color)<br>
image_colored.show()<br>
enh_con=ImageEnhance.Contrast(image)<br>
contrast=1.5<br>
image_contrasted=enh_con.enhance(contrast)<br>
image_contrasted.show()<br>
enh_sha=ImageEnhance.Sharpness(image)<br>
sharpness=3.0<br>
image_sharped=enh_sha.enhance(sharpness)<br>
image_sharped.show()
output:<br>
![image](https://user-images.githubusercontent.com/87934584/176424845-7c3315f0-53a8-4db0-b228-8bdf2adcf282.png)
![image](https://user-images.githubusercontent.com/87934584/176424920-1ba63638-82be-4028-aa60-7c26b51ebe54.png)
![image](https://user-images.githubusercontent.com/87934584/176424993-ac049a5b-47d5-459b-b87e-26e51e9c9210.png)
![image](https://user-images.githubusercontent.com/87934584/176425061-f4f3cdeb-519c-465e-97ab-81a362698339.png)
![image](https://user-images.githubusercontent.com/87934584/176425182-c9ff2164-c4c4-4514-82b2-99bddd97ff7d.png)

18.Morphological_operation<br>
import cv2<br>
import numpy as np<br>
from matplotlib import pyplot as plt<br>
from PIL import Image,ImageEnhance<br>
img=cv2.imread('mardona.jpg',0)<br>
ax=plt.subplots(figsize=(20,10))<br>
kernel=np.ones((5,5),np.uint8)<br>
opening=cv2.morphologyEx(img,cv2.MORPH_OPEN,kernel)<br>
closing=cv2.morphologyEx(img,cv2.MORPH_CLOSE,kernel)<br>
erosion=cv2.erode(img,kernel,iterations=1)<br>
dilation=cv2.dilate(img,kernel,iterations=1)<br>
gradient=cv2.morphologyEx(img,cv2.MORPH_GRADIENT,kernel)<br>
plt.subplot(151)<br>
plt.imshow(opening)<br>
plt.subplot(152)<br>
plt.imshow(closing)<br>
plt.subplot(153)<br>
plt.imshow(erosion)<br>
plt.subplot(154)<br>
plt.imshow(dilation)<br>
plt.subplot(155)<br>
plt.imshow(gradient)<br>
cv2.waitKey(0)<br>
output:<br>
![image](https://user-images.githubusercontent.com/87934584/176426007-2731e985-46f2-4920-b34e-8332586675be.png)

19.slicing with background ?<br>
import cv2<br>
import numpy as np<br>
from matplotlib import pyplot as plt<br>
image=cv2.imread('dore.jpg',0)<br>
x,y=image.shape<br>
z=np.zeros((x,y))<br>
for i in range(0,x):<br>
    for j in range(0,y):<br>
        if(image[i][j]>50 and image[i][j]<150):<br>
            z[i][j]=255<br>
        else:<br>
            z[i][j]=image[i][j]<br>
equ=np.hstack((image,z))<br>
plt.title('Graylevel slicing with background')<br>
plt.imshow(equ,'gray')<br>
plt.show()<br>

output:<br>![image](https://user-images.githubusercontent.com/87934584/178711477-8b08ac1d-83ec-4d8c-a478-bd092a3a37ac.png)

20.Graylevel slicing without background?
import cv2<br>
import numpy as np<br>
from matplotlib import pyplot as plt<br>
image=cv2.imread('dore.jpg',0)<br>
x,y=image.shape<br>
z=np.zeros((x,y))<br>
for i in range(0,x):<br>
    for j in range(0,y):
        if(image[i][j]>50 and image[i][j]<150):<br>
            z[i][j]=255<br>
        else:<br>
            z[i][j]=0<br>
equ=np.hstack((image,z))<br>
plt.title('Graylevel slicing without background')<br>
plt.imshow(equ,'gray')<br>
plt.show()<br>

output:<br>![image](https://user-images.githubusercontent.com/87934584/178711943-dc482981-3b05-4c0a-b650-a160d6c6e34c.png)


