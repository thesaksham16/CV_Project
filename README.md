# 👁️‍🗨️ Computer Vision TA-2 – B.Tech Data Science (6th Sem)


**Created by:** Saksham Chawla\
**Branch:** B.Tech CSE (Data Science)\
**University:** Ramdeobaba University (RBU), Nagpur. 

📅 **Semester**: 6th 

📘 **Subject**: Computer Vision Lab



Welcome to my Computer Vision TA-2 repository! 👨‍💻 This project includes implementations of core CV techniques using Python and OpenCV. All work is performed in Google Colab, and images are uploaded through the Colab Files section. Each practical includes the objective, implementation, results, observations, and conclusion.

---

## 🔧 Technologies Used

- Python 🐍
- OpenCV (cv2) 📷
- Google Colab 📒

---

## 📂 Practical Implementations

### 🎯 Problem 1: RANSAC – Outlier Removal & Transformation

#### 🎯 Objective:
Use RANSAC to remove outlier key point matches and fit a transformation model between two images.

#### 🧪 Steps:
1. Load two images with overlapping content using `cv2.imread()`.
2. Convert both images to grayscale.
3. Detect keypoints and compute descriptors using SIFT or ORB.
4. Match keypoints using BFMatcher or FLANN.
5. Apply `cv2.findHomography()` with `cv2.RANSAC` to estimate a transformation matrix.
6. Filter out outlier matches.
7. Warp one image onto another using the homography matrix.
8. Display matched keypoints and transformed result.

#### 🖼️ Input:
- A pair of images from different viewpoints with overlapping scenes (e.g., `Pair1_Image1.jpg` and `Pair1_Image2.jpg`).

#### 📝 Observation:
- Feature points between the two images were matched using **SIFT or ORB** descriptors.
- Some matches were **inaccurate or noisy**, leading to outliers in the initial match set.
- The RANSAC algorithm successfully filtered out these outliers, retaining only **inliers** that fit a geometric model.
- A transformation matrix (homography) was estimated, and the matching points aligned correctly after RANSAC filtering.

#### ✅ Conclusion:
- RANSAC is highly effective for **robust model estimation** in the presence of noisy or incorrect matches.
- It helps achieve **precise alignment and transformation** between images even with initial inaccuracies.
- This method is crucial for tasks like **image stitching, panorama creation, and 3D reconstruction**.
- Overall, RANSAC ensures **accuracy and consistency** in computer vision pipelines involving multiple frames or views.

---

### 🏛️ Problem 2: Harris Corner Detection

#### 🎯 Objective:
Implement the Harris corner detector to find and visualize corners in a grayscale image.

#### 🧪 Steps:
1. Read the uploaded image using `cv2.imread()`.
2. Convert the image to grayscale.
3. Apply the `cv2.cornerHarris()` function.
4. Dilate the result for better corner marking.
5. Threshold and mark corners on the original image.
6. Display the result with `matplotlib` or `cv2.imshow()`.

#### 🖼️ Input:
- Used a **sunflower image** with clear patterns and gradients.

#### 📝 Observation:
- The Harris corner detector successfully identified corners at locations with **strong intensity variation** in both directions.
- Most corners were found around **edges of petals**, **leaf veins**, and **texture-rich areas** in the sunflower image.
- Fine-tuning the threshold helped eliminate weak and non-distinct points.
- The corners were marked clearly with red dots, showcasing **feature-rich** areas in the image.

#### ✅ Conclusion:
- Harris Corner Detection is a **classical and powerful** method for identifying interest points in grayscale images.
- It works well in images with **sharp gradients**, making it suitable for structured and textured objects.
- However, it may detect more false positives compared to advanced detectors, and is **sensitive to noise**.
- Still, it is a solid choice for **feature detection in static scenes**.

---

### 👁️‍🗨️ Problem 3: Shi-Tomasi Corner Detection

#### 🎯 Objective:
Use the Shi-Tomasi corner detector to identify and mark corner points in an image.

#### 🧪 Steps:
1. Convert image to grayscale.
2. Use `cv2.goodFeaturesToTrack()` to find corners.
3. Iterate through the detected corners and mark them.
4. Display the resulting image.

#### 🖼️ Input:
- Used an image with **sharp lines and edges** (e.g., architecture or geometric shapes).

#### 📝 Observation:
- The Shi-Tomasi detector detected **refined and stable corner points** using eigenvalue analysis.
- Most of the corners were around **clear edge intersections** like windows, object outlines, and architectural edges.
- The `cv2.goodFeaturesToTrack()` function allowed control over **corner quality** and spacing.
- It produced **fewer but more accurate** corners compared to Harris.

#### ✅ Conclusion:
- Shi-Tomasi improves upon Harris by **selecting the most prominent and stable corners**.
- It is more **robust and noise-resistant**, leading to more reliable results in dynamic or real-world environments.
- This method is **preferred in real-time applications** like object tracking and optical flow.





---

## 📌 Final Remarks

This project demonstrates fundamental computer vision concepts applied to real-world images. Each method shows unique strengths and trade-offs. These practicals helped build a strong base in feature detection and image processing.

> Feel free to explore, modify, and build on top of these implementations! 😊

---


