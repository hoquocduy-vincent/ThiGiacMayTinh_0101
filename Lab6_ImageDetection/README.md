# Lab6_ImageDetection - Nhận Diện Ảnh (Image Detection)

## Mô tả
Dự án sử dụng **OpenCV** với **Haar Cascade Classifiers** để thực hiện nhận diện các đối tượng trong ảnh, bao gồm:
- Dấu hiệu dừng (stop sign)
- Khuôn mặt (face detection)
- Miệng (mouth)
- Mũi (nose)

## Yêu cầu bài tập (theo Lab06_ImageDetection.docx)
- Sử dụng Google Colab để thực hành
- Tối thiểu **4 đoạn code**:
  1. Code mẫu nhận diện stop sign
  2. Nhận diện khuôn mặt
  3-4. Nhận diện 2 bộ phận cơ thể (miệng, mũi)
- Không nộp file ảnh input, chỉ sử dụng `hinh1.jpg`, `hinh2.jpg`
- File nộp theo format: `MasoSV_HoTenSV_MaLHP_Lab06.ipynb`

## Cấu trúc thư mục
```
Lab6_ImageDetection/
├── 2374802010074_HoQuocDuy_252_71ITAI40603_0101_Lab6.ipynb  # Notebook chính
├── hinh1.jpg                                               # Ảnh test 1 (stop sign)
├── hinh2.jpg                                               # Ảnh test 2 (khuôn mặt)
├── Lab06_ImageDetection.docx                               # Đề bài lab
├── Mieng.xml                                               # Haar Cascade - Miệng (mouth)
├── mui.xml                                                 # Haar Cascade - Mũi (nose)
├── NhanDienKhuonMat.xml                                    # Haar Cascade - Khuôn mặt (face)
└── stop_data.xml                                           # Haar Cascade - Dấu dừng (stop sign)
```

## Công nghệ sử dụng
- **Python** + **Jupyter Notebook**
- **OpenCV** (`cv2`) - Computer Vision library
- **Matplotlib** (`plt`) - Hiển thị kết quả
- **Haar Cascade Classifiers** - Pre-trained XML models

## Cách chạy
### 1. Môi trường đề xuất: Google Colab
```python
# Cài đặt OpenCV (nếu cần)
!pip install opencv-python matplotlib
```

### 2. Chạy notebook
Mở file và chạy từng cell theo thứ tự:

1. **Cell 1**: Nhận diện stop sign trên `hinh1.jpg`
2. **Cell 2**: Nhận diện khuôn mặt trên `hinh2.jpg` 
3. **Cell 3**: Nhận diện miệng trên `hinh2.jpg`
4. **Cell 4**: Nhận diện mũi trên `hinh2.jpg`

### Code mẫu (từ notebook)
```python
import cv2
import matplotlib.pyplot as plt

# Load ảnh và chuyển grayscale
img = cv2.imread("hinh1.jpg")
img_gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)

# Load cascade classifier
cascade = cv2.CascadeClassifier('stop_data.xml')

# Detect objects
found = cascade.detectMultiScale(img_gray, minSize=(20, 20))

# Vẽ bounding box màu xanh lá
for (x, y, width, height) in found:
    cv2.rectangle(img_rgb, (x, y), (x + height, y + width), (0, 255, 0), 5)

plt.imshow(img_rgb)
plt.show()
```

## Kết quả mong đợi
- **hinh1.jpg**: Detect được stop sign (bounding box xanh lá)
- **hinh2.jpg**: Detect được khuôn mặt, miệng, mũi

## Lưu ý
- Đảm bảo tất cả file XML và ảnh JPG nằm cùng thư mục với notebook
- Thay đổi `minSize=(20, 20)` tùy theo kích thước đối tượng

## Tham khảo
- [OpenCV Haar Cascades](https://github.com/opencv/opencv/tree/master/data/haarcascades)
- [Google Colab](https://colab.research.google.com/)

---

