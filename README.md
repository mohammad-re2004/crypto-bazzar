# Crypto Bazaar

A Flutter cryptocurrency market app that shows live asset prices, 24h change, and a fast coin search.

<p align="center">
  <img src="assets/images/logo.png" alt="Crypto Bazaar logo" width="160" />
</p>

## About

Crypto Bazaar loads a list of digital assets from the public [CoinCap](https://coincap.io) API and displays them in a dark Material UI.

The first screen is a splash view with the app logo and a loading animation. After the request succeeds, the app opens the market list.

## Features

- Rank, name, symbol, and USD price for each asset
- 24h change with green / red color and trend icons
- Live search by coin name
- Pull-to-refresh (`RefreshIndicator`)
- Splash screen with `flutter_spinkit`
- Custom font (`mr` / `fonts/mh.ttf`)
- Shared dark color palette in `lib/data/constant/constants.dart`

## Tech stack

| Tool | Role |
| --- | --- |
| Flutter / Dart | UI and app logic |
| Dio | HTTP client for CoinCap |
| flutter_spinkit | Loading animation |
| Material Design | UI components |

## Project structure

```
crypto-bazzar/
├── lib/
│   ├── main.dart
│   ├── data/
│   │   ├── constant/constants.dart   # colors
│   │   └── model/crypto.dart         # asset model
│   └── screens/
│       ├── home_screen.dart          # splash + first fetch
│       └── coin_list_screen.dart     # list, search, refresh
├── assets/images/
├── fonts/
├── android/ ios/ web/ linux/ macos/ windows/
└── pubspec.yaml
```

## Prerequisites

- [Flutter SDK](https://docs.flutter.dev/get-started/install) (project SDK: `>=2.17.0 <3.0.0`)
- Android Studio, VS Code, or another Flutter-ready IDE
- An emulator or a physical device

## Getting started

```bash
git clone https://github.com/mohammad-re2004/crypto-bazzar.git
cd crypto-bazzar
flutter pub get
flutter run
```

Web:

```bash
flutter run -d chrome
```

## API

Market data comes from CoinCap:

- Initial load in `home_screen.dart` uses `rest.coincap.io/v3/assets`
- Refresh and empty-search reload in `coin_list_screen.dart` use `api.coincap.io/v2/assets`

`Crypto.fromMapJson` maps fields such as `rank`, `name`, `symbol`, `priceUsd`, and `changePercent24Hr`.

> Do not commit API keys. Read them from environment variables or a gitignored local file.

## Screenshots

Add captures under `screenshots/` and link them here:

```
screenshots/
├── splash.png
└── market.png
```

## Roadmap

- Coin detail page
- Price charts and history
- Favorites
- Periodic auto-refresh
- Offline cache
- Stronger network error handling
- Unit and widget tests
- Split the API layer from the UI
- Move `flutter_spinkit` from `dev_dependencies` to `dependencies` in `pubspec.yaml`

## Author

**Mohammadreza Ebadi**  
Flutter & mobile developer  
GitHub: [@mohammad-re2004](https://github.com/mohammad-re2004)

## License

Available for educational and personal use.
