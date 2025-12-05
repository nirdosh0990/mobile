# LocalStore Mobile App

📱 Owner mobile app for LocalStore Platform - Flutter app for iOS & Android. Daily monitoring, menu management, and AI-powered business insights for Vietnamese restaurant owners. Offline-first with FCM push notifications.

## 📖 Specifications

This repository implements features defined in the [LocalStore Platform Specs](https://github.com/localstore-platform/specs/tree/v1.1-specs).

See [docs/SPEC_LINKS.md](docs/SPEC_LINKS.md) for detailed specification references.

## 🛠 Tech Stack

- **Framework:** Flutter 3.x + Dart 3.x
- **State Management:** Riverpod 2.4
- **Networking:** Dio + Retrofit
- **Local Storage:** Hive
- **Push Notifications:** Firebase Cloud Messaging
- **Navigation:** go_router

## 🚀 Quick Start

### Prerequisites

- Flutter 3.x ([Installation Guide](https://docs.flutter.dev/get-started/install))
- Dart 3.x
- Xcode (for iOS development)
- Android Studio (for Android development)
- CocoaPods (for iOS)

### Setup

1. **Clone the repository:**

   ```bash
   git clone https://github.com/localstore-platform/mobile.git
   cd mobile
   ```

2. **Copy environment configuration:**

   ```bash
   cp .env.example .env
   # Edit .env with your configuration
   ```

3. **Install dependencies:**

   ```bash
   flutter pub get
   ```

4. **Run code generation (if applicable):**

   ```bash
   flutter pub run build_runner build --delete-conflicting-outputs
   ```

5. **Run the app:**

   ```bash
   # Run on connected device/emulator
   flutter run

   # Run on specific platform
   flutter run -d ios
   flutter run -d android
   ```

### Development Commands

```bash
# Run tests
flutter test

# Run tests with coverage
flutter test --coverage

# Analyze code
flutter analyze

# Format code
dart format .

# Build release APK
flutter build apk --release

# Build release iOS
flutter build ios --release
```

## 📁 Project Structure

```text
lib/
├── core/               # Core utilities, constants, theme
│   ├── constants/
│   ├── router/
│   ├── theme/
│   └── utils/
├── features/           # Feature modules (Clean Architecture)
│   ├── auth/
│   ├── dashboard/
│   ├── menu/
│   └── settings/
├── l10n/              # Localization files
├── shared/            # Shared widgets and providers
│   ├── providers/
│   └── widgets/
└── main.dart
```

## 🌐 Localization

The app supports Vietnamese (vi-VN) as the primary locale with English (en-US) fallback.

- Currency: `75.000₫` (dot separator)
- Date format: `dd/MM/yyyy`
- All strings in `lib/l10n/`

## 🔗 Related Repositories

- [Specs Repository](https://github.com/localstore-platform/specs) - Technical specifications
- [API Repository](https://github.com/localstore-platform/api) - Backend API
- [Contracts Repository](https://github.com/localstore-platform/contracts) - Shared types

## 📄 License

This project is licensed under the AGPL-3.0 License - see the [LICENSE](LICENSE) file for details.
