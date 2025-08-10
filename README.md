# Hướng dẫn thực thi Notebook trên Kaggle – Ariel Data Challenge 2025

## 1. Thông tin nhóm và kết quả

- **Nhóm:** 3
- **Thành viên:**
  - Phạm Đức Thiện – MSSV: 23020160
  - Phạm Tuấn Việt – MSSV: 23020172
  - Lê Hoàng Việt – MSSV: 23020169
- **Tên nhóm trên Kaggle:** INT3405\_Nhom\_3
- **Tên file notebook và điểm số:**
  - `final-ml-xgboost.ipynb` – Điểm: **0.386** (Vị trí 26)
  - `final-ml-linear.ipynb` – Điểm: **0.314**

---

## 2. Chuẩn bị môi trường trên Kaggle

### Bước 1: Đăng nhập Kaggle

- Truy cập [https://www.kaggle.com/](https://www.kaggle.com/) và đăng nhập bằng tài khoản cá nhân.

### Bước 2: Tạo hoặc tải Notebook

- **Cách 1:** Vào **Code → New Notebook**, copy toàn bộ code từ file `.ipynb` vào.
- **Cách 2:** Chọn **Upload Notebook** để tải file `.ipynb` từ máy tính.

---

## 3. Chuẩn bị dữ liệu cho Notebook (option)

### Upload trực tiếp file vào Notebook (Nhanh nhất)

1. Tải sẵn các file đã xử lý và model từ Google Drive:\
  [https://drive.google.com/drive/folders/1IAVwHFXasH6\_KVeJ4ogpRvRg4hwJx-cc](https://drive.google.com/drive/folders/1IAVwHFXasH6_KVeJ4ogpRvRg4hwJx-cc)\
   Bao gồm:
   - `a_raw_train.npy`
   - `f_raw_train.npy`
   - `a_wv_depth.npy`
   - `mu_model.pkl` (chọn model thích hợp)
   - `sigma_model.pkl` (chọn model thích hợp)
2. Trong Kaggle Notebook:
   - Sử dụng nút **Upload** ở thanh bên phải để tải file dataset và model:
   - Thay đổi path của các file trong class GlobalVariable cho phù hợp với đường dẫn.
   ```python
    self.f_raw_train_path = '/kaggle/input/data03/f_raw_train.npy'
    self.a_raw_train_path = '/kaggle/input/data03/a_raw_train.npy'
    self.a_wv_depth_path = '/kaggle/input/data03/a_wv_depth.npy'
    self.mu_model_path = '/kaggle/input/model_001/scikitlearn/default/3/mu_model.pkl'
    self.sigma_model_path = '/kaggle/input/model_001/scikitlearn/default/3/sigma_model.pkl'
   ```

---

## 4. Chạy Notebook

- Nhấn **Save Version** → **Save** → đợi Kaggle trả kết quả.

### Lưu ý quan trọng nếu bạn bỏ qua mục 3:
- Việc xử lý dữ liệu ban đầu có thể mất nhiều thời gian và có nguy cơ **Run Out of Time** trên Kaggle.  
- Vì vậy, **ngay sau khi chạy notebook lần đầu**, cần lưu các file trung gian ra **dataset cá nhân** để tái sử dụng:
  - `a_raw_train.npy`
  - `f_raw_train.npy`
  - `a_wv_depth.npy`
- __Có thể lưu__ mô hình đã train:
  - `mu_model.pkl`
  - `sigma_model.pkl`
- Sau khi lưu, chỉnh lại đường dẫn (`path`) trong code để trỏ tới các file đã lưu trong dataset cá nhân.
```python
    self.f_raw_train_path = '/kaggle/input/data03/f_raw_train.npy'
    self.a_raw_train_path = '/kaggle/input/data03/a_raw_train.npy'
    self.a_wv_depth_path = '/kaggle/input/data03/a_wv_depth.npy'
    self.mu_model_path = '/kaggle/input/model_001/scikitlearn/default/3/mu_model.pkl'
    self.sigma_model_path = '/kaggle/input/model_001/scikitlearn/default/3/sigma_model.pkl'
```
- Khi chạy lần tiếp theo, notebook sẽ **bỏ qua bước xử lý ban đầu** và sử dụng trực tiếp các file đã lưu, giúp tiết kiệm thời gian và đảm bảo hoàn thành chạy.

---
*Hết*

