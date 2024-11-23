# go to my notion------>(https://tattered-innocent-ff2.notion.site/Nvidia-AI-Specialist-Certification-Report-13d83fc878fb804e86afffa1dbf8dce1)
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

<img width="446" alt="%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7_2024-11-13_112846" src="https://github.com/user-attachments/assets/ad7cc0f0-2915-47d3-8a07-0ffe1598851c">

![image](https://github.com/user-attachments/assets/f4a923a3-cd78-4e5f-bf68-058d176dce55)

## 2.**DarkLabel (labels)**

---

- **Go to the DarkLabel.exe file**

[1ITgGhs8udrKtSkqBUVv6GrFhcQTH3egS](https://drive.google.com/drive/folders/1ITgGhs8udrKtSkqBUVv6GrFhcQTH3egS)

![Untitled](https://github.com/user-attachments/assets/1c8343f7-6923-44d1-a23d-5c6b8bd3d417)

## 3.**DarkLabel (Setting Labeling Files)**

---

- **Create a class called my_classes2 and write the attribute ‘Front’ inside**

![image 1](https://github.com/user-attachments/assets/348c62c2-5cc3-4c17-987d-08d781902973)

---

- **In the Format1 class, write the classeset as my_classes2 and change the name to Front.**

![image 2](https://github.com/user-attachments/assets/1923344b-c99e-43bb-a570-6ba302c981f3)

---

- **Write down the name 'Front' and check the path of the train and val.**

![image 3](https://github.com/user-attachments/assets/978cce48-c94a-47f1-8bee-57471759b24e)

## 4.**DarkLabel  (Extract DarkLabel Labeling Data)**

---

- **Press open video to get a learning video, click the 'Front' attribute value written earlier, and press Box+label. Label by pressing the space bar or the next and predict button. When labeling is finished, press the gt save as button to create a labeling file, and press the as image button to create an image file.**

![image 4](https://github.com/user-attachments/assets/e3c8b379-603e-4504-8893-0aeb840e2f50)

## 5.DarkLabel (**Check extracted labeling)**

---

- **You can see that the learned labeling value came out as a text file.(float value)**

![image 5](https://github.com/user-attachments/assets/b0844fe1-a965-4c61-94eb-5c138db1a25a)

--------------> (Darklabel2.4 file)  [1D1Xv6Yth_cC2eS2fcLN6u_PcSNHvV7e-](https://drive.google.com/drive/folders/1D1Xv6Yth_cC2eS2fcLN6u_PcSNHvV7e-)

## 6. yolov5 (**Learning data with yolov5 colab)**

---

- Run Google colab and then connect to your own Google Drive.

![%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7_2024-11-13_230929](https://github.com/user-attachments/assets/24f6528b-88a3-4efb-9b1d-831e4cba32af)

## 7. yolov5 (install)

---

- Clone and install the yolov5 repertoire.

![%EC%84%A4%EC%B9%98](https://github.com/user-attachments/assets/535401b7-f738-4861-a928-0232d7cfb4a6)
## 8. (**Create Verification Data)**

![%EA%B2%80%EC%A6%9D_%EB%8D%B0%EC%9D%B4%ED%84%B0](https://github.com/user-attachments/assets/d73cf92c-c3f5-42ff-a4ee-3149c18635f9)

---

- The `create_validation_set` function moves a
- It loads the list of training images, splits them into training and validation sets based on the `split_ratio`, then
- `train_test_split` is used`shutil.copy2` pe

## 9. (**Model Learning)**

![%EB%AA%A8%EB%8D%B8_%ED%95%99%EC%8A%B5](https://github.com/user-attachments/assets/11c74434-4514-4c72-93d1-6630d9cb60a4)
---

- `python train.py` runs the training script for the YOLOv5 model.
- `-img 512`: sets the input image size to 512x512.
- `-batch 16`: sets the batch size to 16, defining the number of samples processed at once.
- `-epochs 300`: trains the model for a total of 300 epochs.
- `-data /content/drive/MyDrive/yolov5/yolov5/data.yaml`: specifies the path to the YAML file with dataset information.
- `-weights yolov5n.pt`: uses pretrained weights from the `yolov5n` (YOLOv5 nano) model to initialize training.
- `-cache`: caches the dataset in memory to speed up training.

![%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7_2024-11-13_231328](https://github.com/user-attachments/assets/32bf7eef-4421-4026-b9c6-ba98f6dab064)

## 10.(result)

- (tensor board)

![%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7_2024-11-18_212655](https://github.com/user-attachments/assets/f67a4d41-5f0c-42dc-a00a-2adddb827595)

- Confusion Matrix

![image 6](https://github.com/user-attachments/assets/2887e562-9c19-4dce-bf3e-7af3602bc985)

- F1-Curve

![image 7](https://github.com/user-attachments/assets/59eca1b2-4bf5-4198-98cf-3591ccb1df68)

- labels_correlogram

![image 8](https://github.com/user-attachments/assets/44c79b8b-3de3-4a9c-986f-fe6018e4adc9)

- labels

![image 9](https://github.com/user-attachments/assets/ef2d7b14-3f3a-4a33-9a4b-d7dc049434b2)

- P-Curve

![image 10](https://github.com/user-attachments/assets/e447f3f9-dfef-46a5-9141-e377c0ae8729)

- Result

![image 11](https://github.com/user-attachments/assets/0d80fb3e-b9e9-404a-b680-eeece7122a0c)

- Train batch 0,1,2

![image 12](https://github.com/user-attachments/assets/ddf296c6-783f-4374-bde5-e38546deb2de)

![image 13](https://github.com/user-attachments/assets/32a3024e-f3a2-445e-90e5-b4764e67101a)

![image 14](https://github.com/user-attachments/assets/b3a3cb09-7070-4323-8c98-0079c24bb050)

- Val batch,labels

![image 15](https://github.com/user-attachments/assets/89cb3a7e-4d4b-4423-9eb6-5563188c9d9f)

![image 16](https://github.com/user-attachments/assets/9e874e78-507c-4c9b-8017-45251b42a457)

![image 17](https://github.com/user-attachments/assets/f45c3f6e-00e0-4b32-a087-73a5e1325be4)

- Val batch,labels

![image 18](https://github.com/user-attachments/assets/5e31e171-de30-4ea0-be27-ca6f99a0517c)

![image 19](https://github.com/user-attachments/assets/3624297f-7702-4217-ae77-18489681b2ec)

![image 20](https://github.com/user-attachments/assets/84a51d41-1024-4741-87e2-1723c94b4d2c)

## 11.(detect)

---

- When learning is completed in yolov5 to detect images.

![%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7_2024-11-18_212722](https://github.com/user-attachments/assets/543c6e1f-3244-4029-b3c8-df370e865835)

## 12.(**detection video)**

https://youtube.com/shorts/Q09EUnH2wfE

https://youtube.com/shorts/pdQf36FB_kE

https://youtube.com/shorts/lRZ77K0CQGk

## 13.(**detection images)**

![image 21](https://github.com/user-attachments/assets/9da5ca82-2576-4ea1-b56d-6ef09a6e5dbb)

![image 22](https://github.com/user-attachments/assets/0c74202d-8086-4ff0-ad60-700ba56e645b)

![image 23](https://github.com/user-attachments/assets/a24c7700-a558-43e8-b4f4-9f44e2e8a251)

![image 24](https://github.com/user-attachments/assets/3283a554-3e0f-4910-a0b3-e4ead0229f8c)

## 14.(finish)

---

Through this project, we developed an AI-based clothing tag system that helps visually impaired individuals distinguish the front and back of garments, enabling them to identify clothing with ease and express their personal style more freely.

We would like to extend our heartfelt gratitude to everyone who contributed to the success of this project. First and foremost, we thank our professors and mentors for their invaluable guidance and technical support from the early stages of ideation through to the finer technical details. Their advice and encouragement provided us with the direction and confidence to advance the project successfully. We are also deeply grateful to the visually impaired associations and participants who dedicated their time to assist with data collection and system testing. Their invaluable feedback greatly enhanced the usability and effectiveness of our solution.

Finally, we want to express our sincere appreciation to our team members for their dedication and hard work. Despite numerous challenges, the support and collaboration we shared made it possible to complete this project successfully. We hope that this system will continue to evolve and offer meaningful support to the visually impaired community in the future.

Once again, thank you to everyone for your support and contributions to this project.

My google drive ------------->(https://drive.google.com/drive/folders/1JW3nShGUMiz_seW_lCmzz1CR0zXKKtnc?usp=sharing)

NVIDIA Jetson Nano Learning Video([https://drive.google.com/drive/folders/176VjtSRGkM5FlXzxwM2UxuGHIa_HfEm3?usp=sharing](https://drive.google.com/drive/folders/1V6vNq71NgI34ovcYASDfd7bUjgjZsIP3?usp=sharing))

-(Thank you for reading)-
