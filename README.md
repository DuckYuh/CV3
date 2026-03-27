# Ghép ảnh toàn cảnh (Panoramic Photos– Image Stitching)

## 📌 Giới thiệu
Project thực hiện ghép nhiều ảnh thành ảnh toàn cảnh (panorama) bằng phương pháp dựa trên đặc trưng (feature-based image stitching).

---

## 🎯 Mục tiêu
- Hiểu pipeline ghép ảnh panorama
- Thực hiện các bước: feature detection, matching, homography, stitching
- Sử dụng ít nhất hai phương pháp trích xuất đặc trưng khác
nhau
- Áp dụng cùng một pipeline ghép ảnh cho các phương pháp trích xuất đặc trưng
khác nhau
-  Sosánh kết quả ghép ảnh thu được về độ chính xác căn chỉnh, tính liên tục của ảnh
và chất lượng trực quan

---

## ⚙️ Pipeline

1. Load và tiền xử lý ảnh (chuyển ảnh xám, chuẩn hóa kích thước nếu cần).
2. Trích xuất đặc trưng (feature detection và description).
3. So khớp đặc trưng giữa các cặp ảnh.
4. Ước lượng phép biến đổi hình học (homography) giữa các ảnh.
5. Căn chỉnh ảnh và ghép ảnh để tạo panorama.
6. Xử lý vùng chồng lấn và biên ảnh (blending) ở mức cơ bản.

---

## 🧪 Phương pháp sử dụng

- **SIFT**
  - Độ chính xác cao
  - Ổn định với nhiều loại ảnh

- **BRISK**
  - Tốc độ nhanh
  - Độ chính xác thấp hơn SIFT

---

## 📁 Dữ liệu
- 3 ảnh chụp cùng một cảnh

---

## ▶️ Công cụ sử dụng
- Python
- OpenCV
- NumPy
- Jupyter Notebook

---

## ⚠️ Lưu ý
- Ảnh đầu vào được lưu trong thư mục `images/`.
- Ảnh cần có vùng chồng lấn
- Nên resize ảnh để tăng tốc độ xử lý
- Thứ tự ảnh ảnh hưởng đến kết quả ghép
