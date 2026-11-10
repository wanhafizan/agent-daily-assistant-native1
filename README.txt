AGENT DAILY ASSISTANT — NATIVE ANDROID PROJECT
Based on the Agent Daily Assistant V10 web interface.

WHAT THIS NATIVE VERSION ADDS
- Android AlarmManager schedules reminders independently of the WebView page.
- Uses exact alarms where Android grants exact-alarm access; falls back to inexact idle alarms if permission is denied.
- Alarm repeats at the selected interval (15/30/60/120/240 minutes, daily, weekly, monthly) until Complete is tapped.
- Completion cancels the native alarm.
- Schedules are stored natively and restored after device reboot or app update.
- The existing V10 interface, task fields, checklist, contacts, backup/restore and lists are retained.

IMPORTANT ANDROID LIMITS
- On Android 12+, allow "Alarms & reminders" / exact alarms for this app in system settings.
- Allow notifications for the app.
- Force Stop from Android App Info prevents alarms until the app is opened again. Normal swipe-away/closing is different, but some battery managers may still restrict background behavior.
- Android may apply Doze/battery policies. Set the app battery usage to Unrestricted for best reliability.
- Notification sound is controlled by the Android notification channel. The channel can be customized in Android notification settings. Custom audio chosen in the old web form is retained in app data but custom file playback via Android notification channels needs device-specific validation; do not rely on it until tested on the target phone.

BUILD APK
1. Install Android Studio (latest stable) on a Windows/Mac/Linux computer.
2. Open this entire folder (AgentDailyAssistantNative) in Android Studio.
3. Let Gradle sync and install the Android SDK Platform 35 if prompted.
4. Connect Android phone with USB debugging enabled, then press Run; or choose Build > Build APK(s).
5. APK output is normally app/build/outputs/apk/debug/app-debug.apk.

This environment did not have Android SDK/Gradle installed, so this package is the complete Android Studio source project, not a compiled APK. Build and test on the actual Android phone before relying on alarms.
