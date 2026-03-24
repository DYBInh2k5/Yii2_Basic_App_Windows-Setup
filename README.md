# Yii2 Basic App (Windows Setup)

Du an duoc tao tu Yii2 Basic template va da duoc chinh lai de chay on tren may Windows hien tai.

## 1) Moi truong

- PHP: 8.3.x
- Composer: 2.8.x
- OS: Windows

Luu y quan trong:
- May hien tai thieu extension PHP `ext-curl`.
- Vi vay project da duoc cai theo cach bo qua dependency dev.

## 2) Tao project

Lenh da dung:

```powershell
composer create-project --prefer-dist --no-dev --ignore-platform-req=ext-curl yiisoft/yii2-app-basic yii-basic
```

## 3) Chay project

Tai thu muc project, chay:

```powershell
php yii serve --port=8081
```

Mo trinh duyet:

- http://localhost:8081

## 4) Cap nhat cau hinh dev module

Do cai dat khong co goi dev, cac module `debug` va `gii` co the khong ton tai.

Da cap nhat:
- [config/web.php](config/web.php)
- [config/console.php](config/console.php)

Theo huong:
- Chi bootstrap `debug` neu `class_exists('yii\\debug\\Module')`
- Chi bootstrap `gii` neu `class_exists('yii\\gii\\Module')`

## 5) Cau truc thu muc chinh

- assets
- commands
- config
- controllers
- models
- runtime
- vendor
- views
- web

## 6) Day len GitHub

Neu da co repository tren GitHub, chay:

```powershell
git init
git add .
git commit -m "chore: init yii2 basic project"
git branch -M main
git remote add origin <GITHUB_REPO_URL>
git push -u origin main
```

Neu da co `origin`, bo qua lenh add remote va push truc tiep.

## 7) Tai lieu lien quan

- [IMPLEMENTATION_LOG.md](IMPLEMENTATION_LOG.md)
