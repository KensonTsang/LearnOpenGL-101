# 🌀 OpenGL + CMake + Conan Template

A minimal cross-platform C++ OpenGL project using **CMake** and **Conan 2.x**.  
This project sets up an OpenGL 3.3 context with GLFW and GLAD, and compiles cleanly on **macOS**, **Linux**, and **Windows**.

---

## 🚀 Features

- ✅ OpenGL 3.3 Core Profile context  
- ✅ GLFW for window/context creation  
- ✅ GLAD for OpenGL function loading  
- ✅ Conan 2.x for dependency management  
- ✅ CMake 3.15+ build system  
- ✅ macOS Retina-safe (with proper hints)

---

## 📦 Dependencies (via Conan)

- `glfw/3.3.8`  
- `glad/0.1.36`

---

## 🛠️ Requirements

- CMake ≥ 3.15  
- Conan ≥ 2.0  
- C++17 compiler (e.g. AppleClang 17, GCC 11+, MSVC 2022)

---

## 🧱 Build Instructions

### 1️⃣ Clone the Project

```bash
git clone git@github.com:KensonTsang/LearnOpenGL-101.git
cd OpenGL-0-Template
```

### 2️⃣ Install Conan Dependencies

```bash
conan install . \
  --output-folder=build \
  --build=missing \
  --generator=CMakeDeps \
  --generator=CMakeToolchain
```

### 3️⃣ Configure with CMake

```bash
cmake -S . -B build \
  -DCMAKE_TOOLCHAIN_FILE=build/conan_toolchain.cmake \
  -DCMAKE_BUILD_TYPE=Release
```

### 4️⃣ Build the Project

```bash
cmake --build build
```

### 5️⃣ Run the App

```bash
./build/OpenGLApp
```

---

## 📁 Project Structure

```text
.
├── CMakeLists.txt
├── conanfile.txt
├── README.md
└── src/
    └── main.cpp
```

---

### 🧠 VSCode Setup (Optional)
For best experience with IntelliSense and build integration in Visual Studio Code, add the following to `.vscode/settings.json:`

```
{
  "cmake.configurationProvider": "ms-vscode.cmake-tools"
}
```
---


