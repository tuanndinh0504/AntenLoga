# 📡 LPDA Antenna Design & Simulation (500 MHz - 1.2 GHz)

[![Ansys HFSS](https://img.shields.io/badge/Simulation-Ansys%20HFSS-red.svg)](https://www.ansys.com/products/electronics/ansys-hfss)
[![Python](https://img.shields.io/badge/Automation-PyAEDT-blue.svg)](https://aedt.docs.pyansys.com/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

Mô phỏng, tối ưu hóa và tự động hóa thiết kế Anten Dipole Định kỳ Logarithm (**Log-Periodic Dipole Array - LPDA**) hoạt động trong dải tần **500 MHz đến 1.2 GHz**. 

Dự án này ứng dụng **Ansys HFSS** kết hợp với **PyAEDT (Python)** để dựng mô hình hình học, tính toán thông số mạng truyền dẫn, phỏng đoán đáp ứng trở kháng và tối ưu hóa giản đồ bức xạ.

---

## 💡 HƯỚNG DẪN THÊM VÀO GITHUB (QUICK GUIDE)

1. Mở Repository **`antenloga`** trên GitHub.
2. Bấm nút **Add file** -> Chọn **Create new file**.
3. Tại ô tên file, nhập: `README.md`.
4. Dán (Paste) toàn bộ nội dung từ dòng tiêu đề `# 📡 LPDA Antenna...` trở đi.
5. Kéo xuống dưới và bấm **Commit changes...** để hoàn tất.

---

## 📌 Tính năng chính (Key Features)

* **Thiết kế dải rộng (Wideband Design):** Hoạt động ổn định trên dải tần rộng từ 500 MHz đến 1.2 GHz với hệ số sóng đứng VSWR < 2.0.
* **Tự động hóa với PyAEDT:** Script Python cho phép tự động tính toán kích thước các phần tử (dipole lengths, spacings) dựa trên hệ số tỉ lệ $\tau$ và hệ số khoảng cách $\sigma$.
* **Phân tích chi tiết trong HFSS:**
  * Thông số $S_{11}$ (Return Loss) và trở kháng đầu vào $Z_{in}$.
  * Giản đồ bức xạ 2D/3D (Far-field Radiation Pattern).
  * Hệ số định hướng (Directivity) và Độ lợi (Gain) trên toàn dải tần.

---

## 📐 Thông số kỹ thuật (Specifications)

| Thông số (Parameter) | Giá trị (Value) |
| :--- | :--- |
| **Dải tần hoạt động (Frequency Range)** | 500 MHz – 1.2 GHz |
| **Trở kháng danh định (Nominal Impedance)** | 50 $\Omega$ |
| **Hệ số thiết kế $\tau$ (Tau)** | 0.82 - 0.88 |
| **Hệ số khoảng cách $\sigma$ (Sigma)** | 0.14 - 0.17 |
| **Độ lợi trung bình (Average Gain)** | > 6 - 8 dBi |
| **Hệ số sóng đứng (VSWR)** | $\le$ 2.0 |

---

## 🚀 Hướng dẫn cài đặt & chạy mô phỏng (Execution Guide)

### Yêu cầu hệ thống (Prerequisites)
* **Ansys HFSS** (Phiên bản 2021 R2 trở lên)
* **Python 3.8+**
* Các thư viện Python cần thiết:
  pip install pyaedt numpy matplotlib

### Các bước thực hiện
1. Mở phần mềm Ansys HFSS trên máy tính.
2. Mở Terminal / Command Prompt tại thư mục dự án và chạy câu lệnh:
   python scripts/hfss_automation.py
3. Script sẽ tự động kết nối với HFSS, khởi tạo tham số hình học, đặt nguồn nuôi (Lumped Port) và chạy thiết lập Sweep phân tích tần số.

---

## 📊 Kết quả mô phỏng (Simulation Results)

* **Return Loss ($S_{11}$):** Đạt dưới -10 dB trên toàn bộ dải tần từ 500 MHz đến 1.2 GHz.
* **Radiation Pattern:** Giản đồ bức xạ định hướng rõ rệt về phía các phần tử ngắn (hướng đỉnh anten), tỉ số Front-to-Back (F/B ratio) đạt mức tối ưu.

---

## 🛠️ Công nghệ sử dụng (Technologies Used)

* **Ansys HFSS / Electronics Desktop** - Phân tích trường điện từ 3D.
* **PyAEDT** - Thư viện Python chính thức kết nối Ansys Electronics Desktop.
* **Python (NumPy, Matplotlib)** - Tính toán tham số anten và xử lý đồ thị.
