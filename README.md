# 💰 Crypto Bazaar

A Flutter-based cryptocurrency market application that displays real-time cryptocurrency prices through API integration.

Crypto Bazaar is a simple and practical mobile application built with **Flutter** and **Dart**, designed to provide users with an easy way to view cryptocurrency market information.

---

## 📱 Features

* 📊 Display cryptocurrency prices
* 🔄 Fetch cryptocurrency data from an API
* 🌐 HTTP/API communication
* ⏳ Loading indicators while fetching data
* 📱 Mobile-friendly user interface
* 🎨 Custom application assets and fonts

---

## 🛠️ Technologies

| Technology          | Usage                                  |
| ------------------- | -------------------------------------- |
| **Flutter**         | Cross-platform application development |
| **Dart**            | Programming language                   |
| **HTTP**            | API requests                           |
| **Dio**             | HTTP client and network communication  |
| **Flutter Spinkit** | Loading animations                     |
| **Material Design** | UI components                          |

---

## 🏗️ Project Structure

```text
crypto-bazzar/
│
├── android/          # Android-specific files
├── ios/              # iOS-specific files
├── linux/            # Linux-specific files
├── macos/            # macOS-specific files
├── web/              # Web-specific files
├── windows/          # Windows-specific files
│
├── assets/
│   └── images/       # Application images
│
├── fonts/            # Custom fonts
│
├── lib/              # Main Flutter source code
│
├── test/             # Tests
│
├── pubspec.yaml      # Project dependencies and configuration
└── README.md
```

---

## 🚀 Getting Started

### Prerequisites

Make sure you have the following installed:

* [Flutter SDK](https://flutter.dev/)
* [Dart SDK](https://dart.dev/)
* Android Studio or another Flutter-compatible IDE
* An Android emulator or physical Android device

### Installation

1. Clone the repository:

```bash
git clone https://github.com/mohammad-re2004/crypto-bazzar.git
```

2. Navigate to the project directory:

```bash
cd crypto-bazzar
```

3. Install the dependencies:

```bash
flutter pub get
```

4. Run the application:

```bash
flutter run
```

---

## 🌐 API & Networking

The application communicates with external APIs to retrieve cryptocurrency market information.

Network communication is implemented using Flutter HTTP clients such as:

* `http`
* `dio`

The project therefore demonstrates the basic implementation of **REST API communication in Flutter**, including sending requests and processing API responses.
