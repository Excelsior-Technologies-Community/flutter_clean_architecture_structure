# Flutter Clean Architecture

A scalable Flutter project structure based on **Clean Architecture**
with **feature-first design**, **multiple state management support**,
and **dedicated service layer** for APIs and Firebase.

---

## 📂 Project Structure
```
lib/
│
├── extensions/
│ └── app_extension.dart
│
├── helper/
│ ├── connection_helper.dart
│ └── db/
│
├── services/
│ ├── api_services.dart
│ └── firebase_services.dart
│
├── localization/
│ ├── app_translation.dart
│ ├── app_strings.dart
│ └── en_translation.dart
│
├── model/
│ └── data models
│
├── src/
│ └── feature_name/
│ ├── view/
│ │ └── screen.dart
│ ├── widgets/
│ │ └── feature specific widgets
│ └── state_management/
│ ├── controller (GetX)
│ ├── provider (Provider / Riverpod)
│ └── bloc (Bloc)
│
├── utils/
│ ├── app_colors.dart
│ ├── app_constants.dart
│ ├── app_default_text_style.dart
│ ├── app_enums.dart
│ ├── app_routes.dart
│ ├── app_pages.dart
│ ├── app_images.dart
│ └── app_utils.dart
│
└── widgets/
  └──buttons/
    └── primary_button_widget.dart
```

---

## 🧠 Architecture Overview

### 🔹 Feature-First Architecture
Each feature is isolated inside `src/`, making the app:
- Modular
- Scalable
- Easy to maintain

---

## 🔹 Clean Separation of Concerns

| Layer | Responsibility |
|------|---------------|
| View | UI only |
| Widgets | Feature-specific UI |
| State Management | Business logic |
| Services | API & Firebase |
| Models | Data structures |
| Utils | Global constants |
| Helpers | Infra utilities |

---

## 🔹 Service Layer (`services/`)

Handles all **external dependencies**:

### ✅ API Services
- REST APIs
- Headers & tokens
- Network calls

### ✅ Firebase Services
- Authentication
- Firestore / Storage
- Push notifications

> UI and State Management never talk directly to APIs or Firebase.

---

## 🔹 State Management Support

This architecture supports:
- ✅ GetX
- ✅ Provider
- ✅ Riverpod
- ✅ Bloc

Each feature can choose its own approach.

---

## 🌍 Localization Support
- Centralized string keys
- Language-based translations
- No hard-coded strings

---

## ♻ Reusable Widgets
- Global reusable widgets in `widgets/`
- Feature-specific widgets inside feature folders

---

## 🚀 Benefits

✔ Clean & readable code  
✔ Easy testing & mocking  
✔ Scalable for large apps  
✔ Team-friendly  
✔ Production-ready  
✔ Easy library/package conversion  

---

## 🛠 Best Practices

- Keep UI logic inside `view`
- Use `services` for external calls
- Keep models pure (no logic)
- Do not access UI inside services
- Use one state management per feature

---

## 📌 Ideal For

- Medium to large Flutter apps
- Firebase + REST API projects
- Team-based development
- Clean Architecture learners

---

## 📄 License
MIT License
```
Copyright (c) 2025 Excelsior Technologies

Permission is hereby granted, free of charge, to any person obtaining a copy  
of this software and associated documentation files (the "Software"), to deal  
in the Software without restriction, including without limitation the rights  
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell  
copies of the Software, and to permit persons to whom the Software is  
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all  
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED **"AS IS"**, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR  
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,  
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
```

