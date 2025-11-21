## Xử Lý Tín Hiệu Lời Nói Trong Miền Tần Số Ngắn Hạn

Kho lưu trữ này chứa một Jupyter Notebook viết bằng Python, tái hiện thí nghiệm “Short-Term Frequency Domain Processing of Speech” của Virtual Lab (IIT Guwahati). Sau khi đặt `toiyeu.wav` cùng thư mục với notebook và kích hoạt môi trường ảo `/.venv_dsp`, hãy chạy lần lượt tất cả các cell.

### Tổng quan các phần

1. **Phân tích toàn bộ tín hiệu (Hình 1)**  
   Nạp `toiyeu.wav`, vẽ toàn bộ dạng sóng và hiển thị phổ biên độ tuyến tính / phổ log thu được từ FFT.

2. **Âm hữu thanh / vô thanh / khoảng lặng (Hình 2)**  
   Cắt ba đoạn 30 ms (ước lượng thời điểm) đại diện cho ba trạng thái, rồi trình bày dạng sóng, phổ tuyến tính và phổ log trong một lưới 3×3.

3. **Biến đổi Fourier ngắn hạn – STFT (Hình 3)**  
   Thực hiện STFT với cửa sổ Hanning 20 ms, bước trượt 10 ms và hiển thị phổ log dạng bản đồ thời gian–tần số.

4. **Phổ thực so với phổ chập (Hình 4)**  
   Tạo sóng sin 200 Hz, phân tích hai độ dài 30 ms và 250 ms, đồng thời vẽ dạng sóng cùng phổ tuyến tính / log cho mỗi độ dài.

5. **So sánh hàm cửa sổ (Hình 5 & 6)**  
   Dùng một đoạn hữu thanh 30 ms, áp dụng cửa sổ chữ nhật, Hamming và Hanning; mỗi cửa sổ được minh họa bằng dạng sóng, phổ tuyến tính và phổ log (lưới 3×3).

6. **Ảnh hưởng của kích thước cửa sổ (Hình 8)**  
   So sánh các đoạn 3 ms, 30 ms và 300 ms (đều được biểu diễn trong khung 300 ms) để cho thấy cửa sổ càng dài thì phổ log càng mịn ra sao.

### Cách chạy notebook

```bash
cd /Users/admin/Documents/xulitinhieuso_102230290
source .venv_dsp/bin/activate
# (chỉ cần lần đầu) pip install notebook
jupyter notebook short_term_frequency_domain_speech.ipynb
```

Hãy để `toiyeu.wav` trong cùng thư mục trước khi chạy Phần 1. Tất cả thư viện Python cần thiết (`numpy`, `scipy`, `matplotlib`, `ipykernel`) đã được cài sẵn trong `/.venv_dsp`.

