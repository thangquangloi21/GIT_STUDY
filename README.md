# 🚀 Học git cùng Lợi

### Cài Đặt

```bash
pip install flask
```

### Khởi Động Server
```bash
python main.py
```
Server chạy trên `http://localhost:5555`

### Kiểm Tra Server
```bash
curl http://localhost:5555/
```

### Gọi API Refresh Dữ Liệu
```bash
curl -X POST http://localhost:5555/api/inventory
```

## 📝 Xem Log

Log được lưu trong thư mục `Log/`:
- File: `log_YYYY-MM-DD.txt`
- Ví dụ: `Log/log_2026-01-14.txt`

```bash
# Xem log real-time
type Log\log_2026-01-14.txt
```