# FieldMapper (Pecki)

> An Android utility for surveying, marking, and managing field boundaries and polygon areas directly on the map using on-device GPS.

![Android](https://img.shields.io/badge/Platform-Android-3DDC84?style=flat&logo=android&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-blue.svg)

---

## Overview

**FieldMapper** is an Android application designed for outdoor mapping and boundary tracing. By walking along a perimeter in the field, users can register GPS vertices in real time to generate accurate 2D polygons.

Saved areas are persisted in a local database and can be reviewed at any time. When inspecting a saved area, the app displays the saved polygon overlay together with your live GPS location, making field verification, inspection, and navigation intuitive.

### Typical Use Cases

- **Agriculture & Forestry:** Outline plots, crop fields, or forest sectors without specialized survey gear.
- **Land & Property Inspection:** Walk and verify approximate boundary markers on-site.
- **Outdoor & Events:** Mark camping grounds, search sectors, event boundaries, or designated outdoor zones.

---

## Screenshots

<p align="center">
  <img src="https://github.com/b-proszkowiec/LocationMarker/blob/sample-picture/sample_picture.jpg" width="300">
</p>

---

## Features

- **GPS Vertex Marking:** Capture exact geographic coordinates directly in the field with a single tap.
- **Dynamic Polygons:** Connect points sequentially to create and render custom shapes and perimeters on the map.
- **Local Storage & Management:** Save, name, list, and delete custom areas locally.
- **Live Location Overlay:** View your current real-time GPS position over previously saved polygons.
- **Lightweight & Field-Ready:** Minimal overhead, responsive UI, and persistent offline storage.

---

## Tech Stack

- **Language:** Kotlin _(or Java)_
- **Architecture:** MVVM (Model-View-ViewModel)
- **Map SDK:** Google Maps SDK for Android _(or OSMDroid / Mapbox)_
- **Location Engine:** Google Play Services — `FusedLocationProviderClient`
- **Local Persistence:** Room Database / SQLite
- **UI Components:** Material 3 / Android Jetpack (ViewBinding / Compose)

---

## Getting Started

### Prerequisites

- Android Studio Iguana (or newer)
- Android device (recommended for real-world GPS testing) or an emulator with location simulation enabled
- Google Maps API Key (if using Google Maps SDK)

### Installation

1. **Clone the repository:**

   ```bash
   git clone https://github.com/b-proszkowiec/LocationMarker.git

   ```

2. Open the project in Android Studio: File ➔ Open... ➔ Select the cloned
   directory.

3. Configure Map API Credentials: If the project uses Google Maps, add your API
   key in local.properties:

   MAPS_API_KEY=YOUR_GOOGLE_MAPS_API_KEY_HERE

   (Ensure the Google Maps SDK for Android is enabled in your Google Cloud
   Console).

4. Build and Run: Sync Gradle and deploy the app to your physical test device.

### Permissions

The application requires runtime permissions to provide full GPS accuracy:

- ACCESS_FINE_LOCATION – Required to capture precise GPS coordinates for
  polygon vertices.
- ACCESS_COARSE_LOCATION – Fallback network-based coarse location.
- INTERNET – Required to download map tiles and geolocation data.

### License

This project is licensed under the MIT License - see the LICENSE file for
details.

Author

- Boguslaw Proszkowiec – [GitHub Profile](https://github.com/b-proszkowiec)
