# Ai vui hơn học sinh THCS

Ứng dụng giao việc, chat, theo dõi tự học cho phụ huynh và học sinh THCS. Web tĩnh (HTML/JS) + Supabase + Vercel.

## 1. Supabase
1. Tạo project tại supabase.com.
2. **SQL Editor** > New query > dán toàn bộ `supabase/schema.sql` > Run.
3. **Authentication > Providers > Email**: tắt **Confirm email** (app dùng tên đăng nhập, email giả dạng `ten@avh-hocsinh.app`).
4. **Project Settings > API**: copy `Project URL` và `anon public key`, dán vào `config.js`.

## 2. GitHub
```bash
git init && git add . && git commit -m "init"
git branch -M main
git remote add origin https://github.com/<ban>/<repo>.git
git push -u origin main
```

## 3. Vercel
Add New Project > import repo GitHub > Framework Preset: **Other** > Deploy (không cần build command).
Mỗi lần `git push`, Vercel tự deploy lại.

## Phân quyền
- Phụ huynh đăng ký → tạo nhà với mã riêng (đổi được trong Hồ sơ).
- Học sinh đăng ký bằng mã nhà → chỉ vào đúng nhà đó.
- Việc, chat, hồ sơ chỉ xem được trong cùng nhà (Row Level Security trong database, không chỉ ở giao diện).
- Phụ huynh chỉ giao việc cho học sinh trong nhà mình; học sinh chỉ tự giao cho mình và chỉ tick xong việc của mình.
