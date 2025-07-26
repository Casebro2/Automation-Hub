# Automation Hub

Automation Hub is an Android application built with Kotlin and Jetpack Compose (Material 3) designed to help non-CS Commerce students learn both no-code and code-based automations.

## Key Features

- **Onboarding**: Introduction slides explaining learning stages (Beginner → Expert).
- **Dashboard**: Quick overview of progress and next module.
- **Modules**: List of learning modules categorized by stage, with detailed lessons.
- **Lessons**: Each lesson includes video/text resources, external links, and code snippets.
- **Projects**: Hands-on tasks blending various automation tools, with completion tracking.
- **Calendar**: Schedule learning blocks with reminders.
- **Notes**: In-app note-taking per lesson, persisted locally.
- **Settings**: Theme toggle (light/dark), notifications, data export.

## Architecture & Tech Stack

- **Language**: Kotlin
- **UI Toolkit**: Jetpack Compose (Material 3)
- **Architecture**: MVVM (Model-View-ViewModel)
- **Navigation**: Navigation Compose
- **Data Persistence**: Room Database (for notes and progress tracking)
- **Data Loading**: Coil (for image loading, if any)
- **JSON Parsing**: Kotlinx Serialization
- **Target SDK**: Android 15 (SDK 33+)
- **Min API**: 23

## Build and Run Instructions

To build and run this application, you will need Android Studio installed.

1.  **Clone the repository (or download the project files):**
    ```bash
    git clone <repository_url>
    cd AutomationHub
    ```
    *(Note: Replace `<repository_url>` with the actual repository URL if this project were hosted on Git.)*

2.  **Open the project in Android Studio:**
    *   Launch Android Studio.
    *   Select `File > Open` and navigate to the `AutomationHub` directory.
    *   Click `Open`.

3.  **Sync Gradle:**
    *   Android Studio should automatically prompt you to sync the project with Gradle files. If not, click the "Sync Project with Gradle Files" button in the toolbar (looks like an elephant with a downward arrow).

4.  **Run on an emulator or device:**
    *   Select your desired emulator or connected Android device from the target device dropdown in the toolbar.
    *   Click the "Run" button (green play icon) in the toolbar.

## Customization

### Modules and Projects Data

-   **Location**: `app/src/main/assets/modules.json` and `app/src/main/assets/projects.json`
-   **Description**: These JSON files contain the static data for learning modules and hands-on projects. You can edit these files to add, remove, or modify modules, lessons, and projects.
-   **Structure**: Follow the existing JSON structure for `Module`, `Lesson`, and `Project` objects.

### UI Theme

-   **Location**: `app/src/main/java/com/automationhub/ui/theme/`
-   **Description**: This directory contains `Color.kt` and `Theme.kt` which define the Material 3 color palette and overall app theme. You can modify these files to change the app's appearance.

### Strings

-   **Location**: `app/src/main/res/values/strings.xml`
-   **Description**: All user-facing text is defined here. You can modify these strings to change labels, descriptions, and other text content.

### Onboarding Images

-   **Location**: `app/src/main/res/drawable/`
-   **Description**: The onboarding screens use simple vector drawables. You can replace `ic_onboarding_welcome.xml`, `ic_onboarding_progress.xml`, and `ic_onboarding_projects.xml` with your own vector assets or PNGs/JPGs (ensure they are appropriately sized and optimized).

### Room Database

-   **Location**: `app/src/main/java/com/automationhub/data/database/`
-   **Description**: The `AppDatabase.kt`, `dao/`, and `entity/` directories define the local persistence layer for notes and progress tracking. If you need to extend data storage, you would modify these files and potentially increment the database version.

## Code Quality

-   **Documentation**: KDoc comments are used throughout the codebase for better understanding.
-   **Single-Source-of-Truth**: Data flows from repositories, ensuring consistency.
-   **Unit Tests**: Basic unit tests are provided for ViewModels to ensure business logic correctness.

Feel free to explore and customize the application to fit your specific needs!

