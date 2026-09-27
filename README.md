# Airline Reservation System

A desktop airline booking and management application built as an object-oriented programming project. The interface is written in Flutter, while the core domain logic is implemented in C++ and exposed to Dart through FFI.

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

## Run locally

1. Build the C++ shared library from `cpp_src` with CMake.
2. Set `AIRLINE_ADMIN_PASSWORD` and `AIRLINE_SUPER_ADMIN_PASSWORD` in your local environment.
3. Place the generated library where the Flutter Windows runner can load it.
4. From `flutter_app`, run `flutter pub get`.
5. Start the desktop app with `flutter run -d windows`.

> This is an educational desktop project. The repository does not contain user accounts or passwords and is not designed for production authentication.

## What I practiced

Object-oriented design, inheritance, polymorphism, file persistence, native-library integration, role-based flows, and desktop UI development.

