# Portfolio CV - Nguyễn Văn Anh Tuấn

Website portfolio cá nhân giới thiệu thông tin, kỹ năng, dự án học tập, quá trình học tập và thông tin liên hệ của Nguyễn Văn Anh Tuấn. Sản phẩm được xây dựng bằng HTML và CSS thuần, không cần bước biên dịch.

## Thông tin và liên kết

- **Tác giả:** Nguyễn Văn Anh Tuấn
- **Hồ sơ GitHub:** [github.com/anhtuan221](https://github.com/anhtuan221)
- **Mã nguồn:** [anhtuan221/K20-Portfolio-CNTT20-04](https://github.com/anhtuan221/K20-Portfolio-CNTT20-04)
- **Website GitHub Pages:** [https://anhtuan221.github.io/K20-Portfolio-CNTT20-04/](https://anhtuan221.github.io/K20-Portfolio-CNTT20-04/)
- **Minh chứng/nhật ký kiểm tra:** [AI_LOG.md](./AI_LOG.md)
- **Ghi chú bàn giao v7:** [RELEASE_NOTES.md](./RELEASE_NOTES.md)

## Cấu trúc thư mục

```text
.
├── index.html          # Trang portfolio chính
├── ket-qua.html        # Trang kết quả sau khi gửi form liên hệ
├── css/
│   └── style.css       # Giao diện và responsive
├── assets/             # Ảnh đại diện và hình minh họa dự án
├── AI_LOG.md           # Nhật ký kiểm tra lỗi
├── RELEASE_NOTES.md    # Ghi chú bàn giao phiên bản v7
└── README.md
```

## Chạy trên máy local

Cần có Python 3 và trình duyệt web hiện đại. Từ thư mục dự án, chạy:

```powershell
py -m http.server 8000
```

Mở [http://localhost:8000](http://localhost:8000) trên trình duyệt. Nếu lệnh `py` không có trên máy, có thể dùng `python -m http.server 8000`. Dừng máy chủ bằng `Ctrl+C`.

## Kiểm tra các trang và chức năng

1. Mở `index.html` qua máy chủ local hoặc URL GitHub Pages.
2. Dùng menu đầu trang để kiểm tra các mục Giới thiệu, Kỹ năng, Dự án, Học tập và Liên hệ; kiểm tra ảnh đại diện và hình minh họa dự án.
3. Trong phần Liên hệ, thử gửi form để trống hoặc nhập email sai định dạng để kiểm tra xác thực của trình duyệt. Form yêu cầu họ tên tối thiểu 2 ký tự, lời nhắn từ 10 đến 500 ký tự và email đúng định dạng.
4. Nhập dữ liệu hợp lệ rồi gửi để kiểm tra điều hướng tới `ket-qua.html`. Form dùng phương thức GET nên dữ liệu sẽ xuất hiện trên URL; đây chỉ là chức năng thực hành, không gửi email và không lưu dữ liệu lên máy chủ.
5. Kiểm tra liên kết email và hồ sơ GitHub trong phần Liên hệ.

## Xuất bản

Website được xuất bản tĩnh bằng GitHub Pages tại liên kết ở trên. Mã nguồn gồm các tệp HTML, CSS và tài nguyên trong repository; không cần cài thư viện hay chạy quy trình build.
