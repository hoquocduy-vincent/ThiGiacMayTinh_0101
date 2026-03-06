# Lab05 - Spatial Filtering and Image Enhancement

## Giới thiệu chung

Lab05 tập trung vào **lọc không gian (spatial filtering)** và các phép biến đổi toán học trên ảnh để giảm nhiễu, làm mịn, làm nét và trích xuất biên. Lab gồm **hai notebook**: một notebook sử dụng **Pillow (PIL)** và một notebook sử dụng **OpenCV (cv2)**.

### Mục tiêu chính

- Hiểu và làm quen với **lọc tuyến tính (linear filtering)** và **lọc phi tuyến (median filtering)**
- Áp dụng các **kernel (bộ lọc)** để làm mượt, làm nét và phát hiện biên
- Thực hành với cả hai thư viện phổ biến: **Pillow (PIL)** và **OpenCV (cv2)**
- Quan sát sự khác biệt khi làm việc với ảnh RGB (Pillow) và BGR (OpenCV)

---

## 1. File `2.5.1_Spatial_Filtering-PIL.ipynb`

### Mục đích

Notebook này sử dụng thư viện **Pillow (PIL)** để giới thiệu các kỹ thuật lọc ảnh tại chỗ, bao gồm **lọc trung bình, Gaussian blur, làm nét, phát hiện biên** và **lọc median**.

### Nội dung chính

Trong notebook này bạn sẽ học được:

- Cách **tải và hiển thị ảnh** bằng PIL và matplotlib
- Thêm **nhiễu Gaussian** vào ảnh để mô phỏng ảnh bị nhiễu
- Áp dụng **kernel tùy chỉnh** (convolution) để lọc ảnh
- Sử dụng các bộ lọc có sẵn của PIL (`ImageFilter`) để:
  - Làm mờ (blur)
  - Làm nét (sharpen)
  - Phát hiện biên (edge)
- Áp dụng **median filter** để giảm nhiễu hạt (salt & pepper noise)

Ảnh sử dụng: `lenna.png`, `cameraman.jpeg`, `barbara.png`.

---

## 2. File `2.5.2_Spatial_Filtering.ipynb`

### Mục đích

Notebook này sử dụng thư viện **OpenCV (cv2)** để thực hiện **lọc không gian** và **phép toán hình học** tương tự như notebook PIL, đồng thời làm rõ sự khác biệt về định dạng màu (BGR vs RGB).

### Nội dung chính

Trong notebook này bạn sẽ học được:

- Cách **đọc và hiển thị ảnh** bằng OpenCV và matplotlib (chuyển đổi BGR → RGB)
- Thêm **nhiễu Gaussian** để thử nghiệm
- Áp dụng **lọc trung bình (mean filter)** bằng `cv2.filter2D()` với kernel tùy chỉnh
- Sử dụng các bộ lọc OpenCV:
  - `cv2.GaussianBlur()`
  - `cv2.medianBlur()`
  - Bộ lọc làm nét (sharpen)
  - Phát hiện biên (ví dụ: bằng kernel Sobel hoặc bộ lọc biên)
- Sử dụng **threshold** để phân đoạn đơn giản (if có trong notebook)

Ảnh sử dụng: `lenna.png`, `cameraman.jpeg`, `barbara.png`.

---

## Yêu cầu hệ thống

- Python 3.x
- Jupyter Notebook (hoặc Jupyter Lab)

### Thư viện cần thiết

Cài đặt bằng pip:

```bash
pip install pillow opencv-python matplotlib numpy
```

---

## Hướng dẫn chạy

1. Mở terminal, chuyển đến thư mục `Lab05`.
2. Khởi động Jupyter Notebook:

```bash
jupyter notebook
```

3. Mở từng file `.ipynb` và chạy theo thứ tự các cell.

---

## Ghi chú

- Các notebook có tự động tải ảnh từ Internet (sử dụng `wget`) nếu ảnh chưa tồn tại.
- Nếu gặp lỗi do thiếu ảnh hoặc không có kết nối mạng, bạn có thể đặt các ảnh (`lenna.png`, `cameraman.jpeg`, `barbara.png`) vào cùng thư mục trước khi chạy.

---

## Tài liệu tham khảo

- [Pillow Documentation](https://pillow.readthedocs.io/en/stable/index.html)
- [OpenCV Documentation](https://opencv.org/)
- Gonzalez, Rafael C., and Richard E. Woods. "Digital Image Processing." (2017).
- Các ảnh mẫu từ: https://homepages.cae.wisc.edu/~ece533/images/

© IBM Corporation. All rights reserved.
