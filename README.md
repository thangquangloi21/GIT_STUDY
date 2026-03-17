# 🚀 Học git cùng Lợi

### 1. Tạo repo mới rồi push lên GitHub ví dụ project newproject
```bash
echo "# newproject" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/thangquangloi21/newproject.git
git push -u origin main
```
- echo "# newproject" >> README.md → Tạo file README.md với tiêu đề “newproject”
- git init → Khởi tạo Git trong thư mục hiện tại
- git add README.md → Thêm file vào staging
- git commit -m "first commit" → Tạo commit đầu tiên
- git branch -M main → Đổi branch mặc định thành main
- git remote add origin ... → Kết nối repo local với repo GitHub
- git push -u origin main → Push code lên GitHub


### 2. Push project có sẵn lên GitHub
```bash
git remote add origin https://github.com/thangquangloi21/newproject.git
git branch -M main
git push -u origin main
```
Dùng khi:
Bạn đã có project + đã init Git + có commit rồi.
Chỉ cần kết nối GitHub và push.

### 3. 🔧 Người mới hay bị lỗi gì?
- ❌ Lỗi: remote origin already exists
Do đã add origin trước đó
➡️ Khắc phục:
```bash
git remote remove origin
git remote add origin https://github.com/thangquangloi21/newproject.git
```

- ❌ Lỗi: rejected — non-fast-forward
Do trên GitHub có commit khác
➡️ Khắc phục:
```bash
git pull origin main --allow-unrelated-histories
git push origin main
```

- Reset về commit mới nhất và xoá toàn bộ thay đổi
```bash
git reset --hard HEAD
git pull
```

- Reset theo remote (xoá toàn bộ code local để khớp 100% với GitHub)
```bash
git fetch --all
git reset --hard origin/main
```
⚠️ Nếu bạn có thay đổi chưa add hoặc commit nhưng muốn xoá luôn:
Không cần làm gì thêm — reset hard sẽ xoá sạch.


- Để push đè lên commit trên GitHub (force push), bạn dùng lệnh:
  ```bash
git push -f origin main
```
