**Traffic Detection using Yolov9**

Link project: https://universe.roboflow.com/trafficsignyolov9/traffic-sign-detection-2lmuq-ysmmk

Nhận dạng biển báo giao thông là một lĩnh vực nghiên cứu quan trọng
trong an toàn giao thông. Việc phát triển các hệ thống nhận dạng biển báo
giao thông hiệu quả có thể góp phần giúp người lái xe tuân thủ luật lệ giao
thông, tránh vi phạm và giảm thiểu nguy cơ xảy ra tai nạn.
Đề tài nghiên cứu này tập trung vào việc phát triển một hệ thống nhận
dạng biển báo giao thông sử dụng mô hình YOLOv9. Hệ thống này có thể
nhận diện chính xác các loại biển báo giao thông phổ biến tại Việt Nam
trong điều kiện môi trường thực tế.

**Thực nghiệm**

1 Thu thập dữ liệu

Loại dữ liệu:

Ảnh biển báo giao thông:

• Thu thập ảnh từ nhiều nguồn như internet, cơ sở dữ liệu giao thông,
ảnh chụp thực tế.

• Sử dụng Roboflow để tạo bộ dữ liệu và quản lý ảnh hiệu quả.
Roboflow cung cấp các công cụ giúp thu thập, chú thích và tổ chức
ảnh dễ dàng, đồng thời cho phép cộng tác nhóm và theo dõi tiến trình.

Ảnh nền: Thu thập ảnh nền đường phố từ internet kết hợp với ảnh chụp
thực tế.

2 Xử lý dữ liệu

a) Tiền xử lý ảnh: Sử dụng Roboflow để tự động tiền xử lý ảnh, bao gồm thay đổi kích thước (640x640), cắt, xoay, chỉnh sửa độ tương phản, độ
phơi sáng nhằm cải thiện và tăng cường dữ liệu. Đồng thời áp dụng
hiệu ứng hình ảnh (chỉnh độ sáng tối và làm mờ ảnh để tạo giả định
điều kiện thời tiết xấu). Roboflow cung cấp các công cụ mạnh mẽ giúp
chuẩn hóa dữ liệu và cải thiện hiệu suất mô hình.

b) Tập dữ liệu:

Có 5275 ảnh rõ nét và đủ sáng tương ứng với môi trường thời tiết ban
ngày, không có hiện tượng thời tiết bất thường được chia làm 3 tệp

• Train set: 5331 ảnh

• Valid set: 681 ảnh

• Test set: 512 ảnh


c) Gán nhãn dữ liệu:

Sử dụng công cụ gán nhãn ảnh trong Roboflow để đánh dấu vị trí và
loại của từng biển báo giao thông trong ảnh. Roboflow hỗ trợ gán nhãn
theo nhóm, đảm bảo độ chính xác và nhất quán của nhãn dữ liệu.
Nhãn dữ liệu là mã biển báo được lấy từ Quy chuẩn kỹ thuật quốc gia
về báo hiệu đường bộ (QCVN 41:2019/BGTVT, hay Quy chuẩn 41) do
Tổng cục Đường bộ Việt Nam biên soạn, Bộ Khoa học và Công nghệ
Việt Nam thẩm định, Bộ trưởng Bộ Giao thông vận tải Việt Nam ban
hành năm 2020.

3 Huấn luyện mô hình YOLOv9 trên Colab

Lựa chọn bộ khung: Sử dụng bộ khung YOLOv9 được cung cấp sẵn
hoặc tùy chỉnh bộ khung theo nhu cầu.

Thiết lập cấu trúc mạng nơ-ron: Chọn số lượng lớp mạng nơ-ron, kích
thước bộ lọc, hàm kích hoạt, v.v.

Chọn thuật toán tối ưu hóa: Sử dụng thuật toán tối ưu hóa phù hợp như
Adam, SGD, v.v.

Thiết lập hàm mất mát: Sử dụng hàm mất mát phù hợp cho bài toán
nhận dạng biển báo giao thông, ví dụ như hàm mất mát IOU (Intersection
over Union).

Huấn luyện mô hình trên Google Colab:

• Sử dụng Google Colab để tận dụng tài nguyên tính toán đám mây
mạnh mẽ cho việc huấn luyện mô hình.

• Tải bộ dữ liệu đã được xử lý từ Roboflow lên Google Colab.

• Viết mã để huấn luyện mô hình YOLOv9, theo dõi hiệu suất trên tập
xác nhận và điều chỉnh các tham số mô hình khi cần thiết.

• Lưu mô hình đã được huấn luyện trên Google Colab hoặc tải xuống
máy tính để sử dụng sau.
