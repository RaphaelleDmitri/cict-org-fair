# CICT Org Fair

**Live Application:** https://raphaelldmitri.github.io/cict-org-fair/

**GitHub Repository:** https://github.com/RaphaelleDmitri/cict-org-fair

A Flutter-based mobile and web application developed for the West Visayas State University College of Information and Communications Technology (CICT) Organization Fair. It allows users to view organization fair events and retrieve event information dynamically through Contentful CMS.

## Features

- **What's On:** Displays upcoming organization fair events.
- **Content Management:** Fetches event information dynamically from Contentful CMS.
- **Offline Support:** Displays previously saved event information when offline.
- **About Screen:** Displays application information and version details.
- **Cross-Platform:** Supports Android and web platforms.

## Technologies Used

- Flutter and Dart
- Contentful CMS
- GitHub Pages
- GitHub Actions
- Android SDK

## Application Information

| Detail | Value |
|---|---|
| Application Name | CICT Org Fair |
| Version | 1.1.0 |
| Build Number | 2 |
| Framework | Flutter |
| CMS | Contentful |
| Web Hosting | GitHub Pages |

## Getting Started

### Prerequisites

- Flutter SDK
- Dart SDK
- Android Studio or Visual Studio Code
- Git

### Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/RaphaelleDmitri/cict-org-fair.git
   ```

2. Navigate to the project directory:

   ```bash
   cd cict-org-fair
   ```

3. Install dependencies:

   ```bash
   flutter pub get
   ```

4. Configure the CMS credentials using the provided `cms.example.json` as a reference. Create your own `cms.json` file with the required Contentful configuration.

5. Run the application:

   ```bash
   flutter run --dart-define-from-file=cms.json
   ```

## Building the Application

### Web Release

```bash
flutter build web --release --dart-define-from-file=cms.json
```

### Android APK Release

```bash
flutter build apk --release --dart-define-from-file=cms.json
```

The generated APK can be found at:

```text
build/app/outputs/flutter-apk/app-release.apk
```

## Continuous Integration and Deployment

The project uses GitHub Actions to automate testing and deployment.

- **Continuous Integration:** Runs Flutter tests when a pull request targeting the `main` branch is created or updated.
- **Continuous Deployment:** Automatically builds and deploys the Flutter web application to GitHub Pages whenever changes are pushed to `main`.
- **Manual Deployment:** The deployment workflow can also be triggered manually through GitHub Actions.

## Security Notes

CMS configuration files, signing credentials, and keystore files are excluded from version control.

The Contentful Delivery API token used by the client application should be read-only, since credentials embedded in a Flutter web application can be accessed from its compiled files.

## Developer

**Raphaelle Dmitri Alabanzas**  
West Visayas State University  
College of Information and Communications Technology

---

*Developed as part of the CC 207B Flutter application development activities.*
