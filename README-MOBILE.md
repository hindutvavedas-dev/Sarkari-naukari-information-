# ExamMate — Build APK using only a phone

This project includes a GitHub Actions workflow, so you can build the APK without a PC.

## Phone-only steps

1. Create/login to a GitHub account in Chrome.
2. Create a NEW **public** repository, for example `ExamMate`.
3. Upload the **contents of this ExamMateAndroid folder** (not the outer ZIP itself). Make sure `.github/workflows/build-apk.yml` is uploaded too. GitHub's web uploader may hide dot-folders; if needed, create `.github/workflows` and then create `build-apk.yml` manually by copying its contents.
4. Open the repo → **Actions** → **Build ExamMate APK** → **Run workflow**.
5. Wait for the green check.
6. Open the completed workflow run → **Artifacts** → download `ExamMate-debug-apk`.
7. Extract the downloaded artifact ZIP and install `app-debug.apk` on your phone.

## Important

The APK UI is ready, but live exam answers require a backend endpoint. In the app's Settings, set the API URL to your backend. Do NOT put private API keys inside the Android app.
