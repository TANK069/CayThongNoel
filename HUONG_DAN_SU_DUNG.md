# 🎄 Hướng Dẫn Sử Dụng Christmas Tree 3D

## 📋 Tổng Quan

File **`christmas_tree_touch&gesture_Cloudimages.html`** là file chính để chia sẻ, có đầy đủ tính năng:
- ✅ Điều khiển bằng cử chỉ tay (AI MediaPipe)
- ✅ Điều khiển bằng touch/mouse
- ✅ Hỗ trợ ảnh từ Cloud (URL)
- ✅ Hỗ trợ ảnh từ Local (thư mục images/)
- ✅ 3 chế độ: TREE, SCATTER, FOCUS

## 🚀 Cách Sử Dụng

### Phương án 1: Dùng Ảnh Cloud (Khuyến nghị cho chia sẻ online)

1. **Mở file HTML** trong trình soạn thảo
2. **Tìm phần** `CONFIG.preload.cloudImageUrls` (dòng ~386)
3. **Thêm URL ảnh** của bạn:
   ```javascript
   cloudImageUrls: [
       "https://your-domain.com/image1.jpg",
       "https://your-domain.com/image2.png",
       // ... thêm nhiều URL khác
   ]
   ```
4. **Lưu file** và mở trong trình duyệt
5. **Upload lên server** và chia sẻ link

**Lưu ý:** URL phải cho phép CORS (cross-origin). Nếu không, ảnh sẽ không load được.

### Phương án 2: Dùng Ảnh Local (Khuyến nghị cho offline)

1. **Tạo thư mục** `images/` cùng cấp với file HTML
2. **Đặt tên ảnh** theo format: `(1).jpg`, `(2).jpg`, `(3).png`, ...
3. **Mở file HTML**, tìm `CONFIG.preload.autoScanLocal` (dòng ~396)
4. **Đổi thành** `autoScanLocal: true`
5. **Lưu file** và mở trong trình duyệt
6. **Nén cả HTML + thư mục images/** thành ZIP để chia sẻ

### Phương án 3: Tạo Ảnh Demo Tự Động

1. **Mở file** `images/generate-demo-images.html` trong trình duyệt
2. **Nhấn nút** "Tạo Ảnh Demo"
3. **5 ảnh demo** sẽ được tải xuống tự động
4. **Di chuyển** các file vào thư mục `images/`
5. **Bật** `autoScanLocal: true` trong file HTML chính

## 🎮 Cách Điều Khiển

### Bằng Cử Chỉ Tay (AI):
- **Nắm tay** → Chế độ TREE (cây thông)
- **Mở tay** → Chế độ SCATTER (tán rộng)
- **Pinch (ngón cái + ngón trỏ)** → Chế độ FOCUS (zoom ảnh)

### Bằng Touch/Mouse:
- **Kéo** → Xoay cây thông
- **Click/Tap ảnh** → Zoom vào ảnh đó
- **Double tap** → Chuyển giữa TREE và SCATTER
- **Nút ở dưới** → Chuyển chế độ thủ công

### Phím Tắt:
- **H** → Ẩn/hiện UI controls

## 📁 Cấu Trúc Thư Mục

```
gesture-Christmas_tree-3d_with_photo-main/
├── christmas_tree_touch&gesture_Cloudimages.html  ← File chính
├── images/                                         ← Thư mục ảnh (nếu dùng local)
│   ├── README.md
│   ├── generate-demo-images.html                   ← Tool tạo ảnh demo
│   ├── (1).jpg                                     ← Ảnh của bạn
│   ├── (2).jpg
│   └── ...
└── HUONG_DAN_SU_DUNG.md                           ← File này
```

## ⚙️ Cấu Hình Nâng Cao

Trong file HTML, tìm `CONFIG` để tùy chỉnh:

```javascript
const CONFIG = {
    colors: { ... },           // Màu sắc
    particles: {
        count: 1500,            // Số lượng hạt trang trí
        treeHeight: 24,         // Chiều cao cây
        treeRadius: 8           // Bán kính cây
    },
    camera: { z: 50 },         // Vị trí camera
    preload: { ... }           // Cấu hình ảnh
}
```

## ❓ Câu Hỏi Thường Gặp

**Q: Ảnh không hiển thị?**
- A: Kiểm tra URL có cho phép CORS không, hoặc kiểm tra tên file local có đúng format `(1).jpg` không.

**Q: Làm sao thêm nhiều ảnh?**
- A: Thêm URL vào `cloudImageUrls` hoặc thêm file vào thư mục `images/` với tên `(6).jpg`, `(7).jpg`, ...

**Q: Có thể dùng cả cloud và local không?**
- A: Có! Bật cả `useCloudImages: true` và `autoScanLocal: true`. Cloud sẽ load trước, local làm backup.

**Q: File quá nặng?**
- A: Nén ảnh trước khi thêm vào. Khuyến nghị: JPG chất lượng 80%, kích thước < 500KB mỗi ảnh.

## 📝 Ghi Chú

- File HTML này độc lập, không cần server để chạy (trừ khi dùng cloud images)
- Hỗ trợ tất cả trình duyệt hiện đại (Chrome, Firefox, Safari, Edge)
- Camera chỉ hoạt động trên HTTPS hoặc localhost (yêu cầu của trình duyệt)

---

**Chúc bạn có một Giáng Sinh vui vẻ! 🎄🎅**

