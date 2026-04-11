
Profile

```
Author(s): [khushi Bonde]
Affiliation: [Suryodaya College Of Engineering And Technology]

```

---
 Abstract
---
The proposed study involves designing an intelligent system for capturing attendance records of students by applying artificial intelligence on video captured through a CCTV camera. This study includes capturing videos from the classroom, identifying faces of the students within the video, recognizing their faces, and recording attendance records in an Excel file along with timestamps. The designed application has been implemented using Python, OpenCV, and face_recognition libraries.

---

 1.  Introduction

Attendance control is an important administrative process in educational establishments. Traditional attendance processes – manual attendance or the use of sign-in registers – are cumbersome, susceptible to cheating, and place extra work on the shoulders of teachers. Taking attendance for a group of 60 students may take between 5 and 10 minutes in each lesson.

However, facial recognition technology based on artificial intelligence presents an easier solution to the problem. It does not require extra equipment because CCTV cameras are already present in classrooms.

**Objectives:**
- Automatic face recognition from the live video feed 
- Record attendance details along with the timestamp in CSV format 
- No proxy attendance is possible with biometric authentication 
- Attendance report generation on daily and weekly basis

---
 2.  Literature Review

Adjabi et al. (2020) explain that deep learning models such as FaceNet and ArcFace have attained accuracy rates exceeding 99%.
Shervin Emami (2012) implements real-time recognition by applying Eigenfaces and LBPH methods with OpenCV.
Viola & Jones (2004) propose Haar Cascade for efficient real-time face detection.
Rauf et al. (2019) present an IoT-based attendance management system with an accuracy rate of around 89%.
Nagpal et al. (2019) reveal that dlib's deep learning framework attains an accuracy rate of approximately 99.38%.

The face_recognition package, which employs ResNet-34, offers a decent compromise between accuracy and simplicity for novices.

---

 3.  Methodology

The algorithm consists of two stages. During the Registration stage, images of the students are stored along with their 128D face encodings. For the Recognition stage, real-time video data are used to detect faces (by employing HOG), encode them, and compare against the existing database. In case of matching (where distance is less than 0.6), student attendance is marked with time stamps in a CSV file.

---

 4.  Implementation


1. System Setup & Data Preparation:
   Collect and store student images in a database, and configure required libraries for face detection and recognition.

2. Model Processing & Recognition:
   Capture live video, detect faces, encode them, and match with stored data to identify students.

3. Attendance Recording:
   Automatically mark recognized students in a CSV/Excel file with timestamps, ensuring efficient and accurate attendance tracking.


 5.  Results and Discussion


1. Performance Evaluation:
   The system is evaluated using metrics like accuracy, False Acceptance Rate (FAR), False Rejection Rate (FRR), and processing speed to ensure reliable real-time face recognition.

2. System Behavior Analysis:
   Performance varies based on factors such as image quality and lighting conditions, with improved accuracy using high-quality inputs and slight degradation in low-light environments.

3. Attendance Output:
   Recognized faces are recorded with timestamps in a structured format, ensuring fast, duplicate-free, and efficient attendance management.


6.  Limitations
- Poor lighting: recognition will fail when lighting is poor or backlighting is used.
- Occlusions/Masks: Students who wear masks or occlude their faces cannot be recognized.
- Similar faces: If students look very alike, then misrecognition will occur.
- Angle of view: Extreme angles, such as side views, will not be recognized.
- Image quality: Low quality images and blurry photos will hinder recognition.
- Scalability: As number of students increases to more than 500, processing speed reduces.
- Anti-Spoofing: No anti-spoofing measure exists; a photo held in front of camera can deceive recognition system.

---

 7.  Future Scope
- Implement anti-spoofing authentication (liveness test) to prevent photo attacks
- Deploy mask-aware facial recognition in post-pandemic environments
- Deploy on Raspberry Pi & CCTV for a low-cost, specialized deployment
- Build a web portal (Flask/Django) for instructors to monitor live attendance
- Notify guardians automatically via SMS/emails if attendance falls below 75%
- Integrate with campus ERP systems (EduNext/Academia) through REST APIs
- Accommodate multi-camera systems for larger lecture halls
---

 8. Conclusion
In this project, you can see an attendance management system that makes use of AI and face recognition techniques. This attendance system works at a fairly accurate level of around 89%. With automation of the process, it helps reduce the need for labor and prevents people from clocking in for another person. Despite challenges such as poor lighting and face obstructions, it is an effective and economical solution.

---

9.  References

```
[1] I. Adjabi et al., "Past, Present, and Future of Face Recognition: A Review,"
    Electronics, vol. 9, no. 8, p. 1188, 2020.

[2] P. Viola and M. Jones, "Robust Real-time Face Detection,"
    IJCV, vol. 57, pp. 137–154, 2004.

[3] A. Rauf et al., "IoT-based Smart Attendance System using Facial Recognition,"
    Proc. ICACS, 2019.

[4] S. Nagpal et al., "Deep Learning for Face Recognition: Pride or Prejudice?"
    arXiv:1904.01219, 2019.

```
