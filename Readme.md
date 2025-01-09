# README: Rebuilding and Running the Decompiled Android Game

This document explains the steps I followed to decompile an Android APK, rebuild it in Android Studio, and run the game successfully. By the end, I was able to play and understand the game's logic.

---

## Steps:

### 1. Decompiling the APK
I used [http://www.javadecompilers.com/apk](http://www.javadecompilers.com/apk) to decompile the APK file. This tool provided me with a folder containing the `sources` and `resources` directories.

### 2. Setting Up the Project in Android Studio
I opened a new project in Android Studio and copied both activities from the following location in the decompiled files:
```
\sources\com\classy\survivegame
```
These activities included the game's core logic.

### 3. Adding the Manifest File
I added the `AndroidManifest.xml` file from the following location:
```
\resources
```
This ensured the project had the necessary configurations.

### 4. Adding Themes
I added the themes for both day and night modes from these locations:
```
\resources\res\values-night
\resources\res\values
```
I integrated these themes into the project to ensure proper UI styling.

### 5. Adding Layouts
I added the required layout files from the following location:
```
\resources\res\layout
```
These files defined the game's user interface.

### 6. Adding Drawables and URL String
I:
- Added the drawable resources from:
  ```
  \resources\res\drawable
  ```
- Retrieved the URL string from:
  ```
  \resources\res\values
  ```
- Placed the URL string into the `strings.xml` file in the Android Studio project.
- Removed the invisible character present in the string.

### 7. Running the Game and Understanding the Logic
After setting up the project, I ran the game and explored its logic. The game generates a sequence based on the provided ID. By entering the correct sequence of arrow clicks, I was able to complete the game with the result:
```
Survived in Illinois.
```

---

## Conclusion
By following these steps, I successfully decompiled, rebuilt, and understood the logic of the Android game. This process allowed me to dive deeper into the game's mechanics and reconstruct it in Android Studio.

