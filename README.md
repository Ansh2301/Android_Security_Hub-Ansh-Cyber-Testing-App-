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

📸 App Gallery
<details>
<summary><b>Click to view app screenshots</b></summary>

<p align="center">
<img src="https://github.com/user-attachments/assets/a5a857fa-8d75-464a-ab47-4c8058d49bcc" width="220" alt="Dashboard" />
<img src="https://github.com/user-attachments/assets/6685170e-5a96-4e91-962e-d1ab2e2de76b" width="220" alt="Permissions 1" />
<img src="https://github.com/user-attachments/assets/679a9610-4970-49b2-ade1-5c285a414663" width="220" alt="Permissions 2" />
</p>

<p align="center">
<img src="https://github.com/user-attachments/assets/954f51a2-b957-4c54-9435-972cd34c196c" width="220" alt="Network Security" />
<img src="https://github.com/user-attachments/assets/5dfc85a1-1ec3-4406-b661-483a52f1e79d" width="220" alt="Password Strength" />
<img src="https://github.com/user-attachments/assets/9491bae1-e0ab-4ce2-a417-00bd30b12162" width="220" alt="Security Tips" />
</p>

<p align="center">
<img src="https://github.com/user-attachments/assets/3893f5d7-6f74-425c-8de7-0428fabf7d1f" width="220" alt="Alternative View" />
</p>

</details>

👨‍💻 Developed by

Ansh Chaudhary — Aspiring Android Developer & Security Enthusiast
