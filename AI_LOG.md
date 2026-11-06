# Nhật ký sử dụng AI - Portfolio CV

## 1. Hiện tượng và dữ kiện ban đầu

- Trang portfolio được ghi nhận có vấn đề tải CSS, ảnh đại diện và ảnh minh họa dự án.
- Trong `index.html` và `ket-qua.html`, đường dẫn CSS là đường dẫn tuyệt đối trên máy Windows (`D:\CNTT20-04\portfolio\css\style.css`), trong khi tệp thực tế nằm ở `css/style.css`.
- Các ảnh trong `index.html` dùng đường dẫn bắt đầu bằng `/`, nhưng các tệp ảnh thực tế nằm trong `assets/`.
- Bản HTML lấy từ GitHub Pages có cùng nội dung đường dẫn chưa phù hợp. Chưa có kết quả kiểm tra trực tiếp bằng DevTools sau khi sửa.

## 2. Nhận định trước khi hỏi AI

Từ cấu trúc thư mục và các tham chiếu trong HTML, tôi nhận định đường dẫn tài nguyên là nguyên nhân có khả năng cao: đường dẫn máy cục bộ không dùng được khi xuất bản, còn đường dẫn ảnh từ `/` trỏ tới gốc website thay vì thư mục `assets/`. Mã phản hồi HTTP 304, nếu có, tự nó không chứng minh tài nguyên bị lỗi; cần kiểm tra URL và trạng thái tải thực tế.

## 3. Công cụ và trao đổi với AI

- **Công cụ:** trợ lý AI đọc các tệp HTML, CSS, cấu trúc thư mục và nội dung trang GitHub Pages; sau đó kiểm tra các tham chiếu nội bộ trong HTML.
- **Prompt tóm tắt:** “Dựa trên các tệp và cấu trúc dự án, hãy cập nhật README phù hợp với sản phẩm thực tế; kiểm tra và sửa đường dẫn tài nguyên đang khiến CSS, ảnh không hiển thị. Ghi rõ cách kiểm tra, không khẳng định những gì chưa thử.”
- **Phản hồi/gợi ý chính:** dùng đường dẫn tương đối `css/style.css` cho CSS; dùng `assets/<tên-tệp>` cho ảnh; kiểm tra từng đường dẫn có tệp tương ứng. Chạy bằng máy chủ HTTP local để tránh khác biệt khi mở tệp trực tiếp.

## 4. Quyết định và lý do

Tôi chọn áp dụng các đường dẫn tương đối được gợi ý vì chúng khớp với vị trí tệp trong repository và hoạt động theo cấu trúc thư mục của website tĩnh. Tôi không coi việc URL Pages tải được nội dung HTML là bằng chứng rằng các tài nguyên đã hiển thị đúng; cần kiểm tra lại riêng sau khi cập nhật/xuất bản.

## 5. Phần đã sửa

- Trong `index.html`, đổi CSS sang `css/style.css`; đổi ảnh đại diện và ba ảnh dự án sang các đường dẫn trong `assets/`.
- Trong `ket-qua.html`, đổi CSS sang `css/style.css`.
- Cập nhật `README.md` với cách chạy local, các trang/chức năng cần kiểm tra và liên kết tới nhật ký này.

## 6. Cách thử lại và kết quả

- Đã chạy kiểm tra tự động trên các giá trị `href`/`src` nội bộ của `index.html` và `ket-qua.html`: tất cả đường dẫn được kiểm tra đều trỏ tới tệp có trong repository.
- Đã chạy `git diff --check` (cấu hình xử lý CRLF của repository được tính đến): không còn lỗi whitespace.
- **Chưa thực hiện:** mở trang trong trình duyệt sau khi sửa, thử form trên local, hoặc xác nhận bản GitHub Pages đã được cập nhật và hiển thị ảnh/CSS. Cần chạy máy chủ local theo hướng dẫn trong README, kiểm tra hai trang và form; sau khi xuất bản, kiểm tra lại URL Pages cùng Network/Console.
