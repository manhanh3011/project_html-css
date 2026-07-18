# project_html-css

Dự án xây dựng giao diện tĩnh (static website) dựa trên thiết kế Figma, sử dụng HTML5 và Tailwind CSS v4.

## Công nghệ sử dụng

* **HTML5**: Cấu trúc ngữ nghĩa (Semantic HTML) rõ ràng, chuẩn SEO.
* **Tailwind CSS v4 (CLI)**: Styling giao diện và xử lý Responsive ngay từ đầu.
* **Prettier**: Hỗ trợ format code tự động (đã tích hợp `prettier-plugin-tailwindcss` để sắp xếp class Tailwind chuẩn mực).

## Cấu trúc thư mục cơ bản

* `src/`: Nơi chứa file HTML chính (`index.html`) và file CSS đầu vào (`style.css`).
* `css/`: Thư mục đầu ra, chứa file CSS đã được biên dịch bởi Tailwind (`style.css`).

---

## Hướng dẫn cài đặt và khởi chạy

### 1. Cài đặt các gói phụ thuộc (Dependencies)

Bạn cần cài đặt [Node.js](https://nodejs.org/). Sau đó, mở terminal tại thư mục gốc của dự án và chạy:

```bash
npm install
```

### 2. Chạy môi trường Phát triển (Development)

Trong quá trình code giao diện, bạn cần chạy Tailwind ở chế độ theo dõi (watch mode) để nó tự động biên dịch các class Tailwind mới trong HTML thành CSS.

Chạy lệnh sau trong terminal:

```bash
npm run dev
```

> **Lưu ý:** Để xem giao diện trực tiếp trên trình duyệt với tính năng tự động tải lại (hot-reload), bạn nên cài đặt và sử dụng extension **Live Server** trong VS Code (chuột phải vào file `src/index.html` và chọn *Open with Live Server*).

### 3. Build cho Môi trường Thực tế (Production)

Sau khi hoàn thiện giao diện và chuẩn bị deploy, bạn cần nén (minify) file CSS để giảm tối đa dung lượng tải trang. Chạy lệnh:

```bash
npm run build
```

## Giải thích NPM Scripts

* `npm run dev`: Chạy lệnh `tailwindcss -i ./src/style.css -o ./css/style.css --watch`.
* `npm run build`: Chạy lệnh `tailwindcss -i ./src/style.css -o ./css/style.css --minify`.