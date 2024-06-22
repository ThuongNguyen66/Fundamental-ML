# Mini-Project for Fundamentals of Machine Learning Course
![background](./materials/ai_wp.jpg)
This repository contains the code and data for a mini-project on facial expression recognition using machine learning algorithms.

## 📑 Project Policy
- Team: group should consist of 3-4 students.

    |No.| Student Name    | Student ID |
    | --------| -------- | ------- |
    |1|Nguyễn Thị Hoài Thương|20110320|
    |2|||
    |3|||
    |4|||

- The submission deadline is strict: **11:59 PM** on **June 22nd, 2024**. Commits pushed after this deadline will not be considered.

## 📦 Project Structure

The repository is organized into the following directories:

- **/data**: This directory contains the facial expression dataset. You'll need to download the dataset and place it here before running the notebooks. (Download link provided below)
- **/notebooks**: This directory contains the Jupyter notebook ```EDA.ipynb```. This notebook guides you through exploratory data analysis (EDA) and classification tasks.

## ⚙️ Usage

This project is designed to be completed in the following steps:

1. **Fork the Project**: Click on the ```Fork``` button on the top right corner of this repository, this will create a copy of the repository in your own GitHub account. Complete the table at the top by entering your team member names.

2. **Download the Dataset**: Download the facial expression dataset from the following [link](https://mega.nz/file/foM2wDaa#GPGyspdUB2WV-fATL-ZvYj3i4FqgbVKyct413gxg3rE) and place it in the **/data** directory:

3. **Complete the Tasks**: Open the ```notebooks/EDA.ipynb``` notebook in your Jupyter Notebook environment. The notebook is designed to guide you through various tasks, including:
    
    1. Prerequisite
    2. Principle Component Analysis
    3. Image Classification
    4. Evaluating Classification Performance 

    Make sure to run all the code cells in the ```EDA.ipynb``` notebook and ensure they produce output before committing and pushing your changes.

5. **Commit and Push Your Changes**: Once you've completed the tasks outlined in the notebook, commit your changes to your local repository and push them to your forked repository on GitHub.


Feel free to modify and extend the notebook to explore further aspects of the data and experiment with different algorithms. Good luck.

## Report Mini-Project 
1. Tiền xử lý dữ liệu và trực quan hóa.
2. Áp dụng Phân tích thành phần chính (PCA) để giảm chiều dữ liệu.
3. So sánh hiệu suất của các thuật toán học máy khác nhau trước và sau khi áp dụng PCA.
4. Đánh giá các mô hình sử dụng các metric: accuracy, precision, recall, và F1-score.
   
- Sử dụng bốn mô hình khác nhau để so sánh hiệu suất: Logistic Regression, Random Forest, CNN và MLP.

**Mô Hình CNN**

Mô hình CNN được xây dựng và huấn luyện sử dụng Keras. Các tham số chính của mô hình bao gồm: Convolutional, MaxPooling, Dense.

**Tinh Chỉnh Siêu Tham Số**

Sử dụng GridSearchCV để tìm kiếm các siêu tham số tốt nhất cho từng mô hình dựa trên các grid siêu tham số xác định trước. Dưới đây là các grid siêu tham số được sử dụng:

- Logistic Regression: {'classifier__C': [0.1, 1, 10]}
- Random Forest: {'classifier__n_estimators': [50, 100, 200]}
- MLP: {'classifier__hidden_layer_sizes': [(50,), (100,), (50, 50)]}
  
**Nhận Xét Tổng Quát**

- Logistic Regression: Mô hình này hoạt động tốt trên cả dữ liệu gốc và dữ liệu PCA, nhưng hiệu suất có thể kém hơn so với Random Forest và MLP khi số lượng tính năng lớn.
- Random Forest: Hoạt động rất tốt trên dữ liệu gốc và cũng duy trì hiệu suất tốt trên dữ liệu PCA. Đây là mô hình mạnh mẽ và có khả năng xử lý các tính năng không tuyến tính.
- MLP: Mô hình này có hiệu suất tốt nhất trong số các mô hình đã kiểm tra. MLP có thể học được các mẫu phức tạp trong dữ liệu.
  
**Kết Luận**

Dự án đã thành công trong việc phân loại cảm xúc từ hình ảnh khuôn mặt sử dụng nhiều mô hình học máy khác nhau. Mô hình CNN có hiệu suất tốt nhất, cho thấy tầm quan trọng của việc sử dụng mạng nơ-ron sâu trong các tác vụ nhận dạng hình ảnh. 
