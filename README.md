# Android_Security_Hub-Ansh-Cyber-Testing-App-

A modern, lightweight Android security utility built to provide users with real-time insights into their device's network safety and application privacy. This app serves as a centralized dashboard for auditing system permissions and monitoring connectivity.

🚀 Features

  * **Real-time Network Audit**: Detects the current connection type (Wi-Fi, Cellular, or Ethernet) and verifies actual internet reachability using low-level `NetworkCapabilities`.
  * **Permission Scanner**: Automatically scans all installed applications to provide a total count of potential privacy touchpoints.
  * **Modern UI/UX**: Built entirely with **Jetpack Compose** following Material Design 3 guidelines for a clean, responsive experience.
  * **Safety First**: Designed with a "Zero-Permission" philosophy for the core app itself—it audits others without compromising your own data.

🛠️ Tech Stack

  * Language: Kotlin
  * UI Framework: Jetpack Compose (Material 3)
  * Architecture: MVVM (Model-View-ViewModel) pattern
  * Build System: Gradle Kotlin DSL (`.kts`)
  * Minimum SDK: API 24 (Android 7.0+)
  * Target SDK: API 34 (Android 14)

📸 Screenshots

| Dashboard | App Scanner | Security Tips |
| :--- | :--- | :--- |
|  |  |  |


🏗️ Project Structure

com.cybersecurity.app
├── ui
│   ├── theme       # Material 3 Color Schemes & Typography
│   ├── screens     # Dashboard, Scanner, and Tips Composable screens
│   └── navigation  # Compose Navigation graph
└── utils
    ├── NetworkUtils    # Logic for connectivity and capability checks
    └── PermissionUtils # Logic for app scanning and permission auditing

⚙️ Installation & Setup

1.  Clone the repository:
    ```bash
    git clone https://github.com/YOUR_USERNAME/AnshCybersecurityApp.git
    ```
2.  Open in Android Studio:
    File \> Open \> Select the project folder.
3.  Sync Gradle:
    Click the "Elephant" icon to sync the `build.gradle.kts` files.
4.  Run:
    Select your device/emulator and press the green **Run** button.

🛡️ License
Distributed under the MIT License. See `LICENSE` for more information.

How to use this:

1.  In Android Studio, right-click your **root project folder** (the very top one).
2.  Select **New \> File** and name it `README.md`.
3.  Paste the code above into that file and save it.
4.  When you push to GitHub, this will automatically appear as your "Home Page."
