# Vehicle Physics & Race Management System (Balance Mod)

![Version](https://img.shields.io/badge/version-1.0.31-blue)
![Platform](https://img.shields.io/badge/platform-CarX%20|%20Unity-orange)
![Language](https://img.shields.io/badge/language-C%23-green)

A comprehensive C#-based refactoring and simulation suite for CarX, designed to implement realistic vehicle balancing, advanced race logic, and real-time multiplayer synchronization.

## 🚀 Key Technical Features

### 1. Advanced Physics Simulation
*   **Aerodynamics Model:** Custom implementation of downforce and drag coefficients:
    *   `aero.sx` — Frontal cross-sectional area (m²) affecting drag force.
    *   `aero.cx` — Drag coefficient (dimensionless) representing aerodynamic resistance.
    *   Both values are calculated and applied in real-time to simulate realistic high-speed behavior.
*   **Engine & Powertrain:** Fine-tuned turbo pressure logic, RPM limiters, and torque curve adjustments to match real-world GT3 specifications.
*   **Weight Dynamics:** Dynamic adjustment of mass distribution:
    *   `frontPercent` — Front/rear weight distribution (%) affecting understeer/oversteer balance.
    *   `upPercent` — Vertical center of mass position (%) influencing roll behavior and stability.

### 2. Race Management System (State Machine)
A robust backend logic handling the entire race weekend lifecycle:
*   **Phases:** Lobby -> Practice -> Qualifying -> Race -> Overtime -> Podium.
*   **Overtime Logic:** Smart finish conditions that account for leader progress and session timers.
*   **Grid Management:** Automated teleportation and anti-stuck systems for synchronized grid starts.

### 3. Multiplayer Synchronization
*   Built on top of the **Kino.Sync API** to ensure all physics and race state changes are broadcasted to clients with minimal latency.
*   Custom network packet handling for real-time telemetry and session configuration.

### 4. Developer & Tuning Tools
*   **Custom Unity Canvas UI:** Built from scratch using Unity's Canvas system and integrated via the mod framework.
*   **IMGUI Dashboard:** Live monitoring of vehicle stats (HP, Torque, Weight distribution, Aero forces).
*   **Real-time Tuning Interface:** On-the-fly adjustments of physics parameters for rapid testing and validation.

![Session Setup UI](https://github.com/kido4sv/Balance-Mod-DRO/blob/main/session_setup.png?raw=true)
![Lap Timing HUD](https://github.com/kido4sv/Balance-Mod-DRO/blob/main/lap_timing.png?raw=true)

## 🛠 Tech Stack
*   **Language:** C# (.NET)
*   **Engine:** Unity Engine
*   **UI:** Unity Canvas, IMGUI
*   **Tools:** Git, Visual Studio, Kino Mod API

## 📋 Installation
1. Install **KSL** (Kino Support Library): [GitHub](https://github.com/trbflxr/ksl)
2. Install **Kino Mod**: [GitHub](https://github.com/trbflxr/kino)
3. Download this mod and drop the `.dll` into:
   `...\CarX Drift Racing Online\kino\mods`

## 🏎 Supported Classes (Balance Presets)
The mod currently includes meticulously researched **BoP (Balance of Performance)** presets for:
*   **GT3 Class:** BMW M4 GT3, Porsche 992 GT3, Ferrari 296 GT3, Aston Martin Vantage GT3, and more.

> **Note:** LMDH and Karting presets have been temporarily removed and may return in future updates.

## 👥 Credits & Contributors
*   **Lead Developer:** [Kido](https://github.com/kido4sv)
*   **Testing & Development Support:** Jeefrect, Popura, Harvok, Giozzik, Xameron, Dranser, Schnordic.

---
*Disclaimer: This project is for educational and community purposes, showcasing C# integration within the Unity environment.*
