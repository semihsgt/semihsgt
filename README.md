<h1 align="center">Hey there, I'm Semih 👋</h1>

<p align="center">
  <b>Junior iOS Developer</b> · Kocaeli, Türkiye (UTC+3)
</p>

I build iOS apps end-to-end in SwiftUI with Swift 6 strict concurrency, MVVM and protocol-oriented service layers. I care about readable code, structure that survives a second feature, and shipping something that actually works on a real device. Currently preparing my first app for App Store release.

- 🔭 **Latest build:** [Movie Mind](https://github.com/semihsgt/MovieMindApp_SwiftUI) — AI-powered discovery for movies, TV shows and people, with every suggestion grounded in real TMDB data.
- 🎓 **Associate Degree in Computer Programming** — Kocaeli University (2024 – 2026)
- 📜 **Courses:** [Portfolio Project](https://seanallen.teachable.com/p/portfolio-project) (Sean Allen) · SwiftUI ile iOS Mobil Geliştirme (BTK Akademi)
- 🌍 **Languages:** Turkish (native) · English (B2, EF SET certified)
- 📫 **Reach me:** [LinkedIn](https://www.linkedin.com/in/semihsogut/) · semihsogut.dev@gmail.com

<img width="4500" height="2531" alt="readme_png copy" src="https://github.com/user-attachments/assets/a0f0fbac-bc92-4a42-bd21-92f03615bd6c" />

---

## 📱 Projects

### 🎬 [Movie Mind](https://github.com/semihsgt/MovieMindApp_SwiftUI)

<sub>`SwiftUI` · `Swift 6` · `SwiftData` · `Gemini API` · `TMDB API` · `Swift Testing` · `DocC`</sub>

An AI-powered app for discovering movies, TV shows and people. Gemini proposes titles; TMDB decides what is real.

- **AI that can't hallucinate.** Gemini returns titles under a JSON `responseSchema`, each resolved against TMDB search and year-matched, so no invented IDs, posters or ratings ever reach the UI.
- **`@Fallback` property wrapper.** TMDB omits fields freely. A custom wrapper plus a `KeyedDecodingContainer.decode` overload absorbs missing, null and mistyped values — 60 of 107 decoded properties stay non-optional and the views stopped unwrapping.
- **Actors and narrow protocols.** MVVM over an `actor NetworkManager` and per-use-case protocols, with a generic `ViewState<T>` enum that makes conflicting loading and error states unrepresentable.
- Value-based navigation with zoom transitions, image prefetching and disk caching, an offline SwiftData library, pagination, debounced search, VoiceOver, DocC documentation and Swift Testing unit tests.

### 🌤 [Atlas Weather](https://github.com/semihsgt/AtlasWeatherApp_SwiftUI)

<sub>`SwiftUI` · `Swift 6` · `MVVM` · `CoreLocation` · `MapKit` · `OpenWeatherMap` · `EN/TR localization`</sub>

A native weather app where every location also opens onto the country behind it: facts, photos, the capital on a map.

- **One generic request path.** A single `request<T: Decodable>(baseURL:path:queryItems:)` function maps 4xx/5xx onto typed errors and serves all three APIs.
- **A timeline built from two shapes.** Flat hourly forecasts and separate sunrise/sunset timestamps merge into one `TimelineItem` enum keyed by timestamp, so sunrise renders in place inside the 24-hour scroll.
- **Failures stay local.** With `async let`, one failed forecast degrades a single card instead of the whole screen; a 401 is cached per endpoint and shown as locked rather than broken.
- **Sky colours follow the sun.** A four-phase gradient derived from each location's own sunrise, sunset and observation timestamps, with a fallback for short polar days.

### Other projects

Flutter and web work, including an internship project built on the TMDB API — see the [repository list](https://github.com/semihsgt?tab=repositories).

---

## 🛠 Tech Stack

| Category | Technologies |
|---|---|
| **Languages & UI** | ![Swift 6](https://img.shields.io/badge/Swift_6-F05138?style=flat&logo=swift&logoColor=white) ![SwiftUI](https://img.shields.io/badge/SwiftUI-0071E3?style=flat&logo=swift&logoColor=white) ![UIKit](https://img.shields.io/badge/UIKit-2396F3?style=flat&logo=apple&logoColor=white) ![Dart](https://img.shields.io/badge/Dart-0175C2?style=flat&logo=dart&logoColor=white) ![Flutter](https://img.shields.io/badge/Flutter-02569B?style=flat&logo=flutter&logoColor=white) |
| **Concurrency & memory** | ![Swift Concurrency](https://img.shields.io/badge/Swift_Concurrency-0071E3?style=flat&logo=swift&logoColor=white) ![Actors](https://img.shields.io/badge/Actors-0071E3?style=flat&logo=swift&logoColor=white) ![MainActor](https://img.shields.io/badge/@MainActor-0071E3?style=flat&logo=swift&logoColor=white) ![Sendable](https://img.shields.io/badge/Sendable-0071E3?style=flat&logo=swift&logoColor=white) ![ARC](https://img.shields.io/badge/ARC_%26_Retain_Cycles-4A5568?style=flat) |
| **Architecture** | ![MVVM](https://img.shields.io/badge/MVVM-4A5568?style=flat) ![MVVM-C](https://img.shields.io/badge/MVVM--C-4A5568?style=flat) ![Clean Architecture](https://img.shields.io/badge/Clean_Architecture-4A5568?style=flat) ![POP](https://img.shields.io/badge/Protocol--Oriented_Programming-4A5568?style=flat) ![DI](https://img.shields.io/badge/Dependency_Injection-4A5568?style=flat) ![SOLID](https://img.shields.io/badge/SOLID-4A5568?style=flat) |
| **Frameworks & data** | ![URLSession](https://img.shields.io/badge/URLSession-0071E3?style=flat&logo=swift&logoColor=white) ![SwiftData](https://img.shields.io/badge/SwiftData-0071E3?style=flat&logo=swift&logoColor=white) ![Core Data](https://img.shields.io/badge/Core_Data-0071E3?style=flat&logo=apple&logoColor=white) ![CoreLocation](https://img.shields.io/badge/CoreLocation-0071E3?style=flat&logo=apple&logoColor=white) ![MapKit](https://img.shields.io/badge/MapKit-0071E3?style=flat&logo=apple&logoColor=white) ![HealthKit](https://img.shields.io/badge/HealthKit-FF2D55?style=flat&logo=apple&logoColor=white) ![Swift Charts](https://img.shields.io/badge/Swift_Charts-0071E3?style=flat&logo=swift&logoColor=white) ![Combine](https://img.shields.io/badge/Combine-0071E3?style=flat&logo=swift&logoColor=white) |
| **AI integration** | ![Gemini](https://img.shields.io/badge/Google_Gemini-8E75B2?style=flat&logo=googlegemini&logoColor=white) ![Structured Output](https://img.shields.io/badge/Structured_Output_%2F_JSON_Schema-4A5568?style=flat) ![Foundation Models](https://img.shields.io/badge/On--Device_Foundation_Models-4A5568?style=flat) |
| **Testing & tooling** | ![Swift Testing](https://img.shields.io/badge/Swift_Testing-0071E3?style=flat&logo=swift&logoColor=white) ![DocC](https://img.shields.io/badge/DocC-0071E3?style=flat&logo=swift&logoColor=white) ![VoiceOver](https://img.shields.io/badge/VoiceOver_%26_Dynamic_Type-4A5568?style=flat) ![Xcode](https://img.shields.io/badge/Xcode-147EFB?style=flat&logo=xcode&logoColor=white) ![Git](https://img.shields.io/badge/Git-F05032?style=flat&logo=git&logoColor=white) ![SPM](https://img.shields.io/badge/Swift_Package_Manager-F05138?style=flat&logo=swift&logoColor=white) |

---

## 🤝 Let's connect

I'm open to **junior iOS roles and internships**. If you're working on something interesting in Swift, I'd love to hear about it.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/semihsogut/)
[![Email](https://img.shields.io/badge/Email-EA4335?style=flat&logo=gmail&logoColor=white)](mailto:semihsogut.dev@gmail.com)
