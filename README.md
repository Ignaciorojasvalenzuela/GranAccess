<div align="center">

<img src="app/src/main/res/drawable/logo.png" alt="GranAccess logo" width="140"/>

# GranAccess

**Accessible task-management app for a special-education school**

![Kotlin](https://img.shields.io/badge/Kotlin-7F52FF?style=flat&logo=kotlin&logoColor=white)
![Android](https://img.shields.io/badge/Android-3DDC84?style=flat&logo=android&logoColor=white)
![Jetpack Compose](https://img.shields.io/badge/Jetpack%20Compose-4285F4?style=flat&logo=jetpackcompose&logoColor=white)
![Firebase](https://img.shields.io/badge/Firebase-FFCA28?style=flat&logo=firebase&logoColor=black)

</div>

---

## Overview

GranAccess is an Android application built by a team of four for the **Project Management** course (*Dirección y Gestión de Proyectos*) at the **University of Granada** (2024/25).

It helps a small school organise daily tasks for students with different accessibility needs. Each student can use the app in the format that suits them best — **text, pictograms or audio** — while teachers and an administrator manage tasks, menus and material requests from the same app.

## Features

| Role | What they can do |
|---|---|
| **Administrator** | Create and manage student and teacher accounts · create, edit and assign step-by-step tasks · reorder task steps · manage the school canteen menus · send notifications |
| **Teacher** | Request classroom materials |
| **Student** | Log in with a picture-based or text-based login · complete assigned tasks step by step · fulfil material requests · place canteen orders by menu type |

**Accessibility first:** every student has a profile that defines how content is shown (text only, images, or audio), and the login screen itself can be completed with pictures instead of a password.

## Tech stack

- **Language:** Kotlin
- **UI:** Android Views + Jetpack Compose, Material Design
- **Backend:** Firebase Authentication, Cloud Firestore and Firebase Storage
- **Libraries:** Glide and Picasso (image loading), Gson, RecyclerView
- **Min SDK:** 24 (Android 7.0) · **Target SDK:** 34

## Project structure

```
app/src/main/java/com/example/granaccess/
├── cuentas/   # Accounts: login (text / image), registration, user management, role views
├── tareas/    # Tasks: creation, steps, assignment, notifications, canteen menus, materials
└── ui/theme/  # Compose theme (colours, typography)
```

## Getting started

1. Clone the repository and open it in **Android Studio**.
   ```bash
   git clone https://github.com/Ignaciorojasvalenzuela/GranAccess.git
   ```
2. Create your own Firebase project, enable **Authentication**, **Firestore** and **Storage**, and replace `app/google-services.json` with your project's file. The original development database is no longer active.
3. In Firestore, create a `usuarios` collection with a document whose `rol` field is `admin` — this becomes the default administrator.
4. Build and run on a device or emulator (Android 7.0+).

> Some backend features require Firebase's pay-as-you-go **Blaze** plan.

## My contribution

I worked mainly on the **task-management module**: creating, editing and viewing step-by-step tasks, the **notification system** and the **canteen ordering** flow.

## Team

Developed by Alejandro Coman Venceslá, José Antonio Fernández Aranda, Jesús Reyes de Toro and **Ignacio Rojas Valenzuela** — students of the Double Degree in Computer Engineering and Business Administration, University of Granada.

Original repository: [AleComan/GranAccess](https://github.com/AleComan/GranAccess)
