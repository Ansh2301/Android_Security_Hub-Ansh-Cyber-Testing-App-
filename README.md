🛡️Android_Security_Hub (Ansh-Cyber-Testing-App)

📖 Overview

This project is a comprehensive Android Cybersecurity Assistant designed to empower users with real-time device security insights. Developed as part of the internship assignment, the app focuses on four critical pillars: App Privacy, Network Integrity, Credential Strength, and Security Literacy.

🚀 Key Features

1\. 🔍 App Permission Scanner

Audits all installed applications to identify potential privacy risks.

  * echnical Implementation: Leverages the `Android PackageManager API` to query application metadata.
  * Insight: Provides a transparent count of "Sensitive Permissions" (Camera, Location, Microphone) to help users identify over-privileged apps.

2\. 🌐 Network Security Check

Analyzes the current data connection to prevent data leakage on insecure networks.

  * Technical Implementation: Utilizes `ConnectivityManager` and `NetworkCapabilities`.
  * Data Points: Displays Network Type (Wi-Fi/Mobile), Connection Status, and Device IP Address.

3\. 🔑 Password Strength Checker

An interactive tool that evaluates user passwords against common entropy standards.

  * Visual Feedback: Uses a dynamic color-coded system (Red/Yellow/Green) to categorize passwords as **Weak**, **Medium**, or **Strong**.
  * Logic: Implemented custom heuristic analysis to check for length, character diversity, and complexity.

4\. 💡 Security Tips Dashboard

A curated educational hub featuring industry-standard best practices.

  * Topics: 2FA (Two-Factor Authentication), Public Wi-Fi risks, and App Update hygiene.

🛠️ Technology Stack & "The Why"

  * Kotlin & Jetpack Compose: Chosen for a fully declarative UI approach. Compose allowed for rapid iteration of the Material 3 design and seamless state management for real-time network updates.
  * Material Design 3 (M3): Used to ensure the app feels modern and "native" to the latest Android 14 environments.
  * ConnectivityManager API: Selected over older deprecated libraries to ensure the app remains performant and future-proof on modern SDKs.

🏗️ Architecture

The app follows the MVVM (Model-View-ViewModel) pattern:

  * UI (Compose): Observes state and handles user interaction.
  * ViewModels: Manages the logic for permission scanning and password validation.
  * Utils (Repository Layer): Interacts with Android System Services (Network/Package Manager).

🧠 Technical Challenges & Solutions

The "Unresolved Reference" Bug

  * Problem: During development, the compiler intermittently failed to recognize `NETWORK_CAPABILITY_INTERNET` despite correct imports, likely due to a conflict between the Compose Compiler and older SDK references.
  * Solution: I implemented a low-level integer mapping (Capability 12). This bypassed the high-level API "ghost" error and ensured the build was stable across all environments without sacrificing functionality. This demonstrated a deep-dive approach into how Android handles system constants.

UI State Synchronization

  * Problem: Updating the network status in real-time without draining the battery.
  * Solution: Used `LaunchedEffect(Unit)` to trigger a single high-accuracy check upon screen entry, reducing unnecessary background polling.

⚙️ How to Run
1.  Clone: `https://github.com/Ansh2301/Android_Security_Hub-Ansh-Cyber-Testing-App-`
2.  Sync: Open in Android Studio and Sync Gradle.
3.  Deploy: Run on an emulator or physical device (API 24+).
4.  APK: A pre-compiled debug APK is available in the [Releases] (https://github.com/Ansh2301/Android_Security_Hub-Ansh-Cyber-Testing-App-) section.

📸 App Screenshots

<p align="center">
  <img src="https://github.com/user-attachments/assets/86c82ff1-d8a5-4e57-9689-b2c04bd1169" width="180" alt="Dashboard" />
  <img src="https://github.com/user-attachments/assets/080b2953-175f-4419-8d09-9965d1c2c2c4" width="180" alt="Permissions 2" />
  <img src="https://github.com/user-attachments/assets/a03dd36e-689c-4146-97e4-24c55f0e0c9e" width="180" alt="Network Status" />
</p>

<p align="center">
  <img src="https://github.com/user-attachments/assets/1de54aa7-0d2f-4590-a5c5-4c2cbfccd595" width="180" alt="Password Checker 1" />
  <img src="https://github.com/user-attachments/assets/323fb427-0562-4298-9f73-75fd97555188" width="180" alt="Password Checker 2" />
  <img src="https://github.com/user-attachments/assets/4e0e77eb-ed5e-456b-8a7e-b7d47c0cb06f" width="180" alt="Security Tips" />
</p>

👨‍💻 Developed by

Ansh Chaudhary — Aspiring Android Developer & Security Enthusiast
