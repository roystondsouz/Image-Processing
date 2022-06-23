**IMAGE PROCESSING**

**1. Develop a program to display grayscale image using read and write operation.**
pip install opencv-python
import cv2
img=cv2.imread('flower5.jpg',0)
cv2.imshow('image',img)
cv2.waitKey(0)
cv2.destroyAllWindows()

**OUTPUT**

![174041726-df4b96be-11b2-4f5a-b4b9-aee932a7be26](https://user-images.githubusercontent.com/98145297/175274035-294e0072-cbfe-401a-9071-261287760dfd.png)
