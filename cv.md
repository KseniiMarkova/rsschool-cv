#**Markova Ksenia**

##**Contacts**
*__Email:__ kdmp4121@gmail.com

##**About me**
My goal is to learn the basic skills of working with web layout to replenish my resume.

##**Skills**
C #, Python

##**Code example**
```
import cv2
import numpy as np
img = cv2.imread("Harry.jpg", cv2.IMREAD_GRAYSCALE)
sift = cv2.xfeatures2d.SIFT_create()
surf = cv2.xfeatures2d.SURF_create()
orb = cv2.ORB_create(nfeatures=1500)
noise_strengths = [i for i in range(10)]
for strength in noise_strengths:
    mean = 0
    var = strength * 100
    sigma = var ** 0.5 
    gauss_noise1 = np.random.normal(mean, sigma, img.shape)
    print(strength,(np.min(gauss_noise1), np.max(gauss_noise1)))
    noisy1 = np.clip((img + gauss_noise1).astype(np.uint8), 0, 255)
    keypoints, descriptors = sift.detectAndCompute(img, None)
    img = cv2.drawKeypoints(img, keypoints, None)
    cv2.imshow("Image", img)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
```

##**Education**
*TPU
*ITMO

##**English level**
A2