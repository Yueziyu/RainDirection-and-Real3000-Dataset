# RainDirection-and-Real3000-Dataset
This repository contains an introduction and links to RainDirection and Real3000 datasets for paper "Unpaired Learning for Deep Image Deraining with Rain Direction Regularizer".  *Authors: Yang Liu, Ziyu Yue ,Jinshan Pan, Zhixun Su, Dalian University of Technology and Nanjing University of Science and Technology*. In the part about dataset of this work, I wrote a program to generate rainy images and rain streak maps with rain streak direction information in batches by imitating the process of PS rain making, and output their corresponding label files of rain streak direction information at the same time. And I collected 3,000 real world rain images with no ground truth from pictures and videos on the Internet.This work was published in the  IEEE International Conference on Computer Vision 2021(ICCV2021). You can get the paper from [here](https://openaccess.thecvf.com/content/ICCV2021/html/Liu_Unpaired_Learning_for_Deep_Image_Deraining_With_Rain_Direction_Regularizer_ICCV_2021_paper.html).
# Data overview
We have maked a new rainy dataset **RainDirection** with the direction information of rain streak and a new real world rainy dataset **Real3000**. You can download **RainDirection** and **Real3000** dataset from this [BaiduYun link](https://pan.baidu.com/s/1N5t3OzJngpcEozNeGYHjdg) (Extract code: 33e8).
## RainDirection
The RainDirection dataset is a synthetic rainy dataset. The rainy images in RainDirection are obtained by adding clean images from Flick2K and DIV2K dataset with synthetic labeled rain maps according to the rain model *O(x) = B(x)* + *R(x)*, and the rain streak map is obtained by the direction fuzzy kernel acting on the sparse Gaussian noise map. Each rainy image is assigned with a direction label, the horizontal Angle of the image is zero to the right and increases the angle counterclockwise. These direction labels are used to calculate the direction loss during training.  The training and test set of RainDirection contains 2920 and 430 images, respectively.  

<p align="center">  
  <img src="resources/0808.png" alt="Lizard" width="400"/> <img src="resources/0814.png" alt="Lizard" width="400"/><br>
</p>
<p align="center">
  <img src="resources/0853.png" alt="Lizard" width="400"/> <img src="resources/0858.png" alt="Lizard" width="400"/><br>
</p>  
    
The folder structure is as follows:    
  
  
    rainy_direction_dataset
      RainDirection2920train
          direction
              direction.txt
          latent
              1.png
              2.png
              ...
              ...
              2920.png
          rainy
              1.png
              2.png
              ...
              ...
              2920.png
          streak
              1.png
              2.png
              ...
              ...
              2920.png

      RainDirection430test
          direction
              direction.txt
          latent
              1.png
              2.png
              ...
              ...
              430.png
          rainy
              1.png
              2.png
              ...
              ...
              430.png
          streak
              1.png
              2.png
              ...
              ...
              430.png
## Real3000  
The Real3000 dataset contains 3000 real rainy images without ground truth images collected from the internet and captured by a Canon EOS 6D camera. The training
and test set contains 2700 and 300 diverse natural outdoor images, respectively. Images numbered 1705 to 2004 were selected as the test set.  

<p align="center">  
  <img src="resources/426.png" alt="Lizard" width="400"/> <img src="resources/464.png" alt="Lizard" width="400"/><br>
</p>
<p align="center">  
  <img src="resources/442.png" alt="Lizard" width="400"/> <img src="resources/560.png" alt="Lizard" width="400"/><br>
</p>
  
The folder structure is as follows:  


    real3000
      1.png
      2.png
      ...
      ...
      3000.png
## Citation:  
  
  
    @inproceedings{liu2021unpaired,
      title={Unpaired Learning for Deep Image Deraining With Rain Direction Regularizer},
      author={Liu, Yang and Yue, Ziyu and Pan, Jinshan and Su, Zhixun},
      booktitle={Proceedings of the IEEE/CVF International Conference on Computer Vision},
      pages={4753--4761},
      year={2021}
    }
## Contact:  
If you have any question, please email bubbleteapotzyyue@foxmail.com
