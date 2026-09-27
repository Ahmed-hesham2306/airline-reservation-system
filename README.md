# Airline Reservation System

A desktop airline booking and management application built as an object-oriented programming project. The interface is written in Flutter, while the core domain logic is implemented in C++ and exposed to Dart through FFI.

[Download the project as a ZIP](https://github.com/Ahmed-hesham2306/airline-reservation-system/archive/refs/heads/main.zip) · [Browse the source code](https://github.com/Ahmed-hesham2306/airline-reservation-system)

## Highlights

- Passenger, administrator, and super-administrator roles
- Flight search, booking, cancellation, and seat selection
- Ticket pricing, travel class, and luggage handling
- Admin tools for flights, users, tickets, and seat availability
- C++ object-oriented design with factory and singleton patterns
- CSV-based persistence for a self-contained desktop demo

## Tech stack

- C++
- Flutter and Dart
- Dart FFI
- CMake

## Project structure

```text
cpp_src/       C++ domain logic, persistence, and FFI bridge
flutter_app/   Flutter desktop interface
```

## Requirements

- Windows 10 or 11
- Flutter SDK with Windows desktop support enabled
- Visual Studio 2022 or Build Tools with **Desktop development with C++**
- CMake 3.14 or newer

Check the setup with `flutter doctor` before continuing.

## Download and run

1. Download the ZIP above and extract it, or clone the repository:

   ```powershell
   git clone https://github.com/Ahmed-hesham2306/airline-reservation-system.git
   cd airline-reservation-system
   ```

2. Choose local demo passwords for the administrator roles:

   ```powershell
   $env:AIRLINE_ADMIN_PASSWORD="choose-a-local-admin-password"
   $env:AIRLINE_SUPER_ADMIN_PASSWORD="choose-a-local-super-admin-password"
   ```

3. Build the C++ bridge. CMake places `libairline_bridge.dll` in the Flutter Windows runner automatically:

   ```powershell
   cmake -S cpp_src -B cpp_src/build -G "Visual Studio 17 2022" -A x64
   cmake --build cpp_src/build --config Release
   ```

4. Install Flutter packages and launch the app:

   ```powershell
   cd flutter_app
   flutter pub get
   flutter run -d windows
   ```

Passenger accounts can be created from the sign-up screen. The CSV files under `flutter_app/DB` are local demo storage and start without personal records.

> This is an educational desktop project. The repository does not contain user accounts or passwords and is not designed for production authentication.

## What I practiced

Object-oriented design, inheritance, polymorphism, file persistence, native-library integration, role-based flows, and desktop UI development.
