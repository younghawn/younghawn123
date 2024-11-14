# Nvidia AI Specialist Certification Report

# **[주제 Title]**

## **시각장애인들 위한 AI 기반 의류 태그 시스템으로 옷 앞면 뒷면 구분하기**

---

## **AI-based clothing tag system for the visually impaired distinguishes front and back of clothing**

# Opening background information

[ 배경 정보 ]

<aside>
✅ 시각장애인은 옷을 입는 과정에서 옷의 앞뒤를 구분하는 것이 어려울 수 있습니다. 특히 다양한 디자인과 소재가 있는 현대 의류에서는 촉각으로만 앞뒤를 구별하기 쉽지 않기 때문에 이러한 문제를 해결할 필요성이 높아지고 있습니다. 현재 일부 의류에서는 앞뒤를 쉽게 구분할 수 있도록 돌출된 태그나 브레이유 점자를 사용하는 경우가 있지만, 이러한 방식이 모든 옷에 적용되거나 충분히 인지하기 쉬운 것은 아닙니다. 이에 따라 인공지능(AI)을 활용한 새로운 기술이 시각장애인을 돕기 위한 대안으로 떠오르고 있습니다.

</aside>

---

- Visually impaired individuals often face challenges in distinguishing the front from the back of clothing when dressing. With the variety in modern clothing designs and materials, relying solely on tactile cues can be challenging, highlighting the need for effective solutions. Some clothing brands currently incorporate raised tags or Braille for easier distinction; however, these methods are not universally applied across all garments and may not always be easily detectable. Therefore, AI technology presents a promising alternative to assist visually impaired individuals in overcoming these challenges.

# General description of the current project

[프로젝트 전반적인 설명]

<aside>
✅ 이 프로젝트는 시각장애인들이 옷의 앞뒤를 쉽게 구분할 수 있도록 AI 기반 의류 태그 시스템을 개발하는 것입니다. 스마트폰 앱 또는 태그 리더기를 통해 의류의 방향 정보를 음성으로 제공하여 독립적인 착용을 지원하고, 시각장애인의 생활 자율성을 높이는 것을 목표로 합니다.

</aside>

---

- This project aims to develop an AI-based clothing tag system that helps visually impaired individuals easily identify the front and back of garments. Using a smartphone app or tag reader, the system provides audio guidance on clothing orientation, supporting independent dressing and enhancing autonomy for visually impaired users.

# **Proposed idea for enhancements to the project**

[제안하고 싶은 프로젝트의 강점]

<aside>
✅ 이 프로젝트는 시각장애인의 접근성을 높여 독립적인 착용을 지원하며, 스마트폰 앱과 AI 기술을 통해 간편하고 직관적으로 의류의 앞뒤를 구분할 수 있게 합니다. 가정과 공공장소 등 다양한 상황에서 유용하게 적용될 수 있으며, 포용적인 사회를 만드는 데 기여하는 사회적 가치를 지닙니다.

</aside>

---

- This project enhances accessibility for visually impaired individuals, supporting independent dressing through a user-friendly smartphone app and AI technology that intuitively identifies garment orientation. It has versatile applications in both home and public settings and contributes to creating an inclusive society with significant social value.

---

# 영상 취득 방법

<aside>
✅ 의류를 여러 방향으로  촬영을 하였고 학습용은  1개비디오,  검증용은 4개의 비디오로 제작되었다.

</aside>

- Clothing was filmed in various directions, and one video was produced for learning and four videos for verification.

---

### -학습용 데이터 영상-

[https://youtube.com/shorts/GoYu1WJa5rE](https://youtube.com/shorts/GoYu1WJa5rE)

### -검증용 데이터 영상-

[https://youtube.com/shorts/HCJX9vd7g9I](https://youtube.com/shorts/HCJX9vd7g9I)

[https://youtube.com/shorts/QLN-niirask](https://youtube.com/shorts/QLN-niirask)

[https://youtube.com/shorts/QU1YHHeT-bw](https://youtube.com/shorts/QU1YHHeT-bw)

[https://youtube.com/shorts/-YoDbXzaBpg](https://youtube.com/shorts/-YoDbXzaBpg)

# **프로젝트 진행(Project Progress)**

## 1.영상 추출(**Image extraction)**

- 뱁믹스2(VABMIX_2) 을 이용하여 영상 해상도  640 X 640 크기를 설정한다.

---

- An image resolution of 640 X 640 is set using a bab mix 2 (VAMIX_2).

![스크린샷 2024-11-13 112846.png](%25EC%258A%25A4%25ED%2581%25AC%25EB%25A6%25B0%25EC%2583%25B7_2024-11-13_112846.png)

![스크린샷 2024-11-13 113058.png](%25EC%258A%25A4%25ED%2581%25AC%25EB%25A6%25B0%25EC%2583%25B7_2024-11-13_113058.png)

## 2.**DarkLabel  라벨링 (labels)**

- **DarkLabel.exe 파일로 이동**

---

- **Go to the DarkLabel.exe file**

[1JGpk_62UDtXw75_T9BOjZSmitk_SHDZb](https://drive.google.com/drive/folders/1JGpk_62UDtXw75_T9BOjZSmitk_SHDZb)

![Untitled](Untitled.png)

## 3.**DarkLabel  라벨링 파일 세팅(Setting Labeling Files)**

- **darklabel.yml 에 들어가 Tshirt 라는 클래스를 생성후 “front”속성을 생성한다.**

---

- **Create a class, "front" after generating a class, "front"**

![스크린샷 2024-11-13 222924.png](%25EC%258A%25A4%25ED%2581%25AC%25EB%25A6%25B0%25EC%2583%25B7_2024-11-13_222924.png)

- **format1 클래스에서 classes_set을 ”Tshirt”로 수정하고 이름도 “Tshirt로 바꾼다.**

---

- **In the format1 class, the classes_set is modified to "Tshirt", and the name is changed to "Tshirt".**

![스크린샷 2024-11-13 223018.png](%25EC%258A%25A4%25ED%2581%25AC%25EB%25A6%25B0%25EC%2583%25B7_2024-11-13_223018.png)

- data.yml파일에 들어가 “Tshirt”속성명 을 이름에 넣어준다. train,val 경로확인.

---

- **In Data, enter the name of "Tshirt" in the name.Check for train, val path.**

![스크린샷 2024-11-13 223053.png](%25EC%258A%25A4%25ED%2581%25AC%25EB%25A6%25B0%25EC%2583%25B7_2024-11-13_223053.png)

## 4.**DarkLabel  라벨링 데이터 추출(Extract DarkLabel Labeling Data)**

- open video 버튼을 눌러 영상을 가져오고 format 9 번에 설정해준 “Tshirt”클래스 를 클릭한다.
front 밑에 box+label 클릭후  next-predict 를 눌러가며 프레임마다 라벨링 을 지정해준다.
라벨링이 다 추출이 됬으면 save as video와 as images를 눌러 폴더에 저장해준다.

---

- Press the open video button to get the image and click the "Tshirt" class you set in format 9.
Click box+label under front and press next-prediction to label each frame.
When the labeling is completely extracted, press save as video and as images to save it in the folder.

![티셔츠 라벨링.png](%25ED%258B%25B0%25EC%2585%2594%25EC%25B8%25A0_%25EB%259D%25BC%25EB%25B2%25A8%25EB%25A7%2581.png)

## 5.DarkLabel 추출된 라벨링 확인(**Check extracted labeling)**

- Tshirt labels 파일에 txt 추출된 라벨링 확인(float값)

---

- Check txt extracted labeling in Tshirt labels file (float value)

![스크린샷 2024-11-13 235012.png](%25EC%258A%25A4%25ED%2581%25AC%25EB%25A6%25B0%25EC%2583%25B7_2024-11-13_235012.png)

[10hC7Rj9rhct-GgCwGhaxhUwu2iXG-L5v](https://drive.google.com/drive/folders/10hC7Rj9rhct-GgCwGhaxhUwu2iXG-L5v)

## 6. yolov5 코랩으로 데이터 학습시키기(**Learning data with yolov5 colab)**

- 구글 코랩을 실행시킨뒤 자신의 구글 드라이브와 연결한다.

---

- Run Google colab and then connect to your own Google Drive.

![스크린샷 2024-11-13 230929.png](%25EC%258A%25A4%25ED%2581%25AC%25EB%25A6%25B0%25EC%2583%25B7_2024-11-13_230929.png)

## 7. yolov5 설치(install)

- yolov5 레퍼지토리를 클론 후 설치한다.

---

- Clone and install the yolov5 repertoire.

![설치.png](%25EC%2584%25A4%25EC%25B9%2598.png)

## 8. 검증 데이터 만들기(**Create Verification Data)**

![검증 데이터.png](%25EA%25B2%2580%25EC%25A6%259D_%25EB%258D%25B0%25EC%259D%25B4%25ED%2584%25B0.png)

- `create_validation_set` 함수는 지정된 경로에서 학습 데이터의 일부를 검증 데이터로 이동시킵니다.
- 학습 이미지 리스트를 가져와 지정된 비율(`split_ratio`)로 학습과 검증 세트로 분리한 후, 검증 데이터에 해당하는 이미지와 라벨 파일을 지정된 검증 경로에 복사합니다.
- `train_test_split` 함수는`shutil.copy2` 함수는 파일 복사를 수행합니다.

---

- The `create_validation_set` function moves a
- It loads the list of training images, splits them into training and validation sets based on the `split_ratio`, then
- `train_test_split` is used`shutil.copy2` pe

## 9. 모델 학습(**Model Learning)**

![모델 학습.png](%25EB%25AA%25A8%25EB%258D%25B8_%25ED%2595%2599%25EC%258A%25B5.png)

- `python train.py`는 YOLOv5 모델의 학습을 실행하는 명령어입니다.
- `-img 512`: 입력 이미지 크기를 512x512로 설정합니다.
- `-batch 16`: 배치 크기를 16으로 설정하여 한 번에 처리할 데이터 샘플 수를 지정합니다.
- `-epochs 300`: 총 300 에포크 동안 학습을 수행합니다.
- `-data /content/drive/MyDrive/yolov5/yolov5/data.yaml`: 학습에 사용할 데이터셋 정보가 포함된 YAML 파일 경로를 지정합니다.
- `-weights yolov5n.pt`: 미리 학습된 `yolov5n` (YOLOv5 nano) 모델 가중치를 사용하여 학습을 시작합니다.
- `-cache`: 학습 데이터를 캐시하여 학습 속도를 높입니다.

---

- `python train.py` runs the training script for the YOLOv5 model.
- `-img 512`: sets the input image size to 512x512.
- `-batch 16`: sets the batch size to 16, defining the number of samples processed at once.
- `-epochs 300`: trains the model for a total of 300 epochs.
- `-data /content/drive/MyDrive/yolov5/yolov5/data.yaml`: specifies the path to the YAML file with dataset information.
- `-weights yolov5n.pt`: uses pretrained weights from the `yolov5n` (YOLOv5 nano) model to initialize training.
- `-cache`: caches the dataset in memory to speed up training.

![스크린샷 2024-11-13 231328.png](%25EC%258A%25A4%25ED%2581%25AC%25EB%25A6%25B0%25EC%2583%25B7_2024-11-13_231328.png)

## 10.결과(result)

- 텐서보드(tensor board)

![텐서보드.png](%25ED%2585%2590%25EC%2584%259C%25EB%25B3%25B4%25EB%2593%259C.png)

- Confusion Matrix

![confusion_matrix.png](confusion_matrix.png)

- F1-Curve

![F1_curve.png](F1_curve.png)

- labels_correlogram

![labels_correlogram.jpg](labels_correlogram.jpg)

- labels

![labels.jpg](labels.jpg)

- P-Curve

![P_curve.png](P_curve.png)

- Result

![results.png](results.png)

- Train batch 0,1,2

![train_batch0.jpg](train_batch0.jpg)

![train_batch2.jpg](train_batch2.jpg)

![train_batch1.jpg](train_batch1.jpg)

- Val batch,labels

![val_batch0_labels.jpg](val_batch0_labels.jpg)

![val_batch1_pred.jpg](val_batch1_pred.jpg)

![val_batch0_pred.jpg](val_batch0_pred.jpg)

- Val batch,labels

![val_batch2_pred.jpg](val_batch2_pred.jpg)

![val_batch1_labels.jpg](val_batch1_labels.jpg)

![val_batch2_labels.jpg](val_batch2_labels.jpg)

## 11.탐지(detect)

![탐지.png](%25ED%2583%2590%25EC%25A7%2580.png)

- yolov5 에서 학습이 완료되면 이미지와 비디오들을 감지한다.

---

- When learning is completed in yolov5 to detect images.

![스크린샷 2024-11-14 020614.png](%25EC%258A%25A4%25ED%2581%25AC%25EB%25A6%25B0%25EC%2583%25B7_2024-11-14_020614.png)

## 12.탐지 동영상(**detection video)**

[https://youtube.com/shorts/HCJX9vd7g9I](https://youtube.com/shorts/HCJX9vd7g9I)

[https://youtube.com/shorts/QLN-niirask](https://youtube.com/shorts/QLN-niirask)

[https://youtube.com/shorts/QU1YHHeT-bw](https://youtube.com/shorts/QU1YHHeT-bw)

[https://youtube.com/shorts/-YoDbXzaBpg](https://youtube.com/shorts/-YoDbXzaBpg)

## 13.탐지 이미지(**detection images)**

![image.png](image.png)

![image.png](image%201.png)

![image.png](image%202.png)

![image.png](image%203.png)

## 14.마무리(finish)

이 프로젝트를 통해 시각장애인을 위한 AI 기반 의류 태그 시스템을 개발하여 옷의 앞면과 뒷면을 구분하는 솔루션을 제공하게 되었습니다. 이를 통해 시각장애인들이 옷을 보다 쉽게 인식하고 스스로의 스타일을 자유롭게 표현할 수 있도록 돕고자 했습니다.

본 프로젝트가 완성될 수 있도록 도와주신 모든 분들께 깊은 감사의 말씀을 드립니다. 먼저, 프로젝트 초기 아이디어 단계에서부터 세부적인 기술적 도움을 아끼지 않으신 지도 교수님과 멘토님들께 감사드립니다. 이들의 조언과 격려 덕분에 연구의 방향성을 잡고 올바른 길로 나아갈 수 있었습니다. 또한, 데이터 수집과 시스템 테스트를 위해 시간을 내어 적극적으로 참여해 주신 시각장애인 협회와 사용자 분들께도 깊이 감사드립니다. 이들의 소중한 피드백 덕분에 시스템의 사용성을 한층 더 높일 수 있었습니다.

끝으로, 팀원 여러분의 노력과 열정에 감사를 전합니다. 여러 차례의 어려움 속에서도 서로 격려하며 협력해주신 덕분에 프로젝트를 성공적으로 마무리할 수 있었습니다. 앞으로도 이 시스템이 계속 발전하여 시각장애인들에게 실질적인 도움이 되기를 기대합니다.

다시 한번, 이 자리를 빌려 모든 분들께 진심으로 감사의 마음을 전합니다.

---

Through this project, we developed an AI-based clothing tag system that helps visually impaired individuals distinguish the front and back of garments, enabling them to identify clothing with ease and express their personal style more freely.

We would like to extend our heartfelt gratitude to everyone who contributed to the success of this project. First and foremost, we thank our professors and mentors for their invaluable guidance and technical support from the early stages of ideation through to the finer technical details. Their advice and encouragement provided us with the direction and confidence to advance the project successfully. We are also deeply grateful to the visually impaired associations and participants who dedicated their time to assist with data collection and system testing. Their invaluable feedback greatly enhanced the usability and effectiveness of our solution.

Finally, we want to express our sincere appreciation to our team members for their dedication and hard work. Despite numerous challenges, the support and collaboration we shared made it possible to complete this project successfully. We hope that this system will continue to evolve and offer meaningful support to the visually impaired community in the future.

Once again, thank you to everyone for your support and contributions to this project.

노션[(https://www.notion.so/Nvidia-AI-Specialist-Certification-Report-13d83fc878fb804e86afffa1dbf8dce1)](https://www.notion.so/Nvidia-AI-Specialist-Certification-Report-13d83fc878fb804e86afffa1dbf8dce1?pvs=21)

-감사합니다.(Thank you for reading)-