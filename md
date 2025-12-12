# CineVault Admin

CineVault Admin is a lightweight mobile application designed for theater operators to quickly update movie assignments and show information directly from an Android device.  
The app connects securely to the CineVault backend APIs and supports fast searching, theater selection, and authenticated updates.

---

## Features

### Movie Management
- Search movies by title (real-time API search)
- Select a movie to assign to a theater

### Theater Management
- Search theaters by name
- View theater details and update show allocations

### Secure Authentication
- Admin login required for every update
- Credentials are stored securely using encrypted storage (AES-256)

### Quality-of-Life Enhancements
- Automatically remembers:
  - User ID
  - Password
  - Last selected theater
- One-tap update for repeated daily show changes
- Simple and clean UI for fast usage by theater owners

---

## Tech Stack

- Android (Kotlin)
- Jetpack Compose (Material3)
- Retrofit + OkHttp
- EncryptedSharedPreferences (AES-256)
- MVVM-lite pattern (Composable UI + state)

---

## Requirements

- Android 7.0 (API 24) or higher
- Internet connection required
- Valid CineVault admin credentials

---

## Installation

This app is distributed via Google Play.  
Download the latest version from the Play Store once published.

To install manually:

1. Clone the repository  
2. Open in Android Studio  
3. Generate a signed app bundle  
4. Install on device or upload to Play Console

---

## API Endpoints Used

### Search Movies
```

GET /movies/search?q=<query>

```

### Search Theaters
```

GET /theaters/search?q=<query>

```

### Update Show
```

POST /theaters/update

````

#### Example Request Payload
```json
{
  "movie_id": "0bd86866-cc04-4449-8be5-bb6ed4cf6553",
  "user_id": "admin@cinevault.live",
  "pswd": "YourPassword",
  "theater_id": "ce462499-48d1-4a3c-b812-04da4b970224"
}
````

---

## Privacy Policy

CineVault Admin respects your privacy and ensures the protection of all data processed through the app.

### Information We Collect

* User ID (email)
* Admin password
* Selected theater ID

This information is:

* Sent securely to the CineVault server only for authentication and show updates
* Never shared with any third parties
* Stored locally using **AES-256 encrypted storage**

### How We Use Your Data

* Authenticate you as a CineVault theater administrator
* Allow you to update show details in your theater
* Improve convenience by remembering your last used credentials and theater

### Data Storage

* Credentials saved locally are encrypted using `EncryptedSharedPreferences`
* No sensitive information is stored in plain text
* You may clear this data manually by reinstalling the app or using “Clear App Data”

### Third-Party Access

CineVault Admin does **not** share, sell, or disclose your data to any third parties.

### Network & Transmission

All communication with CineVault servers occurs over **HTTPS**.
No data is transmitted without encryption.

### Contact

For privacy inquiries:
[support@cinevault.live](mailto:support@cinevault.live)

---

## Google Play Data Safety Summary

### Data Collected

| Data Type  | Usage                        |
| ---------- | ---------------------------- |
| User ID    | Authentication               |
| Password   | Authentication               |
| Theater ID | Assigning movie to a theater |

### Data Shared

None

### Data Encryption

All data is encrypted in transit (HTTPS) and at rest (AES-256 encrypted storage).

### Data Deletion

Users may delete data by:

* Logging out (future feature)
* Clearing app data manually
* Reinstalling the application

---

## License

This project is proprietary and maintained by CineVault.
Unauthorized distribution or modification is not permitted.

---

## Support

For issues or feature requests:
[support@cinevault.live](mailto:support@cinevault.live)
