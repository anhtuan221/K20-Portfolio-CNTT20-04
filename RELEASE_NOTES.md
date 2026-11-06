# Release Notes - Portfolio CV v7

## Thông tin bàn giao

- **Sản phẩm:** Portfolio CV cá nhân - Nguyễn Văn Anh Tuấn
- **Phiên bản:** v7
- **Ngày cập nhật:** 2026-10-30
- **Repository:** [anhtuan221/K20-Portfolio-CNTT20-04](https://github.com/anhtuan221/K20-Portfolio-CNTT20-04)
- **Website:** [GitHub Pages](https://anhtuan221.github.io/K20-Portfolio-CNTT20-04/)

## Thay đổi chính

- Hoàn thiện README với mô tả sản phẩm, cấu trúc thư mục, cách chạy local và hướng dẫn kiểm tra các phần chính.
- Ghi lại quá trình phát hiện, quyết định sửa và giới hạn kiểm thử trong [AI_LOG.md](./AI_LOG.md).
- Sửa liên kết stylesheet thành đường dẫn tương đối trong [index.html](./index.html) và [ket-qua.html](./ket-qua.html).
- Sửa đường dẫn ảnh đại diện và ảnh minh họa dự án trong [index.html](./index.html) theo vị trí thực tế dưới `assets/`.

## Lỗi đã sửa

- Đường dẫn tuyệt đối trên máy Windows làm CSS không tải được khi mở ở máy khác hoặc trên GitHub Pages.
- Đường dẫn ảnh bắt đầu từ gốc website không trỏ tới các tệp thực tế trong `assets/`.

## Commit liên quan và mã nguồn bàn giao

- **Commit nền hiện tại:** [`6ffcaff`](https://github.com/anhtuan221/K20-Portfolio-CNTT20-04/commit/6ffcaff) (`Add files via upload`).
- Các thay đổi v7 nêu trong tài liệu này **chưa có commit riêng**; chúng là các thay đổi đang có trong working tree của thư mục dự án. Vì vậy commit trên chỉ là mốc nền, không chứa các cập nhật v7. Không dùng riêng commit đó làm bản mã v7 đã nộp.
- Bản mã v7 cần bàn giao là các tệp trong cùng thư mục dự án này, gồm `index.html`, `ket-qua.html`, `css/style.css`, `assets/`, `README.md`, `AI_LOG.md` và tài liệu này. Sau khi tạo commit và đẩy lên repository, thay liên kết commit nền bằng commit chứa các thay đổi v7 để có thể truy cập chính xác bản mã đã nộp.

## Hạn chế còn lại

- Form liên hệ chỉ dùng xác thực HTML5 và gửi dữ liệu bằng GET tới trang kết quả; không gửi email hay lưu dữ liệu lên máy chủ, và dữ liệu có thể xuất hiện trên URL.
- Các liên kết GitHub trong thẻ dự án vẫn là nội dung chờ cập nhật.
- Sau các thay đổi v7, chưa kiểm tra trực quan trên trình duyệt và chưa xác nhận CSS/ảnh trên GitHub Pages đã được cập nhật.

## Tiếp tục kiểm tra và bàn giao

1. Từ thư mục dự án, chạy `py -m http.server 8000` (hoặc `python -m http.server 8000`) và mở `http://localhost:8000`.
2. Kiểm tra CSS, ảnh, menu, mục dự án/học tập/liên hệ; thử form với dữ liệu không hợp lệ và hợp lệ, xác nhận trang `ket-qua.html` mở ra.
3. Nếu kiểm tra đạt, tạo commit chứa các tệp v7, đẩy lên nhánh xuất bản và cập nhật mục **Commit liên quan** ở trên bằng hash/URL commit đó.
4. Sau khi GitHub Pages triển khai xong, mở URL website, kiểm tra lại các tài nguyên trong Network và lỗi trong Console. Chỉ ghi nhận kết quả sau khi đã thực hiện.

Hướng dẫn local chi tiết và danh sách bước kiểm tra cũng có trong [README.md](./README.md).
