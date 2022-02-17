# MangoDeblurGAN
## Abstact

1. The raw data of the mango image is blurry and unclear. Therefore this project aims to make the mango picture more clear and hopes to improve classification accuracy.
2. I found that none of the state-of-the-art models can generate a clear mango image very well. Therefore, I want to build my own model to solve this problem.

## Method
By combining two models with different training dataset
1. DeblurGAN: https://github.com/KupynOrest/DeblurGAN
2. ESRGAN: https://github.com/xinntao/ESRGAN

## Architecture
![image](https://user-images.githubusercontent.com/56544982/143666792-b74935c6-282b-48ad-ad5b-ad2d23a878f9.png)


## Requirement
1. Python
2. Opencv
3. Please refer to the README of the following URL:
<br> - https://github.com/KupynOrest/DeblurGAN
<br> - https://github.com/xinntao/ESRGAN


## Step

1. Clear mango is in data\train\clear
2. Run image_blurring.ipynb to generate motion-blurred mango from clear mango, and put it into data\train\motionblur
3. Train DeblurGAN with motion blurred mango and clear mango
4. Run image_blurring.ipynb to generate gaussian blurred mango from clear mango, and put it into data\train\gaussianblur
5. Train ESRGAN model with gaussian-blurred mango and clear mango
6. Test the result by using raw mango image from data\test

## Result
Order from left to right: raw image, after DeblurGAN, after ESRGAN

![image](https://user-images.githubusercontent.com/56544982/143666901-d528c66e-d979-45f9-aa3d-0366fb065f93.png)

## Reference
1. https://github.com/KupynOrest/DeblurGAN
2. https://github.com/xinntao/ESRGAN




