# 🎬 Android Movie App - MyMovie

Android Movie App is a native Android application developed in Java.  
The app displays a list of popular movies, allows users to search movies, view movie details, watch trailers, and see cinema location information using Google Maps.

## 📱 Features

- Display popular movies from TMDB API
- Search movies by title
- Show movie details:
  - Movie title
  - Overview / description
  - Poster image
- Watch movie trailers using YouTube embedded video
- Display cinema location on Google Maps
- Get user current location permission
- Clean movie list using RecyclerView and CardView

## 🛠️ Technologies Used

- Java
- Android Studio
- XML Layouts
- RecyclerView
- CardView
- Volley
- Glide
- Google Maps SDK
- Google Play Services Location
- WebView
- TMDB API

## 📂 Project Structure

```text
Android_Movie_App/
│
├── app/
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/com/example/mymovie/
│   │   │   │   ├── MainActivity.java
│   │   │   │   ├── MovieDetailActivity.java
│   │   │   │   ├── MyMovieAdapter.java
│   │   │   │   ├── MyMovieData.java
│   │   │   │   ├── VideoPlayer.java
│   │   │   │   └── movie_item_list.java
│   │   │   │
│   │   │   ├── res/
│   │   │   └── AndroidManifest.xml
│   │
│   └── build.gradle.kts
│
├── build.gradle.kts
├── settings.gradle.kts
├── gradlew
└── gradlew.bat
```

## ⚙️ Requirements

Before running the project, make sure you have:

- Android Studio installed
- Java 11
- Android SDK installed
- Internet connection
- TMDB API key
- Google Maps API key

## 🚀 How to Run the Project

### 1. Clone the repository

```bash
git clone https://github.com/Marouanemounir/Android_Movie_App.git
```

### 2. Open the project

Open the project in **Android Studio**.

### 3. Sync Gradle

Wait until Android Studio finishes Gradle synchronization.

### 4. Add your API keys

This project uses two external services:

- TMDB API
- Google Maps API

For security reasons, do not hardcode API keys directly in Java files or in `AndroidManifest.xml`.

Recommended approach:

Create or edit the `local.properties` file:

```properties
TMDB_API_KEY=your_tmdb_api_key_here
MAPS_API_KEY=your_google_maps_api_key_here
```

### 5. Run the app

Run the application on an Android emulator or a physical Android device.

## 🔐 API Keys

### TMDB API

Used to fetch popular movies, movie details, posters, and trailers.

You can get your API key from:

```text
https://www.themoviedb.org/
```

### Google Maps API

Used to display cinema location and user location.

You can get your API key from:

```text
https://console.cloud.google.com/
```

## 🧩 Main Screens

### Home Screen

Displays a list of popular movies using RecyclerView.

### Search Feature

Allows users to filter movies by typing in the search field.

### Movie Details Screen

Shows detailed information about the selected movie, including:

- Title
- Description
- Poster image
- Trailer button
- Map location

### Video Player Screen

Plays the selected movie trailer using an embedded YouTube video inside a WebView.

## 📦 Main Dependencies

```kotlin
implementation("androidx.recyclerview:recyclerview:1.3.2")
implementation("androidx.cardview:cardview:1.0.0")
implementation("com.android.volley:volley:1.2.1")
implementation("com.github.bumptech.glide:glide:4.16.0")
annotationProcessor("com.github.bumptech.glide:compiler:4.16.0")
implementation("com.google.android.gms:play-services-maps:18.2.0")
implementation("com.google.android.gms:play-services-location:21.0.1")
implementation("com.google.android.exoplayer:exoplayer-core:2.19.1")
```

## 📌 Permissions Used

The app requires the following permissions:

```xml
<uses-permission android:name="android.permission.INTERNET" />
<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />
<uses-permission android:name="android.permission.ACCESS_FINE_LOCATION" />
<uses-permission android:name="android.permission.ACCESS_COARSE_LOCATION" />
```

These permissions are used for API requests, internet access, and location/map features.

## 🧠 What I Learned

Through this project, I practiced:

- Building a native Android application using Java
- Consuming REST APIs with Volley
- Parsing JSON data
- Displaying dynamic data with RecyclerView
- Loading images from URLs using Glide
- Passing data between Android activities
- Integrating Google Maps in Android
- Handling runtime permissions
- Playing online video content using WebView

## 📸 Screenshots

```markdown
![Home Screen](screenshots/home.png)
![Movie Details](screenshots/details.png)
![Video Player](screenshots/video.png)
```

## 🚧 Future Improvements

- Add user authentication
- Add favorite movies feature
- Improve UI/UX design
- Add movie categories
- Add offline caching
- Add dark mode
- Add better error handling
- Hide API keys using a safer configuration

## 👨‍💻 Author

**Marouane Mounir**

- GitHub: [Marouanemounir](https://github.com/Marouanemounir)

## 📄 License

This project is for educational purposes.
