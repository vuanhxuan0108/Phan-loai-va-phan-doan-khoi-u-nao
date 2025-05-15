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
