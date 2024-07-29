# Emotion Feedback Capstone Design Project

This project, "Emotion Feedback," aims to recommend conversation topics for video chats based on real-time emotion analysis.
<br>

## Team Members

| <img src="https://github.com/Tave-13th-Project-Team-4-Fiurinee/.github/blob/main/profile/image/%EC%9D%B4%EC%A4%80%EB%B2%94.jpg" alt="이준범" width="200" height="200">  | <img src="https://github.com/Tave100Shot/.github/blob/master/profile/img/%EA%B9%83%ED%97%88%EB%B8%8C_%EB%B0%95%ED%98%84%EB%B9%88.png" alt="이원재" width="200" height="200"> | <img src="https://github.com/Tave100Shot/.github/blob/master/profile/img/%EA%B9%83%ED%97%88%EB%B8%8C_%EC%86%A1%EC%9C%A4%EC%A3%BC.png" alt="권영우" width="200" height="200"> | <img src="https://github.com/Tave100Shot/.github/blob/master/profile/img/%EA%B9%83%ED%97%88%EB%B8%8C_%EC%9D%B4%EC%9C%A0%EC%A7%84.png" alt="심재호" width="200" height="200"> |
|:---:|:---:|:---:|:---:|
| 이준범 | 이원재 | 권영우 | 심재호 |
| Backend, Signaling Server | Model Server | Frontend | Modeling |
| [ss7622](https://github.com/ss7622) | [Lee-wonjae](https://github.com/Lee-wonjae) | [kwonup](https://github.com/kwonup) | [JaehoSim98](https://github.com/JaehoSim98) |

<br/>

## 📅 Development Period
 - 2024-03-02 ~ 2024-06-14
<br>

## Introduction
"Emotion Feedback" is a system designed to alleviate awkward atmospheres and lack of conversation topics during video chats by recommending topics based on real-time emotion analysis.
<br>

### Common Issues in Conversations:
<img src="https://github.com/EmotionFeedback/.github/blob/main/imgs/%EC%84%A4%EB%AC%B8.png" alt="소개팅 설문조사">
source: '결혼정보회사 듀오 ‘미혼 남녀 소개팅 관련 설문 조사’  
<br>

- Awkward atmosphere
- Lack of conversation topics

### Solution:
- Emotion-based conversation topic recommendation
<br>

## System Features

- **Real-time Emotion Analysis**: Analyze and store the emotions of the participants in real-time.
- **Emotion-based Topic Recommendation**: Recommend conversation topics based on the stored emotions and conversation content.
- **Understanding Partner’s Favorability**: Analyze and display the favorability graph of the conversation partner post-conversation.
<br>

## System Architecture

<img src="https://github.com/EmotionFeedback/.github/blob/main/imgs/%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202024-06-05%20202344.png" alt="시스템 아키텍쳐">
<br>

## Functional Flow

1. **Video Call**: Users start a video call through the system.

2. **Data Collection and Analysis**:
   - **Image Analysis**: Analyze the user's facial expressions captured from the video.
   - **Text Analysis**: Convert the conversation into text and analyze the sentiment.
   - **Audio Analysis**: Analyze the tone and speed of the user's voice to determine the emotional state.

3. **Data Processing**
   - Preprocessing images to fit CNN models.
   - Converting and preprocessing audio and text data for analysis.

4. **Favorability Detection**
   - Combining data from text, image, and audio analysis to evaluate the favorability between users.

5. **Real-time Topic Recommendation**
   - Using stored data and GPT API to recommend conversation topics in real-time.

6. **Data Storage and Feedback**
   - Storing analyzed text data and favorability scores in a database.
   - Providing feedback to users based on stored data after the conversation ends.

### Technical Stack

- **Frontend**: React, Figma, WebRTC, MediaStream API
- **Backend**: FastAPI, SpringBoot, WebSocket, PostgreSQL, AWS
- **Modeling**: CNN for image, audio, and text analysis, LangChain for natural language processing
<br>

## Evaluation and Future Plans

Despite achieving significant accuracy for emotion detection, continuous improvements are planned, including expanding the dataset, refining models, and exploring additional applications such as enhancing conversational flow and user engagement.

### Challenges and Solutions

- **STT Delay**: Mitigated by adding a 3-second delay to accommodate processing time.
- **Model Accuracy**: Improved by modifying preprocessing steps and model parameters, achieving 78% accuracy for image models and 82% for audio/text models.
- **Real-time Processing**: Achieved using asynchronous processing with FastAPI to handle model server communications.

### Future Plans

- Increase the amount of quality data to improve model performance.
- exploring additional applications such as enhancing conversational flow and user engagemen
<br>

## Demonstration video

[📼 Demonstration video](https://youtu.be/BfVNF6mo3EA?si=dSLIJjktVfRsRmDv)

## Awards

3rd place in Sejong University Creatvie Design Competition
<img src="https://github.com/EmotionFeedback/.github/blob/main/imgs/KakaoTalk_20240726_041948791.jpg" alt="상">
