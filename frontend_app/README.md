# frontend_app

Foodie Delivery - Flutter mobile app (Ocean Professional)

## Overview
This app includes a modern, minimalist UI using the Ocean Professional theme:
- Primary: #2563EB (blue), Accent/Secondary: #F59E0B (amber), Error: #EF4444
- Subtle shadows, rounded corners, and smooth transitions
- Tab-based navigation with four screens: Home, Search, Orders, Profile

## Structure
- lib/main.dart: App entrypoint and AppShell with bottom navigation.
- lib/theme/app_theme.dart: Ocean Professional ThemeData builder.
- lib/models/: Simple data model scaffolds (e.g., restaurant.dart).
- lib/ui/screens/
  - home/home_screen.dart
  - search/search_screen.dart
  - orders/orders_screen.dart
  - profile/profile_screen.dart
- lib/ui/widgets/: Reusable UI components (e.g., gradient_header.dart).

## Navigation
The app uses Material 3 NavigationBar:
- Home: Discover restaurants, sample cards and categories.
- Search: Search field and helpful suggestions.
- Orders: Empty state and past orders placeholders.
- Profile: Basic account/settings placeholders.

## Running
- flutter pub get
- flutter run

No external environment variables are required at this stage.

## Extending the app
- API integration:
  - Place networking and repository code under a new folder, e.g., `lib/data/`.
  - Update models in `lib/models/` and map API responses in repositories.
  - Do not use BuildContext across async gaps. Fetch data in async methods, store primitive state; build UI based on state flags in build().
- State management:
  - Provider is available if you need it later. Create providers under `lib/state/`.
- UI:
  - Reuse common widgets from `lib/ui/widgets/`.
  - Follow the theme and shape guidelines from `lib/theme/app_theme.dart`.

## Notes
The screens contain placeholder content and are designed to build and run in the preview environment. Replace placeholders with live data and interactions as APIs become available.
