# Project Blueprint

## Overview

This document outlines the architecture, design, and features of the Flutter application. The goal is to create a well-structured, visually appealing, and maintainable application following modern Flutter best practices.

## Current State & Style Guide

The application is currently a new Flutter project with the default counter app. The following is the style and architecture guide we will follow for all future development.

*   **Architecture:** We will use a layered architecture, separating UI, business logic, and data. For state management, we'll use `provider` for its simplicity and power.
*   **Theming:** We will use Material Design 3, with a `ColorScheme` generated from a seed color. `google_fonts` will be used for typography to ensure a consistent and beautiful look. Light and dark modes will be supported.
*   **Code Style:** Code will be clean, well-commented, and formatted using `dart format`. We will follow Flutter's best practices for performance and readability.
*   **File Organization:** Code will be organized by feature to keep the project easy to navigate as it grows.

## Current Task: Initial Refactoring

**Plan:**

1.  **Add Dependencies:**
    *   Add `provider` for state management.
    *   Add `google_fonts` for typography.
2.  **Implement Theme:**
    *   Create a `ThemeProvider` class to manage light/dark mode.
    *   Define `ThemeData` for both light and dark themes using `ColorScheme.fromSeed`.
    *   Integrate custom fonts from `google_fonts` into the `TextTheme`.
3.  **Refactor `main.dart`:**
    *   Wrap the root `MyApp` widget with a `ChangeNotifierProvider` to make the `ThemeProvider` available throughout the app.
    *   Update `MyApp` to consume the `ThemeProvider` and apply the correct theme.
4.  **Enhance UI:**
    *   Update the `MyHomePage` to showcase the new theme, including custom text styles, button styles, and a theme toggle button in the `AppBar`.
