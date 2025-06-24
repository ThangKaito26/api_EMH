# English Mastery Hub Backend (Node.js/Express)

## Hướng dẫn deploy lên Render (miễn phí)

1. **Tạo tài khoản [Render](https://render.com/)** (nếu chưa có).
2. **Push thư mục `api/` này lên GitHub** (tạo repo mới, chỉ cần thư mục api).
3. **Trên Render:**
   - Chọn "New Web Service" > "Connect your GitHub" > chọn repo vừa push.
   - Chọn branch (thường là `main` hoặc `master`).
   - **Environment:** Node
   - **Build Command:** `npm install`
   - **Start Command:** `npm start`
   - **Environment Variables:**
     - Thêm biến `GOOGLE_API_KEY` với giá trị là API key thật của bạn.
   - Nhấn "Create Web Service".
4. **Sau khi deploy xong**, Render sẽ cung cấp một URL dạng `https://your-app.onrender.com`.

## Chạy thử local
```bash
cd api
cp .env.example .env # sửa GOOGLE_API_KEY trong file .env
npm install
node backend.js
```

## Endpoint sử dụng
- POST `/api/generate-image` với JSON `{ "prompt": "..." }`
- Trả về kết quả giống Google API.

---
**Lưu ý:** Không commit file `.env` thật lên GitHub!
