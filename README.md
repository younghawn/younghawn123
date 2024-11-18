# go to my notion------>(https://www.notion.so/Nvidia-AI-Specialist-Certification-Report-13d83fc878fb804e86afffa1dbf8dce1)
# **[Title]**

---

## **AI-based clothing tag system for the visually impaired distinguishes front and back of clothing**

# Opening background information

---

- Visually impaired individuals often face challenges in distinguishing the front from the back of clothing when dressing. With the variety of modern clothing designs and materials, relying solely on tactile cues can be difficult. While some clothing brands incorporate raised tags or Braille to address this issue, these methods are not universally applied and may not always be easily detectable. This highlights the need for effective and inclusive solutions. AI technology offers a promising alternative, providing innovative ways to assist visually impaired individuals in overcoming this challenge.

# General description of the current project

---

- This project aims to develop an AI-based clothing tag system that helps visually impaired individuals easily identify the front and back of garments. Through a smartphone app or tag reader, the system provides audio guidance for clothing orientation, promoting independence and enhancing autonomy for users.

# Proposed Idea for Enhancements

---

- This project focuses on improving accessibility for visually impaired individuals by combining AI technology with a user-friendly smartphone app to identify garment orientation intuitively. The system’s versatility allows it to be applied in both home and public settings, contributing to a more inclusive society while delivering significant social value.

---

# (Image Acquisition Method**)**

- Clothing was filmed from various angles, resulting in one video for training and one videos three verification.

---

### **-Learning Data Images-**

https://youtube.com/shorts/6UiR7YuuXps

[]()

### **-Validation Data Images-**

https://youtube.com/shorts/Q09EUnH2wfE

https://youtube.com/shorts/pdQf36FB_kE

https://youtube.com/shorts/lRZ77K0CQGk

# **Project Progress**

## 1.**Image extraction**

---

- Images were extracted with a resolution of 640x640 using BabMix 2 (VAMIX_2).

![스크린샷 2024-11-13 112846.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/e8866741-e341-44c0-808a-bd3d3ddc73c7/ffd052df-5f94-4eac-9289-e8a1ffd59391/%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7_2024-11-13_112846.png)

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/e8866741-e341-44c0-808a-bd3d3ddc73c7/9c5ab3e3-430f-4036-91d9-2a8d9cbd9d9e/image.png)

## 2.**DarkLabel (labels)**

---

- **Go to the DarkLabel.exe file**

[1ITgGhs8udrKtSkqBUVv6GrFhcQTH3egS](https://drive.google.com/drive/folders/1ITgGhs8udrKtSkqBUVv6GrFhcQTH3egS)

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/e8866741-e341-44c0-808a-bd3d3ddc73c7/b24c09a2-e2db-474e-8c3b-cca7ae27f498/Untitled.png)

## 3.**DarkLabel (Setting Labeling Files)**

---

- **Create a class called my_classes2 and write the attribute ‘Front’ inside**

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/e8866741-e341-44c0-808a-bd3d3ddc73c7/d976279c-ecea-4fa7-9473-21e4094896f3/image.png)

---

- **In the Format1 class, write the classeset as my_classes2 and change the name to Front.**

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/e8866741-e341-44c0-808a-bd3d3ddc73c7/e95a23b0-0f18-4626-a921-8fd0b9acf6bf/image.png)

---

- **Write down the name 'Front' and check the path of the train and val.**

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/e8866741-e341-44c0-808a-bd3d3ddc73c7/4e572d8a-e650-4ccf-95b9-bb490d4e2d61/image.png)

## 4.**DarkLabel  (Extract DarkLabel Labeling Data)**

---

- **Press open video to get a learning video, click the 'Front' attribute value written earlier, and press Box+label. Label by pressing the space bar or the next and predict button. When labeling is finished, press the gt save as button to create a labeling file, and press the as image button to create an image file.**

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/e8866741-e341-44c0-808a-bd3d3ddc73c7/59207bd8-6636-424d-a5a7-1b3313de906e/image.png)

## 5.DarkLabel (**Check extracted labeling)**

---

- **You can see that the learned labeling value came out as a text file.(float value)**

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/e8866741-e341-44c0-808a-bd3d3ddc73c7/20771849-9a70-464e-83c2-b80fbd8d9a32/image.png)

[1D1Xv6Yth_cC2eS2fcLN6u_PcSNHvV7e-](https://drive.google.com/drive/folders/1D1Xv6Yth_cC2eS2fcLN6u_PcSNHvV7e-)

## 6. yolov5 (**Learning data with yolov5 colab)**

---

- Run Google colab and then connect to your own Google Drive.

![스크린샷 2024-11-13 230929.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/e8866741-e341-44c0-808a-bd3d3ddc73c7/75b9665a-310c-4f04-8d47-317f7fdb5d64/%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7_2024-11-13_230929.png)

## 7. yolov5 (install)

---

- Clone and install the yolov5 repertoire.

![설치.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/e8866741-e341-44c0-808a-bd3d3ddc73c7/0ab87139-4b85-4764-ac43-66c9a24736ed/%EC%84%A4%EC%B9%98.png)

## 8. (**Create Verification Data)**

![검증 데이터.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/e8866741-e341-44c0-808a-bd3d3ddc73c7/b853eeab-0a8f-41d8-b5fd-53d89dcb8b8a/%EA%B2%80%EC%A6%9D_%EB%8D%B0%EC%9D%B4%ED%84%B0.png)

---

- The `create_validation_set` function moves a
- It loads the list of training images, splits them into training and validation sets based on the `split_ratio`, then
- `train_test_split` is used`shutil.copy2` pe

## 9. (**Model Learning)**

![모델 학습.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/e8866741-e341-44c0-808a-bd3d3ddc73c7/3134a754-b505-4022-bca5-6c70f3f1b244/%EB%AA%A8%EB%8D%B8_%ED%95%99%EC%8A%B5.png)

---

- `python train.py` runs the training script for the YOLOv5 model.
- `-img 512`: sets the input image size to 512x512.
- `-batch 16`: sets the batch size to 16, defining the number of samples processed at once.
- `-epochs 300`: trains the model for a total of 300 epochs.
- `-data /content/drive/MyDrive/yolov5/yolov5/data.yaml`: specifies the path to the YAML file with dataset information.
- `-weights yolov5n.pt`: uses pretrained weights from the `yolov5n` (YOLOv5 nano) model to initialize training.
- `-cache`: caches the dataset in memory to speed up training.

![스크린샷 2024-11-13 231328.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/e8866741-e341-44c0-808a-bd3d3ddc73c7/294e6007-4db4-4d45-bdcf-383dd8b3e00a/%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7_2024-11-13_231328.png)

## 10.(result)

- (tensor board)

![스크린샷 2024-11-18 212655.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/e8866741-e341-44c0-808a-bd3d3ddc73c7/f73fc936-afd4-4783-854f-f5ca2e769e6f/%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7_2024-11-18_212655.png)

- Confusion Matrix

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/e8866741-e341-44c0-808a-bd3d3ddc73c7/3a76f3f4-d8f9-4917-b16f-4184550e9aad/image.png)

- F1-Curve

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/e8866741-e341-44c0-808a-bd3d3ddc73c7/80f80a9e-7269-4af3-becf-04e0a2ee1e35/image.png)

- labels_correlogram

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/e8866741-e341-44c0-808a-bd3d3ddc73c7/e6e9a142-5888-4db1-816c-002145514366/image.png)

- labels

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/e8866741-e341-44c0-808a-bd3d3ddc73c7/21ac0d2e-5e43-45b8-90ca-ffa95bb66afd/image.png)

- P-Curve

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/e8866741-e341-44c0-808a-bd3d3ddc73c7/d06730dd-cc04-4706-803d-26c2bb2faf39/image.png)

- Result

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/e8866741-e341-44c0-808a-bd3d3ddc73c7/1cb5dae2-57d8-42cf-b773-f89798bd93a2/image.png)

- Train batch 0,1,2

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/e8866741-e341-44c0-808a-bd3d3ddc73c7/179129fb-6c0e-4c4b-b1f3-ae76e7e3e5a5/image.png)

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/e8866741-e341-44c0-808a-bd3d3ddc73c7/529585c4-f5de-4eca-b450-44f743af070b/image.png)

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/e8866741-e341-44c0-808a-bd3d3ddc73c7/da132769-1775-4a04-8b4c-f9e866472704/image.png)

- Val batch,labels

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/e8866741-e341-44c0-808a-bd3d3ddc73c7/9e916bcf-eee6-419b-ae98-ece0a568d7e7/image.png)

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/e8866741-e341-44c0-808a-bd3d3ddc73c7/292bfc0a-c22e-477c-98e4-26dae8bb0e9a/image.png)

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/e8866741-e341-44c0-808a-bd3d3ddc73c7/2323e029-8e1c-466d-914e-8e3d3c115353/image.png)

- Val batch,labels

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/e8866741-e341-44c0-808a-bd3d3ddc73c7/3b2a6f9b-0a34-4dcf-be19-baed2fc1279a/image.png)

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/e8866741-e341-44c0-808a-bd3d3ddc73c7/daf1d3cb-a040-4495-8269-4749b3c867bd/image.png)

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/e8866741-e341-44c0-808a-bd3d3ddc73c7/0b064698-e462-427d-b1b6-bc749c409155/image.png)

## 11.(detect)

![탐지.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/e8866741-e341-44c0-808a-bd3d3ddc73c7/e875667e-2e39-41d4-b0f0-973fb0966270/%ED%83%90%EC%A7%80.png)

---

- When learning is completed in yolov5 to detect images.

![스크린샷 2024-11-18 212722.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/e8866741-e341-44c0-808a-bd3d3ddc73c7/72646810-7542-438f-8fa6-b0a337962b14/%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7_2024-11-18_212722.png)

## 12.(**detection video)**

https://youtube.com/shorts/Q09EUnH2wfE

https://youtube.com/shorts/pdQf36FB_kE

https://youtube.com/shorts/lRZ77K0CQGk

## 13.(**detection images)**

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/e8866741-e341-44c0-808a-bd3d3ddc73c7/d1cc5671-0ca7-44e3-853b-609e1499a2e2/image.png)

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/e8866741-e341-44c0-808a-bd3d3ddc73c7/c25ce500-6629-43a3-98dd-47938fc3733e/image.png)

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/e8866741-e341-44c0-808a-bd3d3ddc73c7/978bf2bf-9c9a-48b2-a83a-0a8ab7246018/image.png)

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/e8866741-e341-44c0-808a-bd3d3ddc73c7/7e377fcc-6f67-4d8b-b4d3-a632a7d64971/image.png)

## 14.(finish)

---

Through this project, we developed an AI-based clothing tag system that helps visually impaired individuals distinguish the front and back of garments, enabling them to identify clothing with ease and express their personal style more freely.

We would like to extend our heartfelt gratitude to everyone who contributed to the success of this project. First and foremost, we thank our professors and mentors for their invaluable guidance and technical support from the early stages of ideation through to the finer technical details. Their advice and encouragement provided us with the direction and confidence to advance the project successfully. We are also deeply grateful to the visually impaired associations and participants who dedicated their time to assist with data collection and system testing. Their invaluable feedback greatly enhanced the usability and effectiveness of our solution.

Finally, we want to express our sincere appreciation to our team members for their dedication and hard work. Despite numerous challenges, the support and collaboration we shared made it possible to complete this project successfully. We hope that this system will continue to evolve and offer meaningful support to the visually impaired community in the future.

Once again, thank you to everyone for your support and contributions to this project.

노션[(https://www.notion.so/Nvidia-AI-Specialist-Certification-Report-13d83fc878fb804e86afffa1dbf8dce1)](https://www.notion.so/Nvidia-AI-Specialist-Certification-Report-13d83fc878fb804e86afffa1dbf8dce1?pvs=21)

-(Thank you for reading)-
