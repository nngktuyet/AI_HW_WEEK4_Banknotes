# Banknote Recognition

## 1. Giới thiệu

Đây là project nhận diện mệnh giá tiền giấy bằng mô hình **Convolutional Neural Network (CNN)**.

Mục tiêu của project là huấn luyện model để phân loại ảnh tiền theo từng mệnh giá. Khi đưa vào một ảnh tiền, hệ thống sẽ dự đoán ảnh đó thuộc mệnh giá nào.

---

## 2. File chính

```text
AI_HW_vnbanknotes.ipynb
```

File này dùng để:

* Load dữ liệu ảnh tiền.
* Tiền xử lý ảnh.
* Train mô hình CNN.
* Đánh giá accuracy/loss.
* Dự đoán mệnh giá tiền từ ảnh mới.

---

## 3. Cài đặt môi trường

Mở Terminal trong thư mục project:

```bash
cd /Users/nguyenngockimtuyet/AI_HW
```

Cài các thư viện cần thiết:

```bash
python3 -m pip install tensorflow keras opencv-python numpy matplotlib
```

Nếu dùng Windows:

```bash
pip install tensorflow keras opencv-python numpy matplotlib
```

---

## 4. Cấu trúc dữ liệu

Dataset nên được chia thành các folder class theo từng mệnh giá tiền, ví dụ:

```text
banknote_data/
├── 1000/
├── 2000/
├── 5000/
├── 10000/
├── 20000/
├── 50000/
├── 100000/
├── 200000/
└── 500000/
```

Mỗi folder chứa ảnh của đúng mệnh giá tương ứng.

Nếu dataset có cả mặt trước và mặt sau của tờ tiền, nên đưa cả hai mặt vào train để model nhận diện tốt hơn trong thực tế.

---

## 5. Quy trình xử lý

```text
Ảnh tiền
→ Resize ảnh
→ Chuẩn hóa pixel
→ Đưa vào mô hình CNN
→ Train model
→ Đánh giá model
→ Dự đoán mệnh giá
```

Mô hình CNN sẽ học các đặc trưng như màu sắc, hoa văn, bố cục và ký hiệu trên từng tờ tiền để phân loại.

---

## 6. Cách chạy

Mở file notebook:

```text
AI_HW_vnbanknotes.ipynb
```

Sau đó chạy lần lượt các cell trong notebook để train và test model.

---

## 7. Output mẫu

```text
Predicted class: 500000
Confidence: 94.52%
```

---

## 8. Kết luận

Project Banknote Recognition giúp áp dụng CNN vào bài toán nhận dạng mệnh giá tiền giấy. Bài này phù hợp để hiểu quy trình cơ bản của một bài toán phân loại ảnh: chuẩn bị dữ liệu, train model, đánh giá và dự đoán ảnh mới.
