# Báo cáo phân tích (IPO)

Xác định Input: email liên tục thông báo tài khoản đang được đăng nhập trên thiết bị khác, vô tài khoản cá nhân không được phải bắt đăng nhập mật khẩu lại

# Process (Các bước xử lý)
Xác thực lại danh tính bằng số điện thoại cá nhân hoặc CCCD nếu có xác thực và reset lại máy tính nếu đã tải các mã độc về. Thu hồi quyền truy cập
# Output (Trạng thái an toàn đầu ra):
Mã độc bị loại bỏ hoàn toàn khỏi thiết bị.
Toàn bộ Session và Token cũ của hacker giữ trong tay trở nên vô giá trị (Invalidated).
Tài khoản được bảo vệ bằng cơ chế xác thực mới trên thiết bị sạch.

# Triển khai

 Đổi mật khẩu từ thiết bị khác (Thao tác trên Thiết bị sạch)

Kích hoạt hoặc thiết lập lại Xác thực 2 lớp (2FA) bằng ứng dụng 
Thu hồi quyền truy cập (Revoke Token & Key) trên GitHub
Thao tác hủy Personal Access Tokens (PAT):
1. Đăng nhập vào GitHub trên thiết bị sạch.
2. Nhấp vào ảnh đại diện ở góc trên bên phải -> Chọn Settings.
3. Cuộn xuống menu bên trái, chọn Developer settings (ở dưới cùng).
4. Chọn Personal Access Tokens -> Chọn tiếp Tokens (classic) hoặc Fine-grained tokens (tùy loại bạn đã tạo).
5. Tìm các token nghi ngờ hoặc nhấn Delete (hoặc Revoke) toàn bộ các token cũ để hủy ngay lập tức quyền truy cập của hacker qua API.