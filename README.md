[README.md](https://github.com/user-attachments/files/33296692/README.md)
# Bill QR Manager

Website tĩnh đọc file Excel/CSV ngay trên trình duyệt và tạo mã QR chứa **chỉ mã bill**. Không có backend, không có database và không tải nội dung Excel lên máy chủ của website.

## Tính năng
- Đọc `.xlsx`, `.xls`, `.csv` từ máy tính.
- Hiển thị dữ liệu thành bảng lưới gần giống Excel.
- Tự nhận diện một số tên cột mã bill phổ biến; có thể chọn lại cột bằng danh sách.
- Tìm kiếm toàn bộ bảng.
- Chọn một dòng để xem QR và các thông tin của dòng đó.
- Tải QR thành ảnh PNG hoặc in.
- Có dữ liệu mẫu để thử giao diện.
- Responsive trên máy tính và điện thoại.

## Chạy thử trên máy
1. Giải nén gói ZIP.
2. Mở `index.html` bằng trình duyệt Chrome/Edge khi có Internet.
3. Bấm **Tải file Excel** và chọn file của bạn.

Lưu ý: thư viện SheetJS và QRCode được tải từ CDN, nên cần Internet để tải các thư viện. Dữ liệu Excel vẫn được xử lý trong trình duyệt.

## Đưa lên GitHub Pages
1. Đăng nhập GitHub và tạo repository mới, ví dụ `bill-qr-manager`.
2. Đặt repository ở chế độ **Public** nếu bạn muốn dùng GitHub Pages miễn phí theo thiết lập phổ biến.
3. Tải `index.html` lên thư mục gốc repository (nút **Add file → Upload files → Commit changes**).
4. Mở **Settings → Pages**.
5. Trong **Build and deployment**, chọn **Deploy from a branch**.
6. Chọn branch `main`, thư mục `/(root)`, sau đó bấm **Save**.
7. Chờ GitHub Pages triển khai và mở đường dẫn được hiển thị trong mục Pages.

## Định dạng file Excel
- Hàng đầu tiên của trang tính đầu tiên được dùng làm tiêu đề cột.
- Các hàng bên dưới được coi là dữ liệu.
- Tên cột nên là `Mã bill`, `Mã vận đơn`, `Mã vận đơn / bill`, `Bill Code` hoặc tương tự.
- Nếu website chọn nhầm cột, hãy chọn lại cột chính xác trong danh sách **Chọn cột mã bill**.
- Nếu mã bill có số 0 ở đầu, nên định dạng cột mã bill là **Text/Văn bản** trong Excel trước khi lưu, để Excel không loại bỏ số 0 đầu.

## Bảo mật và giới hạn
- Không có database, đăng nhập hay đồng bộ dữ liệu giữa thiết bị.
- File được đọc tại trình duyệt, nhưng các thư viện JavaScript được tải từ CDN; cần Internet.
- Không lưu dữ liệu sau khi đóng hoặc tải lại trang. Tải lại file Excel khi cần dùng lại.
- Không dùng QR này để tra cứu trực tuyến: QR chỉ chứa chuỗi mã bill. Muốn QR mở một trang web, cần thay đổi yêu cầu QR.
- Chỉ tải lên file mà bạn được phép xử lý; cân nhắc quy định bảo mật dữ liệu nội bộ của đơn vị.
