## Setup Environment

Flow chạy project
1. Download file .zip từ Google Drive
2. Giải nén project
3. Mở folder project bằng VS Code
4. Đảm bảo folder chứa data train nằm cùng thư mục với file code
5. Đổi biến train_dir trong code thành tên folder chứa dataset
6. Chạy file notebook hoặc file Python để train model

Ví dụ:

train_dir = "data"

Cấu trúc thư mục:

project/
│
├── train.ipynb
├── data/
│ ├── class_1/
│ ├── class_2/
│ └── class_3/


Trong đó:
- `dataset` là folder chính chứa dữ liệu train
- Các folder con (`class_1`, `class_2`, ...) là tên nhãn dữ liệu
  
### 1. Yêu cầu

* Python 3.11 hoặc 3.12 (64-bit)
* VS Code hoặc Jupyter Notebook

> Không nên dùng Python 3.14 vì TensorFlow chưa hỗ trợ ổn định.

---

## 2. Clone project

```bash
git clone <your-repository-link>
cd <project-folder>
```

---

## 3. Tạo môi trường ảo

### Windows

Nếu dùng Python 3.11:

```bash
py -3.11 -m venv venv
```

Nếu dùng Python 3.12:

```bash
py -3.12 -m venv venv
```

Kích hoạt môi trường ảo:

```bash
.\venv\Scripts\Activate.ps1
```

Nếu PowerShell báo lỗi quyền:

```bash
Set-ExecutionPolicy -Scope Process -ExecutionPolicy RemoteSigned
```

Sau đó chạy lại:

```bash
.\venv\Scripts\Activate.ps1
```

Khi thành công sẽ hiện:

```bash
(venv)
```

---

## 4. Cài thư viện

Nâng cấp pip:

```bash
python -m pip install --upgrade pip
```

Cài các thư viện cần thiết:

```bash
pip install tensorflow keras opencv-python matplotlib numpy
```

Nếu chạy notebook:

```bash
pip install notebook ipykernel
```

---

## 5. Kiểm tra TensorFlow

```bash
python -c "import tensorflow as tf; print(tf.__version__)"
```

Nếu terminal hiện version TensorFlow nghĩa là cài đặt thành công.

Ví dụ:

```bash
2.18.0
```

---

## 6. Chọn đúng Kernel trong VS Code

1. Mở file `.ipynb`
2. Chọn **Select Kernel**
3. Chọn môi trường `venv`

Kiểm tra bằng:

```python
import sys
print(sys.executable)
```

Nếu xuất hiện:

```bash
venv\Scripts\python.exe
```

nghĩa là notebook đang chạy đúng môi trường.

---

## 7. Một số lỗi thường gặp

### Không cài được TensorFlow

```bash
ERROR: Could not find a version that satisfies the requirement tensorflow
```

Cách sửa:

* Dùng Python 3.11 hoặc 3.12
* Xóa môi trường ảo cũ
* Tạo lại `venv`
* Cài lại thư viện

---

### Keras báo thiếu TensorFlow

```bash
ModuleNotFoundError: No module named 'tensorflow'
```

Cài lại TensorFlow:

```bash
pip install tensorflow
```

---

# AI_BTVN_Week3_CNN_CN
