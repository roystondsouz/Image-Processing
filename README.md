**IMAGE PROCESSING**<BR>
  
  **1.Develop a program to?**
(i) Read the image, convert it into grayscale image
(ii) write (save) the grayscale image and
(iii) display the original image and grayscale image**
  
  (Note: To save image to local storage using Python, we use cv2.imwrite() function on OpenCV library
  
  import cv2
OriginalImg=cv2.imread('free.jpg')
GrayImg=cv2.imread('free.jpg',0)
isSaved=cv2.imwrite('E:\yathin\i.jpg',GrayImg)
cv2.imshow('Display Original image',OriginalImg)
cv2.imshow('Display Grayscale image',GrayImg)
cv2.waitKey(0)
cv2.destroyAllWindows()
if isSaved:
print('The image is successfully saved')
  
  **output:**
![178705842-a27299a7-79be-4dc2-ac82-25986221ff66](https://user-images.githubusercontent.com/98145297/178951319-1dfc367e-01cc-4ac3-bee3-9aab58941556.png)

  ![178705947-fa4d6355-967b-44a8-977e-83896ddc348a](https://user-images.githubusercontent.com/98145297/178951333-d25388f8-1347-45b1-ad92-d1b9ffe0b54c.png)

  
  
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
  
**  10.Develop a program to readimage using URL?**
  
 from skimage import io
import matplotlib.pyplot as plt
url='https://www.alfredapp.com/blog/tips-and-tricks/tiny-png-workflow-compress-images/tinypng-panda.png'
image=io.imread(url)
plt.imshow(image)
  **output**
  ![175267752-1bb4a140-4b67-4c3b-a490-0dd6a8ab7388](https://user-images.githubusercontent.com/98145297/178954935-97908ab5-65e2-40fd-b0ab-581f6f567f86.png)

  11. import cv2
import matplotlib.image as mpimg
import matplotlib.pyplot as plt
img=mpimg.imread('images.jpg')
plt.imshow(img)
plt.show()

  ![175288897-b09f70dc-787b-4b19-beb5-aa9b54cb04cb](https://user-images.githubusercontent.com/98145297/178955160-57d13ef7-6865-4e90-8626-c770a5b045a2.png)

hsv_img=cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
light_orange=(0,50,50)
dark_orange=(10,255,255)
mask=cv2.inRange(hsv_img,light_orange,dark_orange)
result=cv2.bitwise_and(img,img,mask=mask)
plt.subplot(2,1,1)
plt.imshow(mask,cmap="gray")
plt.subplot(2,1,2)
plt.imshow(result)
plt.show()
  
  **output**
  
  
   ![175289105-10541db3-c382-4f66-8dab-a73fbf23faa5](https://user-images.githubusercontent.com/98145297/178955414-9235e926-2854-4c62-8cf6-eed95e8e0dcb.png)

  
   ![175289116-33e1fd8a-8b01-4389-81ff-299755b1ebdf](https://user-images.githubusercontent.com/98145297/178955432-7f7a057d-7496-466f-8852-f70fb3f5b5fc.png)

  light_white=(0,0,200)
dark_white=(145,60,255)
mask_white=cv2.inRange(hsv_img,light_white,dark_white)
result_white=cv2.bitwise_and(img,img,mask=mask_white)
plt.subplot(1,2,1)
plt.imshow(mask_white,cmap="gray")
plt.subplot(1,2,2)
plt.imshow(result_white)
plt.show()
  
  **Output**
  
  ![175289164-cc631749-91e1-4fc6-9ad2-03f093de4ab2](https://user-images.githubusercontent.com/98145297/178955802-fb0d5647-da80-46f0-bdd1-92e320b67e64.png)

  ![175289196-4e81d1dc-b5c5-44d5-8545-7fbc9d6817f7](https://user-images.githubusercontent.com/98145297/178955815-71a4b48e-9ad0-4bac-8c05-f7d968e86f83.png)

  
  final_mask=mask+mask_white
final_result=cv2.bitwise_and(img,img,mask=final_mask)
plt.subplot(1,2,1)
plt.imshow(final_mask,cmap="gray")
plt.subplot(1,2,2)
plt.imshow(final_result)
plt.show()
  
  
   
  ![175289261-eab81fc0-4e8e-4266-9691-6410cbccc286](https://user-images.githubusercontent.com/98145297/178955921-6f60933a-d7b7-4591-aab4-187557bd7e09.png)

  
  
  
  ![175289283-ab0a0a56-c9b8-4d92-965b-ef3fa899d725](https://user-images.githubusercontent.com/98145297/178955940-ea95cb77-431b-48b4-b5b6-712d973fdc4e.png)

  
  blur=cv2.GaussianBlur(final_result,(7,7),0)
plt.imshow(blur)
plt.show()
  

  ![175289334-3e3334c1-60fa-440b-8b80-ac5b9f636260](https://user-images.githubusercontent.com/98145297/178955991-b913e65b-59f7-4d36-a610-ec6c51c874c4.png)

  

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

  
**15.write program to perform bitwise operation?**
  import cv2
import matplotlib.pyplot as plt
image1=cv2.imread('mardona.jpg',1)
image2=cv2.imread('mardona.jpg')
ax=plt.subplots(figsize=(15,10))
bitwiseAnd=cv2.bitwise_and(image1,image2)
bitwiseOr=cv2.bitwise_or(image1,image2)
bitwiseXor=cv2.bitwise_xor(image1,image2)
bitwiseNot_img1=cv2.bitwise_not(image1)
bitwiseNot_img2=cv2.bitwise_not(image2)
plt.subplot(151)
plt.imshow(bitwiseAnd)
plt.subplot(152)
plt.imshow(bitwiseOr)
plt.subplot(153)
plt.imshow(bitwiseXor)
plt.subplot(154)
plt.imshow(bitwiseNot_img1)
plt.subplot(155)
plt.imshow(bitwiseNot_img2)
cv2.waitKey(0)
  
  **OUTPUT**
  
  ![176419794-150537e0-33d5-40a0-9d3f-a90f0e6b8c81](https://user-images.githubusercontent.com/98145297/178956860-bae954e4-7639-4c3e-8d69-1a4c7a13305f.png)

  **16.Blurring image?**
  import cv2
import numpy as np

image=cv2.imread('pand.jpg')
cv2.imshow('original image',image)

*/Gaussian blur
Gaussian=cv2.GaussianBlur(image,(7,7),0)
cv2.imshow('Gaussian Blurring',Gaussian)

*/Median Blur
median=cv2.medianBlur(image,5)
cv2.imshow('MediaN Blurring',median)

*/Billateral Blur
bilateral=cv2.bilateralFilter(image,9,75,75)
cv2.imshow('Bilateral Blurring',bilateral)
cv2.waitKey(0)
cv2.destroyAllWindows()
  
  **Output**
 
  
![176423729-31495072-a7ea-475e-964f-1b9e4387feaf](https://user-images.githubusercontent.com/98145297/178957045-90645970-c16d-4acf-be97-f923c3917216.png)
  
  
![176423387-3e9038a1-30a3-4890-90c9-e878ade379ed](https://user-images.githubusercontent.com/98145297/178957131-820b7fbd-a9b2-4f1b-909e-7299545cb8b7.png)
  
  
  
![176423231-fd583b5d-3792-4d02-bfaf-8ec1a231a0e1](https://user-images.githubusercontent.com/98145297/178957154-58d741a6-c000-4e17-aeb1-1939ffaa09c4.png)
  
  
![176422811-5f8a3ee0-3a9f-411c-8505-a8140fcfb289](https://user-images.githubusercontent.com/98145297/178957213-0d271cae-f736-44e2-beda-0ae853e5a93c.png)
  
  **17.Image Enhancement?**
  from PIL import Image
from PIL import ImageEnhance
image=Image.open('pand.jpg')
image.show()
enh_bri=ImageEnhance.Brightness(image)
brightness=1.5
image_brightened=enh_bri.enhance(brightness)
image_brightened.show()
enh_col=ImageEnhance.Color(image)
color=1.5 image_colored=enh_col.enhance(color)
image_colored.show()
enh_con=ImageEnhance.Contrast(image)
contrast=1.5
image_contrasted=enh_con.enhance(contrast)
image_contrasted.show()
enh_sha=ImageEnhance.Sharpness(image)
sharpness=3.0
image_sharped=enh_sha.enhance(sharpness)
image_sharped.show()
  
  **Output**
    
  
![176424920-1ba63638-82be-4028-aa60-7c26b51ebe54](https://user-images.githubusercontent.com/98145297/178957798-b7f44e98-064f-44cc-b807-9e43939d7fd6.png)

  
  
  
