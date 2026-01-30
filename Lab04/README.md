# Lab04 - Computer Vision Labs

Thư mục này chứa các notebook Jupyter cho Lab04 trong khóa học Computer Vision. Các notebook này tập trung vào các phép biến đổi hình học, các phép toán toán học trên ảnh, và các bộ lọc ảnh. Mỗi notebook được thiết kế để học viên thực hành các kỹ thuật xử lý ảnh cơ bản.

## Các Notebook Chi Tiết

### 1. 2.4.1_Gemetric_trasfroms_PIL.ipynb
Notebook này giới thiệu về các phép biến đổi hình học và các công cụ toán học khác sử dụng thư viện PIL (Pillow). Thời gian ước tính: 40 phút.

**Nội dung chi tiết:**
- **Phần 1: Geometric Transformations**
  - Scaling: Thay đổi kích thước ảnh theo chiều ngang, dọc, hoặc cả hai. Sử dụng phương thức `resize()` của PIL với các tham số width và height.
  - Translation: Dịch chuyển ảnh (không được hỗ trợ trực tiếp trong PIL, nhưng có thể mô phỏng).
  - Rotation: Xoay ảnh bằng phương thức `rotate()` với góc quay (ví dụ: 45 độ).
- **Phần 2: Mathematical Operations**
  - Array Operations: Chuyển ảnh PIL sang NumPy array, sau đó thực hiện các phép toán như cộng/trừ hằng số, nhân hằng số, thêm nhiễu ngẫu nhiên.
  - Matrix Operations: Áp dụng Singular Value Decomposition (SVD) trên ảnh grayscale (sử dụng barbara.png), xây dựng ma trận S, và xấp xỉ ảnh với số lượng thành phần khác nhau (1, 10, 100, 200, 500) để thấy ảnh được tái tạo như thế nào.

**Ảnh sử dụng:** lenna.png, baboon.png, barbara.png (tải từ URL nếu cần).

**Kỹ năng học được:** Hiểu về biến đổi hình học, thao tác mảng, và phân tích ma trận trong xử lý ảnh.

### 2. 2.4.2_Gemetric_trasfroms_OpenCV.ipynb
Notebook này tương tự như notebook đầu tiên nhưng sử dụng thư viện OpenCV thay vì PIL. Thời gian ước tính: 40 phút.

**Nội dung chi tiết:**
- **Phần 1: Geometric Transformations**
  - Scaling: Sử dụng `cv2.resize()` với tham số fx (scale ngang), fy (scale dọc), và interpolation (INTER_NEAREST hoặc INTER_CUBIC). Ví dụ: scale ngang gấp đôi, scale dọc một nửa, hoặc scale cả hai.
  - Translation: Sử dụng `cv2.warpAffine()` với ma trận transformation M (bao gồm tx, ty). Ví dụ: dịch chuyển 100 pixel ngang, 50 pixel dọc, và điều chỉnh kích thước output để tránh cắt ảnh.
  - Rotation: Sử dụng `cv2.getRotationMatrix2D()` để tạo ma trận xoay, sau đó `cv2.warpAffine()`. Ví dụ: xoay 45 độ quanh tâm ảnh.
- **Phần 2: Mathematical Operations**
  - Array Operations: Cộng/trừ hằng số, nhân hằng số, thêm nhiễu ngẫu nhiên vào ảnh (sử dụng NumPy).
  - Matrix Operations: SVD trên ảnh grayscale (barbara.png), xây dựng ma trận S, và xấp xỉ ảnh với số lượng thành phần khác nhau.

**Ảnh sử dụng:** lenna.png, baboon.png, barbara.png.

**Kỹ năng học được:** Sử dụng OpenCV cho biến đổi hình học và toán học, so sánh với PIL.

### 3. 2374802010074_HoQuocDuy_252_71ITAI40603_0101.ipynb
Notebook này tập trung vào các bộ lọc ảnh và các phép toán xử lý ảnh cơ bản sử dụng OpenCV. Đây là notebook thực hành của sinh viên Ho Quoc Duy.

**Nội dung chi tiết:**
- **Phần 1: Box Filter**
  - Sử dụng `cv2.blur()` (hoặc `cv2.boxFilter()`) để làm mờ ảnh với các kích thước kernel khác nhau (3x3, 7x7). Hiển thị ảnh gốc và ảnh đã lọc cạnh nhau để so sánh.
- **Phần 2: Gaussian Filter**
  - Sử dụng `cv2.GaussianBlur()` với kernel lẻ (5x5, 11x11) và sigma=0. Hiển thị kết quả.
- **Phần 3: Median Filter**
  - Sử dụng `cv2.medianBlur()` với kernel size 5 và 9. Hiển thị kết quả.
- **Phần 4: Kiểm tra trên ảnh nhiễu**
  - Áp dụng median filter trên hai ảnh pepper_noise.jpg và pepper_noise02.jpg để loại bỏ nhiễu hạt tiêu.
- **Phần 5: Nhận xét về kích thước filter**
  - Filter phải là ma trận vuông với kích thước lẻ (3x3, 5x5, 11x11). Kích thước lớn làm ảnh mờ hơn.
- **Phần 6: Cân bằng sáng**
  - Sử dụng `cv2.equalizeHist()` trên ảnh grayscale (chuyển từ BGR nếu cần). Áp dụng trên pepper_noise.jpg và pepper_noise02.jpg sau khi median blur.
- **Phần 7: Bài tập lý thuyết**
  - a. Cắt hai ảnh exT3_01.png và exT3_02.png về kích thước 190x155.
  - b. Chuyển ảnh thành âm bản bằng `cv2.bitwise_not()`.
  - c. Trích xuất phần "ball" từ ảnh bằng thresholding và masking (sử dụng `cv2.threshold()` và `cv2.bitwise_and()`).

**Ảnh sử dụng:** cat.jpg, pepper_noise.jpg, pepper_noise02.jpg, exT3_01.png, exT3_02.png.

**Kỹ năng học được:** Áp dụng các bộ lọc để làm mờ và giảm nhiễu, cân bằng histogram, và các phép toán bitwise trên ảnh.

## Yêu cầu Hệ thống
Để chạy các notebook này, bạn cần cài đặt các thư viện sau:
- Python 3.x (khuyến nghị 3.7+)
- Pillow (PIL) - cho notebook 1
- OpenCV (cv2) - cho notebook 2 và 3
- Matplotlib - để vẽ đồ thị và hiển thị ảnh
- NumPy - cho thao tác mảng

**Cài đặt bằng pip:**
```
pip install pillow opencv-python matplotlib numpy
```

**Cài đặt bằng conda (nếu sử dụng Anaconda):**
```
conda install pillow opencv matplotlib numpy
```

## Cách Chạy
1. Mở Jupyter Notebook hoặc Jupyter Lab trong terminal:
   ```
   jupyter notebook
   ```
   hoặc
   ```
   jupyter lab
   ```
2. Điều hướng đến thư mục Lab04.
3. Mở từng notebook (.ipynb) và chạy các cell theo thứ tự.
4. Đảm bảo các file ảnh (lenna.png, baboon.png, v.v.) có trong thư mục hoặc tải từ URL như hướng dẫn trong notebook.

## Lưu Ý
- Các notebook sử dụng ảnh mẫu từ https://homepages.cae.wisc.edu/~ece533/images/. Nếu không có, bạn có thể tải thủ công.
- Một số phép toán có thể mất thời gian trên máy yếu, đặc biệt là SVD với nhiều thành phần.
- Đảm bảo đường dẫn ảnh chính xác; nếu không, chỉnh sửa code tương ứng.

## Tài Liệu Tham Khảo
- [Pillow Documentation](https://pillow.readthedocs.io/en/stable/index.html)
- [OpenCV Documentation](https://opencv.org/)
- Gonzalez, Rafael C., and Richard E. Woods. "Digital image processing." (2017).
- Jian, Wushuai, Xueyan Sun, and Shuqian Luo. "Computer-aided diagnosis of breast microcalcifications based on dual-tree complex wavelet transform." Biomedical engineering online 11.1 (2012): 1-12.
- Các ảnh mẫu từ: https://homepages.cae.wisc.edu/~ece533/images/

© IBM Corporation. All rights reserved.
