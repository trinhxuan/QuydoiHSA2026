# Quy đổi điểm HSA năm 2026

Dự án web tĩnh dùng để quy đổi và dự báo phân vị điểm HSA sang thang điểm THPT A00.

## Thành phần chính

- `index.html`: mã nguồn giao diện và toàn bộ logic quy đổi.
- `.nojekyll`: giúp GitHub Pages phục vụ file tĩnh trực tiếp, không xử lý qua Jekyll.
- `.github/workflows/pages.yml`: cấu hình tự động triển khai GitHub Pages khi đẩy code lên nhánh `main`.

## Công nghệ sử dụng

- HTML/CSS/JavaScript thuần.
- Tailwind CSS qua CDN.
- Chart.js qua CDN.
- MathJax 3 qua CDN.

Dự án không cần bước build, không cần cài đặt Node.js.

## Chạy thử trên máy tính

Mở trực tiếp file `index.html` bằng trình duyệt, hoặc chạy server tĩnh:

```bash
python -m http.server 8000
```

Sau đó mở:

```text
http://localhost:8000
```

## Đưa lên GitHub

### Cách 1: Upload trực tiếp trên GitHub

1. Tạo repository mới trên GitHub, ví dụ: `quydoi-hsa-2026`.
2. Giải nén file dự án ZIP.
3. Upload toàn bộ các file/thư mục trong dự án lên repository.
4. Vào **Settings → Pages**.
5. Ở mục **Build and deployment**, chọn **GitHub Actions**.
6. Đợi workflow chạy xong, GitHub sẽ cấp link web.

### Cách 2: Dùng Git

```bash
git init
git add .
git commit -m "Initial GitHub Pages project"
git branch -M main
git remote add origin https://github.com/<ten-tai-khoan>/<ten-repo>.git
git push -u origin main
```

Sau đó vào **Settings → Pages** và chọn **GitHub Actions**.

## Lưu ý triển khai

File `index.html` đang dùng các thư viện CDN, vì vậy khi mở online cần có kết nối Internet để Tailwind CSS, Chart.js và MathJax tải đầy đủ.

## Giấy phép

Chưa khai báo giấy phép. Nếu muốn công khai cho người khác sử dụng/sửa đổi, hãy bổ sung file `LICENSE` phù hợp.
