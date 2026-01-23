# Lab03

## Tổng Quan

Dự án Lab03 bao gồm các notebook hướng dẫn về xử lý hình ảnh và phân tích dữ liệu.

## Notebook 1: 2.3.2_ Histograms and Intensity Transformations

Notebook này tập trung vào các kỹ thuật xử lý hình ảnh, bao gồm:

- **Pixel Transforms**: Các phép biến đổi trên từng pixel.
- **Histograms**: Tạo và phân tích histogram để hiểu phân bố cường độ của hình ảnh.
- **Intensity Transformations**: Bao gồm tạo ảnh âm bản, điều chỉnh độ sáng và độ tương phản, cân bằng histogram.
- **Thresholding và Simple Segmentation**: Ngưỡng hóa để phân đoạn hình ảnh.

Notebook sử dụng thư viện OpenCV và matplotlib, với các ví dụ trên các hình ảnh như lenna, baboon, goldhill, v.v.

## Notebook 2: Consumption

Notebook này phân tích dữ liệu chuyến đi Uber từ tháng 7 năm 2014, bao gồm:

- **Tiền xử lý dữ liệu**: Đọc và chuyển đổi dữ liệu thời gian.
- **Phân tích chuỗi thời gian**: Số chuyến đi theo giờ và ngày.
- **Mô hình hàng tuần**: Trung bình số chuyến đi theo giờ và ngày trong tuần.
- **Tính khoảng cách**: Khoảng cách đến các điểm quan tâm như Metro Art và Empire State Building.
- **Bản đồ hóa**: Sử dụng Folium để tạo bản đồ nhiệt và trực quan hóa theo thời gian.
- **Kiểm định thống kê**: So sánh sự khác biệt về mùa vụ giữa ngày trong tuần và cuối tuần.

Notebook sử dụng pandas, matplotlib, seaborn, geopy, folium, và scipy.

## Cài Đặt và Chạy

### Yêu cầu hệ thống
- Python 3.x
- Jupyter Notebook

### Thư viện cần thiết
- opencv-python
- matplotlib
- pandas
- seaborn
- geopy
- folium
- scipy

Cài đặt các thư viện bằng pip:

```
pip install opencv-python matplotlib pandas seaborn geopy folium scipy
```

### Chạy notebook
1. Mở Jupyter Notebook.
2. Mở file .ipynb tương ứng.
3. Chạy từng cell theo thứ tự.

## Tài liệu tham khảo
- [OpenCV Documentation](https://opencv.org/)
- [Pandas Documentation](https://pandas.pydata.org/)
- [Folium Documentation](https://python-visualization.github.io/folium/)
