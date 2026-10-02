# ExamMate Android

A concise competitive-exam assistant UI built with Kotlin + Jetpack Compose.

## What it does
- Exam questions in Hinglish or English
- Concise answers
- Backend integration for live web verification
- Sources displayed under answers
- No API key hard-coded in the APK

## Build
1. Open this folder in Android Studio.
2. Let Gradle sync.
3. Run on an Android 7.0+ device/emulator.
4. Build > Generate App Bundle / APK > Generate APK.

## Backend contract
Set the endpoint in Settings. It must accept:
```json
{"query":"SSC CHSL last cutoff?","language":"hinglish","concise":true}
```
and return:
```json
{"answer":"...","sources":["https://ssc.gov.in/..."]}
```

## Accuracy architecture
The backend should search official exam bodies first (SSC, UPSC, RRB, IBPS, NTA, state commissions, etc.), use dated sources, distinguish official vs tentative information, and never invent cutoff/date values. The Android app deliberately does not embed secret API keys.
