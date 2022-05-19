# Salient_Object_Detection
Salient objection detection (SOD) is a method trying to depict boundary of object, therefore seperating the background and target. Our propose was to research SOD algorithm and applied it to the auto checkout counter, which was a project in collaboration with Ministry of Technology in Taiwan. Network was trained to learn how to differentiate pixels in images to whether it was objects. In case that this model was to classify images shot by phones, we modified the input to better normalize the scales. This brought about 10% of enhancement since the trained checkpoint could fit more closely to applied images. Besides, we researched on the contribution about how the environment impacted the object distinguishment. The result implied that SOD could not easily classify objects with depth (z-axis). Therefore, we attempted to compare images with various angles and determine the consequence with the least noise.

## Training Procedure
We firstly pre-trained this model with ImageNet database. This gave us a robust model in return. We subsequently utilized dataset composed of images from camera to reinforce the prediction behavior. The additional training had 100 more epochs with other settings remained the same as training with ImageNet.

*Self Training Dataset Link: https://drive.google.com/drive/folders/1Lwqg37ICnIENR78TwUut48TiylXzWM2E?usp=sharing*

*Checkpoint file: https://drive.google.com/file/d/1w1DKS2_DHnkisedI8SwHpPtM_5nfR85i/view?usp=sharing*

## Testing Result
We put a batch of testing images in the directories. The classification in overall performed well, but we realized there existed blurring boundary once two objects were too close to each other. In our report, we concluded the reason causing this problem that the depicting box (bounding box) was overlapped that model possibly thought it as a whole. In addition, we changed several backgrounds eager to observe how the background noise influencing the result. Combining with above-mentioned contributions, we pointed out some reasons prone to affect the behavior.
- Depth of Focos (DoF) 
- Reflectiveness of Light
- Displacement between Objects
- Object's Color Constractness
- Normalized Scale Change in Images

## Contact Info
Author: Chun-Sheng Wu, MS student in Computer Engineering @ Texas A&M University  
Email: jinsonwu@tamu.edu  
LinkedIn: https://www.linkedin.com/in/chunshengwu/

*This project was in collaboration with Ministry of Technology in Taiwan and conducted with Jung-Te Lin under the supervision of Dr. Jiun-In Guo at Intelligent Vision Lab, National Chiao Tung University*
