# Crash Reporting Dashboard – Flutter App

A lightweight Flutter plugin for capturing crash reports and application logs and sending them to popular platforms like **Webhook**, **Telegram**, **Slack**, or **Discord**.

[Step-by-Step Guide to Build Real-Time Crash Reporting in Flutter.](https://www.sevensquaretech.com/flutter-crash-reporting-dashboard-with-github-code/)

---

## 🚀 Features

- Capture uncaught Flutter & Dart exceptions
- Send crash reports in real-time
- Supports multiple delivery platforms:
  - Webhook
  - Telegram
  - Slack
  - Discord
- Lightweight and easy to integrate
- Stores basic crash data locally using SharedPreferences

---

## 📦 Package Information

- **Name:** crash-reporting-dashboard-flutter-app
- **Version:** 1.0.0
- **SDK:** Flutter >= 1.17.0, Dart >= 2.17.0 < 4.0.0
- **Homepage:** https://github.com/SevenSquare-Tech/crash-reporting-dashboard-flutter-app

---

## 🔧 Installation

Add the dependency to your `pubspec.yaml` file:

```yaml
dependencies:
  crash_reporting_dashboard_flutter_app: ^1.0.0
```

Then run:

```bash
flutter pub get
```

---

## 🛠️ Usage

### 1. Initialize Crash Reporting

Call the initializer at the start of your application:

```dart
void main() {
  FlutterError.onError = (FlutterErrorDetails details) {
    // Send error to crash reporting service
  };

  runApp(MyApp());
}
```

### 2. Send Logs or Exceptions

```dart
try {
  // risky code
} catch (e, stackTrace) {
  // send error report
}
```

---

## 🔔 Supported Platforms

| Platform | Supported |
| -------- | --------- |
| Webhook  | ✅        |
| Telegram | ✅        |
| Slack    | ✅        |
| Discord  | ✅        |

---

## 🧪 Testing

Run unit tests using:

```bash
flutter test
```

Mocking is supported via the `mockito` package.

---

## 📁 Dependencies Used

- flutter
- shared_preferences
- http (dev dependency)
- mockito
- flutter_lints
