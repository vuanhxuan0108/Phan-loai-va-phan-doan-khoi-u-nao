# Phân loại và phân đoạn khối u não

## Giới thiệu
Dự án này áp dụng học sâu để thực hiện hai nhiệm vụ chính:
1. **Phân loại khối u não**: Xác định loại khối u từ ảnh MRI sử dụng mô hình ResNet50.
2. **Phân đoạn khối u não**: Xác định vùng bị ảnh hưởng trong ảnh MRI bằng mô hình U-Net.

## Công nghệ sử dụng
- **ResNet50**: Mô hình CNN mạnh mẽ để phân loại ảnh, được xây dựng thủ công từ đầu bằng TensorFlow/Keras thay vì sử dụng mô hình pretrained.
- **U-Net**: Kiến trúc deep learning phổ biến trong bài toán phân đoạn ảnh y tế, được thiết kế và huấn luyện từ đầu mà không dựa vào mô hình có sẵn.
- **TensorFlow/Keras**: Thư viện chính để xây dựng và huấn luyện mô hình.
- **OpenCV & NumPy**: Tiền xử lý ảnh trước khi đưa vào mô hình.

## Cách cài đặt và chạy dự án

### 1. Cài đặt môi trường
Trước tiên, cài đặt các thư viện cần thiết:
```bash
pip install -r requirements.txt
```

### 2. Huấn luyện mô hình
Dự án này đã cung cấp mô hình huấn luyện sẵn (`modelResnet50.h5` cho phân loại và `Unet_tumor.h5` cho phân đoạn). Nếu muốn huấn luyện lại, bạn có thể chạy các tệp notebook tương ứng:
```bash
jupyter notebook resnet-tumor.ipynb  # Huấn luyện mô hình ResNet50
jupyter notebook unet-tumor.ipynb  # Huấn luyện mô hình U-Net
```

### 3. Dự đoán với mô hình đã huấn luyện
Mở file `main.ipynb` và chạy các bước dự đoán hoặc sử dụng các tệp notebook tương ứng:
```bash
jupyter notebook main.ipynb  # Chạy pipeline đầy đủ
```

## Cấu trúc thư mục
```
├── datasets/  # Chứa dữ liệu MRI
├── Unet_tumor.h5  # Mô hình U-Net đã huấn luyện
├── modelResnet50.h5  # Mô hình ResNet50 đã huấn luyện
├── main.ipynb  # Pipeline đầy đủ
├── resnet-tumor.ipynb  # Huấn luyện mô hình ResNet50
├── unet-tumor.ipynb  # Huấn luyện mô hình U-Net
├── .gitattributes  # Cấu hình Git
└── README.md  # Tài liệu hướng dẫn
```

## Đóng góp
Bạn có thể fork repository này và tạo pull request để đóng góp.

## Giấy phép
Dự án này được phát hành theo giấy phép MIT.
