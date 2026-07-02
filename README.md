# SeenSound (EaRise)

A mobile app that translates **Turkish ↔ Turkish Sign Language (TİD)** using a 3D animated character.

Built for **GençBizz** (Turkish high-school entrepreneurship program). **EaRise** qualified for the **25th GençBizz Turkey National Final** and won the **Human Resources Award**.

## Features

- Text-to-sign and speech-to-sign translation
- 3D character plays sign-language animation videos
- Firebase Authentication (email/password and Google Sign-In)
- User profiles and subscription UI
- Onboarding animations and polished Material UI

## Tech Stack

| Layer | Technologies |
|-------|----------------|
| Mobile | Flutter, Dart |
| Backend | Firebase Auth, Cloud Firestore, Firebase Storage |
| Speech | `speech_to_text` |
| Media | `video_player` |
| Animations | Blender (40 sign-language words, authored in 2 weeks) |

## Screenshots

_Add Play Store / demo screenshots here._

## Getting Started

### Prerequisites

- [Flutter SDK](https://docs.flutter.dev/get-started/install) (stable channel)
- Android Studio or VS Code with Flutter extensions
- A Firebase project (if you want auth/storage to work)

### Setup

```bash
git clone https://github.com/memirusta/EaRise.git
cd EaRise
flutter pub get
```

1. Create a Firebase project at [Firebase Console](https://console.firebase.google.com).
2. Add an Android app with package name `com.gencbizz.EaRise`.
3. Download `google-services.json` and place it in `android/app/`.
4. Enable Authentication, Firestore, and Storage as needed.
5. Upload sign-language video assets to Firebase Storage (paths used in `lib/seensound/`).

```bash
flutter run
```

> **Note:** The repository may ship without a valid `google-services.json`. The original Firebase project is no longer maintained. You must use your own Firebase config to run the app.

## Project Structure

```
lib/
├── main.dart
├── introduction_animation/
└── seensound/
    ├── main_page/
    └── pages/
        ├── translate/     # Core translation flow
        ├── profile/       # Auth & account
        └── about_earise/  # About, feedback, social links
```

## Team & Context

- **Company:** EaRise (GençBizz student company)
- **Mission:** Accessibility — helping deaf and hard-of-hearing users communicate
- **Competition:** 25th GençBizz Turkey National Final
- **Award:** Human Resources Award (GençBizz)

## Contributors

| | Role |
|---|------|
| **[Furkan Baytak](https://www.linkedin.com/in/baytakfurkan/)** | Lead developer — most of the app architecture, Flutter implementation, and Firebase integration |
| **[Mehmet Emir Usta](https://www.linkedin.com/in/mehmet-emir-usta-560831256/)** | Co-founder & developer — Blender sign-language animations (40 words in 2 weeks), product direction, GençBizz |

## Developer

**Mehmet Emir Usta** · [LinkedIn](https://www.linkedin.com/in/mehmet-emir-usta-560831256/) · [GitHub](https://github.com/memirusta)

**Furkan Baytak** · [LinkedIn](https://www.linkedin.com/in/baytakfurkan/)

## License

MIT — see [LICENSE](LICENSE).  
Copyright (c) 2024 Furkan Baytak. Contributors: EaRise / GençBizz team.

## Disclaimer

This is a **portfolio / archival** release. Firebase credentials in the original build are expired or removed. Do not expect production services to work out of the box without your own backend setup.
