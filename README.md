# Mealy - Smart To-Do & Quick Meals

Mealy is a Flutter app that combines meal discovery with personal task planning. It uses Firebase for authentication, data storage, and media uploads, and provides distinct user and admin experiences.

## Highlights
- Cross-platform Flutter app with role-based flows for users and admins.
- Firebase Auth and Firestore for secure, real-time data access.
- Meal discovery with favorites, history tracking, and rich detail views.
- Task planner with scheduling, categories, and completion tracking.
- Admin dashboards with analytics and user management.

## Features
### User
- Sign up, login, and remember-me session handling.
- Explore meals, view details, and mark meals as done (history tracking).
- Save favorite meals with sorting and grouping.
- Manage daily tasks with date/time scheduling and completion toggles.
- Profile editing with avatar and cover image uploads.

### Admin
- Add, edit, and delete meals with image upload to Firebase Storage.
- User management with activity metrics (active/inactive/total).
- Analytics dashboards for daily visits and logins.

## Tech Stack
- Flutter (Dart)
- Firebase Auth, Firestore, Firebase Storage
- Provider (ChangeNotifier) for state management
- fl_chart for analytics visualizations
- image_picker, shared_preferences, connectivity_plus

## Architecture
- Presentation + ViewModel pattern using ChangeNotifier and Provider.
- Models in lib/models for meals, users, tasks, and analytics.
- Firestore collections used:
  - users
  - meals
  - visitedMeals
  - daily_logins
  - daily_visits
  - users/{uid}/tasks

## Getting Started
1. Install Flutter (SDK 3.7.2 or later).
2. Run dependencies:
   - flutter pub get
3. Configure Firebase (if not already configured in your environment):
   - Add google-services.json and GoogleService-Info.plist
   - flutterfire configure
4. Run the app:
   - flutter run

## Screenshots
All images are stored in the snapshots folder at the project root.

### Auth and Onboarding
| Splash | Sign In | Sign Up |
| --- | --- | --- |
| ![Splash](snapshots/splash.jpg) | ![Sign In](snapshots/signin.jpg) | ![Sign Up](snapshots/signup.jpg) |

| Reset Password | Code Entry | No Internet |
| --- | --- | --- |
| ![Reset Password](snapshots/resetPassword.jpg) | ![Code Entry](snapshots/codeEnter.jpg) | ![No Internet](snapshots/no_internet_dialog.png) |

### User Experience
| Home | Explore Meals | Profile |
| --- | --- | --- |
| ![Home](snapshots/homepage.png) | ![Explore Meals](snapshots/explore_meals.png) | ![Profile](snapshots/profile.png) |

| Profile Settings | Settings | Confirm Delete |
| --- | --- | --- |
| ![Profile Settings](snapshots/profile_settings.png) | ![Settings](snapshots/settings.png) | ![Confirm Delete](snapshots/confirm_delete_dialog.png) |

| Add Meal | Edit Task | Edit Goal |
| --- | --- | --- |
| ![Add Meal](snapshots/add_meal.png) | ![Edit Task](snapshots/edit_task_dialog.png) | ![Edit Goal](snapshots/edit_goal_dialog.png) |

### Admin Experience
| Admin Home |
| --- |
| ![Admin Home](snapshots/admin_home.png) |

## Development Workflow
- main holds production-ready code.
- dev is the main integration branch for new features.
- feature/* branches are used for isolated work and merged into dev.
