# Yii2 Basic App (Windows Setup)

[![CI](https://github.com/DYBInh2k5/Yii2_Basic_App_Windows-Setup/actions/workflows/ci.yml/badge.svg)](https://github.com/DYBInh2k5/Yii2_Basic_App_Windows-Setup/actions/workflows/ci.yml)

Dự án được tạo từ Yii2 Basic template và đã được chỉnh lại để chạy ổn định trên Windows.

## 1) Môi trường

- PHP: 8.3.x
- Composer: 2.8.x
- OS: Windows

Lưu ý quan trọng:
- Máy hiện tại thiếu extension PHP ext-curl.
- Vì vậy dự án được cài theo cách bỏ dependency dev.

## 2) Tạo project

Lệnh đã dùng:

```powershell
composer create-project --prefer-dist --no-dev --ignore-platform-req=ext-curl yiisoft/yii2-app-basic yii-basic
```

## 3) Chạy project

Tại thư mục project, chạy:

```powershell
php yii serve --port=8081
```

Mở trình duyệt:

- http://localhost:8081

## 4) Cập nhật cấu hình dev module

Do cài đặt không có gói dev, các module debug và gii có thể không tồn tại.

Đã cập nhật:
- [config/web.php](config/web.php)
- [config/console.php](config/console.php)

Theo hướng:
- Chỉ bootstrap debug nếu class_exists('yii\\debug\\Module').
- Chỉ bootstrap gii nếu class_exists('yii\\gii\\Module').

## 5) Cấu trúc thư mục chính

- assets
- commands
- config
- controllers
- models
- runtime
- vendor
- views
- web

## 6) Đưa lên GitHub

Nếu đã có repository trên GitHub, chạy:

```powershell
git init
git add .
git commit -m "chore: init yii2 basic project"
git branch -M main
git remote add origin <GITHUB_REPO_URL>
git push -u origin main
```

Nếu đã có origin, bỏ qua lệnh add remote và push trực tiếp.

## 7) Tài liệu liên quan

- [IMPLEMENTATION_LOG.md](IMPLEMENTATION_LOG.md)
- [CHANGELOG.md](CHANGELOG.md)
- [RELEASE_NOTES.md](RELEASE_NOTES.md)
