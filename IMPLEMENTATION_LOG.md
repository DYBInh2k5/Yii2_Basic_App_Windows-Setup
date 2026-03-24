# Yii Project Setup Log

## Overview
- Created a new Yii2 Basic project in this folder.
- Environment: PHP 8.3 and Composer 2.8 on Windows.

## Commands Used
- `composer create-project --prefer-dist --no-dev --ignore-platform-req=ext-curl yiisoft/yii2-app-basic yii-basic`

## Notes
- This machine is missing PHP extension `ext-curl`.
- Project was installed with `--no-dev` and ignored `ext-curl` for dependency resolution.
- In development config, module loading for `debug` and `gii` was guarded with `class_exists(...)` so the app can run without dev packages.

## Run The App
From this folder, run:

```powershell
php yii serve --port=8081
```

Open:
- http://localhost:8081

## Current Status
- App reachable at http://localhost:8081 with HTTP 200.

## Markdown Tracking Updates
- README replaced from default template to project-specific setup guide.
- Added clear run instructions and GitHub push flow.
- Documented reason for no-dev install (`ext-curl` missing in current PHP setup).
- Updated README to full Vietnamese with accents.
- Added CHANGELOG.md for release tracking.
- Added GitHub Actions CI workflow for PHP syntax validation.
- Added CI badge to README.
- Added RELEASE_NOTES.md template.
- Added conditional PHPUnit workflow for GitHub Actions.

## GitHub Publish Checklist
- [x] Update Markdown docs
- [x] Initialize git repository
- [x] Create first commit
- [x] Add remote origin
- [x] Push branch `main` to GitHub
