# 🎬 MovieScout
A high-fidelity, gesture-based movie discovery and watchlist companion application built with **Flutter & Dart**. 

MovieScout changes the way you discover movies. Instead of endlessly scrolling through lists, users can swipe through beautiful card stacks based on their mood or genre, view detailed ratings and trailers, and keep track of their personal watchlist with persistent offline capabilities and interactive analytics.

---

## 🚀 Key Features

*   **⚡ Gesture-Driven Discovery:** Discover movies using an interactive, fluid Tinder-style card swiping interface powered by `flutter_card_swiper`. Swipe right to save a movie to your watchlist, swipe left to pass.
*   **🎭 Mood & Genre Categorization:** Select and explore curated movie lists categorized by dynamic themes/genres (e.g., Nostalgic, Sci-Fi, Drama, Romance, Action).
*   **📊 Watchlist Insights:** An analytics dashboard showcasing your movie preferences with interactive, dynamic pie charts (`fl_chart`) representing genre distributions, plus summary statistics like top-watched genres.
*   **🔍 Full-Text Global Search:** Query TMDB's massive database instantly with dynamic search integration to find any movie.
*   **📱 Rich Media & Deep Linking:** Long-press any movie to pull up a sleek bottom sheet showing the movie's title, live IMDb ratings, and direct deep-links to official YouTube trailers.
*   **💾 Robust Offline Support:** Built with an offline-first architecture using `hydrated_bloc` to serialize and cache your watchlist locally, ensuring instantaneous app load times and perfect offline capability.

---

## 🛠️ Technology Stack

| Component | Technology | Description |
| :--- | :--- | :--- |
| **Framework** | **Flutter & Dart** | Cross-platform high-performance mobile UI framework |
| **State Management** | **Flutter BLoC & Cubit** | Reactive state container for separation of concerns |
| **Local Persistence** | **Hydrated BLoC & Path Provider** | Automatically caches state to local disk asynchronously |
| **Networking** | **Dio** | Robust HTTP client with advanced query parameters and API requests |
| **Data Source** | **TMDB API** | Real-time international movie metadata, images, and trailers |
| **Data Visualization**| **fl_chart** | Rich interactive graphs and statistics |
| **Gestures & UI** | **flutter_card_swiper** | Fluid swiping deck experience |

---

## 📁 Clean Architecture & File Structure

The project follows a clean, modular folder structure designed for scalability and maintainability:

```text
lib/
├── core/            # App constants, global helper functions & theme colors
├── cubits/          # Business logic layers (MovieCubit, WatchlistCubit)
├── models/          # Data schemas and models (GenreData, etc.)
├── navigation/      # Navigation wrapper and responsive bottom navbar
├── screens/         # Feature-specific page UI
│   ├── discovery/       # Swipe-to-discover card screen
│   ├── genre_selection/ # Landing genre selection and search page
│   ├── stats/           # Watchlist insights and fl_chart visualizations
│   └── watchlist/       # Persistent user saved watchlist
├── widgets/         # Custom, reusable presentation components (Movie Tiles, Pie Charts, Stat Cards)
├── app.dart         # Material Application routing and configuration
└── main.dart        # Hydrated storage initialization and App entry point
```

---

## ⚙️ Getting Started & Installation

### Prerequisites
*   [Flutter SDK](https://docs.flutter.dev/get-started/install) (v3.10.4 or higher recommended)
*   Dart SDK (v3.0.0 or higher)
*   A TMDB (The Movie Database) API Key. You can get one for free [here](https://developers.themoviedb.org/).

### Setup Instructions

1.  **Clone the Repository:**
    ```bash
    git clone https://github.com/Abdallahamrr/MovieScout.git
    cd MovieScout
    ```

2.  **Environment Variables:**
    Create a `.env` file in the root directory of the project:
    ```env
    TMDB_API_KEY=your_actual_tmdb_api_key_here
    ```

3.  **Install Dependencies:**
    ```bash
    flutter pub get
    ```

4.  **Run the Application:**
    Ensure you have an emulator running or a physical device connected:
    ```bash
    flutter run
    ```

---

## 📸 Screenshots & Showcase

Below is an overview of the visual experience inside **MovieScout**:

<p align="center">
  <img src="flutter_01.png" alt="MovieScout Interface Showcase" width="360" style="border-radius: 20px; box-shadow: 0 4px 30px rgba(229, 9, 20, 0.35);"/>
</p>

---

## 🤝 Contributing

Contributions make the open-source community an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📄 License

Distributed under the MIT License. See `LICENSE` for more information.
