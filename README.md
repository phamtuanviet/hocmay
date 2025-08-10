# Cách thực thi Notebook trên Kaggle

## 1. Thành viên nhóm và thông tin Kaggle
- **Nhóm:** 3
- **Thành viên:**
  - Phạm Đức Thiện – MSSV: 23020160  
  - Phạm Tuấn Việt – MSSV: 23020172  
  - Lê Hoàng Việt – MSSV: 23020169
- **Tên nhóm trên Kaggle:** INT3405_Nhom_3.
- **Tên file notebook:** `final-ml.ipynb`
- **Thành tích trên Kaggle:** 0.386 (Vị trí thứ 26)

---

## 2. Hướng dẫn chạy `final-ml.ipynb` trên Kaggle

### Bước 1: Truy cập và đăng nhập Kaggle
- Mở [https://www.kaggle.com/](https://www.kaggle.com/)  
- Đăng nhập bằng tài khoản cá nhân.

### Bước 2: Tạo hoặc tải notebook
- **Cách 1:** Vào **Code → New Notebook**, sau đó copy toàn bộ nội dung từ `final-ml.ipynb` vào.
- **Cách 2:** Chọn **Upload Notebook** và tải file `final-ml.ipynb` từ máy tính lên.

---

### Lưu ý quan trọng trước khi chạy bước 3:
- Việc xử lý dữ liệu ban đầu có thể mất nhiều thời gian và có nguy cơ **Run Out of Time** trên Kaggle.  
- Vì vậy, **ngay sau khi chạy notebook lần đầu**, cần lưu các file trung gian ra **dataset cá nhân** để tái sử dụng:
  - `a_raw_train.npy`
  - `f_raw_train.npy`
  - `a_wv_depth.npy`
- __Có thể lưu__ mô hình đã train:
  - `mu_model.pkl`
  - `sigma_model.pkl`
- Sau khi lưu, chỉnh lại đường dẫn (`path`) trong code để trỏ tới các file đã lưu trong dataset cá nhân.
- Bạn **phải thay `data03` và `model01` bằng tên path dataset/model của mình**):
```python
/kaggle/input/data03/f_raw_train.npy
/kaggle/input/data03/a_raw_train.npy
/kaggle/input/data03/a_wv_depth.npy

/kaggle/input/model01/scikitlearn/default/1/mu_model.pkl
/kaggle/input/model01/scikitlearn/default/1/sigma_model.pkl
```
- Khi chạy lần tiếp theo, notebook sẽ **bỏ qua bước xử lý ban đầu** và sử dụng trực tiếp các file đã lưu, giúp tiết kiệm thời gian và đảm bảo hoàn thành chạy.

---

### Bước 3: Thêm dữ liệu
- Mở tab **Settings** bên phải → **Add Data** → Chọn dataset cần sử dụng (ariel-data-challenge-2025).

### Bước 4: Chạy code
- Nhấn vào Save Version → Save, đợi kết quả phản hồi.

