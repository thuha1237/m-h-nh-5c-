# m-h-nh-5c-
# 🔮 Ứng dụng Web Dự báo Rủi ro Khách hàng (PD) với Streamlit

Ứng dụng web tương tác trực quan này được phát triển nhằm mục đích chuyển đổi quy trình từ tệp huấn luyện mô hình học máy Jupyter Notebook thành một giải pháp phân tích rủi ro thực tế cho khách hàng chạy trên nền tảng **Streamlit**.

## 🚀 Tính năng & Mô tả ngắn các Tab chức năng
Ứng dụng được thiết kế cấu trúc phân vùng hợp lý (Zoning) với cấu hình luồng dữ liệu ở Sidebar và các khu vực chính được phân chia theo 4 Tab:
1. **📊 Tổng quan dữ liệu:** Xem phân phối kích thước hàng/cột, hiển thị dữ liệu thô và thống kê mô tả tóm tắt của 24 biến độc lập cấu thành mô hình.
2. **📈 Trực quan hóa:** Biểu đồ hóa thông qua biểu đồ cột phân phối lớp (Bar Chart) hoặc Histogram sử dụng thư viện động Plotly cho biến mục tiêu `PD` và các thuộc tính liên quan khác do người dùng tự chọn.
3. **🔬 Kết quả kiểm định:** Tái lập đánh giá hiệu suất mô hình học máy với các chỉ số đo lường chuẩn xác: *Accuracy, Precision, Recall, F1-Score* kèm theo biểu đồ ma trận nhầm lẫn trực quan Heatmap.
4. **🔮 Sử dụng mô hình:** Cung cấp 2 chế độ dự báo:
   - **Nhập thủ công trực tiếp:** Nhập thông số khảo sát của từng khách hàng qua biểu mẫu giao diện an toàn.
   - **Tải tệp danh sách hàng loạt:** Tải lên tệp tập hợp các khách hàng mới cần chấm điểm rủi ro theo đúng định dạng cấu trúc, chạy dự báo đồng loạt và cho phép tải xuống file thành phẩm kết quả.

## 🤖 Thông tin Mô hình Học máy
- **Thuật toán áp dụng:** Mô hình phân loại tuyến tính **Logistic Regression** trích xuất đồng bộ từ quy trình tối ưu hóa dữ liệu của notebook.
- **Tập biến đầu vào (X):** Gồm 24 chỉ tiêu khảo sát định lượng (`TC1` đến `TC5`, `NL1` đến `NL4`, `DK1` đến `DK5`, `V1` đến `V6`, `TS1` đến `TS4`).
- **Biến mục tiêu (y):** Cột định danh nhị phân `PD` (0: Khách hàng an toàn / Không rủi ro; 1: Khách hàng tiềm ẩn rủi ro).

## 🛠️ Hướng dẫn cài đặt và khởi chạy

1. **Chuẩn bị môi trường và cài đặt thư viện phụ thuộc:**
   Đảm bảo bạn đã cài đặt Python (phiên bản khuyến nghị `>=3.9`). Chạy lệnh sau trong Terminal/Command Prompt để tự động tải các gói thư viện cần thiết:
   ```bash
   pip install -r requirements.txt
