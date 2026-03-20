# Lab5: Phân Đoạn Ảnh (Image Segmentation)

## Mô tả
Thư mục này chứa bài thực hành Lab05 về **Phân Đoạn Ảnh** (Image Segmentation) sử dụng Python với các thư viện OpenCV, scikit-image và matplotlib. Bài lab thực hiện các thuật toán phân đoạn ảnh cơ bản và nâng cao trên ảnh mẫu `Lab5.jpg`.

## Cấu trúc thư mục
```
Lab5_ImageSegmentation/
├── 2374802010074_HoQuocDuy_252_71ITAI40603_0101_Lab5.ipynb     # Notebook chính chứa code và kết quả
├── Lab05_Image Segmentation.doc     # Tài liệu hướng dẫn bài lab (Word)
├── Lab5.jpg                         # Ảnh đầu vào để phân đoạn
└── README.md                        # Tài liệu này
```

## Nội dung chính (trong notebook)
Notebook triển khai các phương pháp phân đoạn ảnh sau:

### 1. **Thresholding (Ngưỡng hóa)**
   - Ngưỡng cố định (T=127)
   - Ngưỡng Otsu tự động

### 2. **K-means Clustering**
   - Phân cụm màu với K=4
   - Sử dụng `cv2.kmeans()`

### 3. **Region Growing (Phát triển vùng)**
   - Triển khai thuật toán đơn giản
   - Seed point ở giữa ảnh

### 4. **Region-based Segmentation**
   - Felzenszwalb (Split and Merge)
   - Sử dụng `skimage.segmentation.felzenszwalb`

### 5. **Edge-based Segmentation**
   - Canny edge detection
   - Dilation để tạo vùng kín

Mỗi thuật toán đều có hàm `plot_res()` để hiển thị so sánh Original vs Result.

## Yêu cầu môi trường
- Python 3.x
- Jupyter Notebook
- Thư viện:
  ```bash
  pip install opencv-python scikit-image matplotlib numpy
  ```

## Hướng dẫn chạy
1. Mở terminal trong thư mục dự án
2. Khởi động Jupyter:
   ```bash
   jupyter notebook
   ```
3. Mở file `Lab5_ImageSegmentation.ipynb`
4. Chạy tất cả cells (Runtime → Run all)
5. Quan sát các kết quả phân đoạn hiển thị bằng matplotlib

## Kết quả mong đợi
- 6 hình ảnh so sánh: Original vs Segmented cho từng thuật toán
- Có thể điều chỉnh tham số (threshold, K, seed, scale...) để thử nghiệm

## Lưu ý
- Đảm bảo file `Lab5.jpg` nằm cùng thư mục với notebook
- Một số cell cần chạy `!pip install opencv-python` lần đầu
- Tài liệu hướng dẫn chi tiết trong `Lab05_Image Segmentation.doc`

## Mục tiêu học tập
- Hiểu các phương pháp phân đoạn ảnh cơ bản
- Làm quen với OpenCV và scikit-image
- Thực hành xử lý ảnh với Python

---

