# Thư mục Ảnh - Christmas Tree

## 📁 Cách sử dụng ảnh Local

### Đặt tên file ảnh:
- `(1).jpg` hoặc `(1).png`
- `(2).jpg` hoặc `(2).png`
- `(3).jpg` hoặc `(3).png`
- ... và tiếp tục

### Lưu ý:
- Tên file phải có dấu ngoặc đơn: `(1)`, `(2)`, `(3)`, ...
- Hỗ trợ định dạng: `.jpg`, `.jpeg`, `.png`
- File sẽ được tự động tìm và load vào cây thông

### Ví dụ cấu trúc:
```
images/
  ├── (1).jpg
  ├── (2).png
  ├── (3).jpg
  ├── (4).jpeg
  └── ...
```

## 🖼️ Tạo ảnh demo

Mở file `generate-demo-images.html` trong trình duyệt để tạo ảnh demo tự động.

## 📝 Cách bật Local Images

Trong file HTML, tìm phần `CONFIG.preload` và đổi:
```javascript
autoScanLocal: true,  // Đổi từ false thành true
```

