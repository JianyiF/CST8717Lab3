# CST8917Lab3: Implementing a Teams Chat Content Moderation Service

## 1. Design the Moderation Workflow
the flowchart of the moderation design

<img width="485" height="478" alt="image" src="https://github.com/user-attachments/assets/b5383d63-c5bc-4196-bfca-a0b990136ffc" />

## 2. Build the Moderation Service
The logic app designer screenshot

<img width="745" height="692" alt="image" src="https://github.com/user-attachments/assets/41ac7171-a19d-4301-a77f-e1ec01f25130" />


## 3. Implement the Email Notification Logic
the setups for all triggers

setup Teams channel when a message is sent in channel

<img width="610" height="579" alt="image" src="https://github.com/user-attachments/assets/0c45dd0e-5e3c-42fa-9c39-9d132c4af8a1" />

check the message composition

<img width="613" height="533" alt="image" src="https://github.com/user-attachments/assets/d438f157-70a4-4acb-aa09-229c38145b3d" />

the condition to check if the message contains the inappropriate contents, for example stupid or dumb will violate chatting policy

<img width="586" height="385" alt="image" src="https://github.com/user-attachments/assets/3d46f4a0-94a0-4228-b17e-92ec39ce84d1" />

then if true the message will be emailed to adminstrator email address about the message sent, sender and time.

<img width="613" height="739" alt="image" src="https://github.com/user-attachments/assets/317d4494-4798-4b52-8155-ce82391b7e1f" />

## 4. Test the Workflow
A message contains inappropriate content is sent in the team message.

<img width="862" height="159" alt="image" src="https://github.com/user-attachments/assets/5b772d3f-5d9a-435d-ab2a-3ff79f826fea" />

The run has successful.

<img width="1898" height="904" alt="image" src="https://github.com/user-attachments/assets/52b1dd0c-b752-4f58-ae91-a1bff93f60d7" />

all trigger pass the run.

<img width="639" height="700" alt="image" src="https://github.com/user-attachments/assets/c916e9be-9ecb-42d3-91f0-661260171035" />

an email has been sent to the administator email.

<img width="1606" height="729" alt="image" src="https://github.com/user-attachments/assets/23918aff-e008-4a63-983f-68f799513b72" />

## challenge

Challenge: The extracted message content was wrapped in HTML tags like <p> stupid </p>, which made string comparisons unreliable and bad request.

Resolution: A Compose action or substring/replace functions were used to clean the content or detect offensive keywords within the HTML structure.

## YouTube video Demo
https://youtu.be/N3XG-0nIRoU
