# VectorPlayground

## Introduction

VectorPlayground is an interactive, web-based 3D application designed for visualizing, manipulating, and understanding vectors and vector operations.

## ✨ Features

### 🧭 Core Visualization & Vector Management

* **3D Scene:** Renders vectors and helpers in a navigable 3D space.
* **Add Vectors:** Input vector coordinates (X, Y, Z) and select a color to add new 'base' vectors originating from (0,0,0).
* **Edit Base Vectors:** Modify the coordinates and color of base vectors using the input form.
* **Delete Vectors:** Remove any vector using a dedicated delete button in the list.
* **Vector List:** Displays all current vectors, showing their name, color, coordinates, and dependency information (how result vectors were calculated).

### 🎮 Interaction

* **Orbit Controls:** Navigate the 3D scene by rotating (left-click drag), panning (right-click drag), and zooming (scroll wheel).
* **Drag & Move Vectors:** Intuitively change a vector's direction and magnitude by clicking and dragging its arrowhead directly in the 3D scene (Note: Dragging converts dependent vectors to base vectors).

### 🧮 Vector Operations & Dependencies

* **Dependent Results:** Create new vectors resulting from operations on existing vectors. These result vectors *dynamically update* when their parent vectors change.
    * **Addition:** `C = A + B`
    * **Subtraction:** `C = A - B`
    * **Scalar Multiplication:** `C = s * A`
    * **Cross Product:** `C = A x B` (Result is perpendicular to A and B)
    * **Vector Projection:** `P = Proj_B(A)` (Calculates the projection of A onto B)
* **Dot Product:** Calculates `A · B` and displays the resulting scalar value.
* **Dependency Handling:**
    * Editing or dragging a result vector converts it into a 'base' vector, breaking its dependency link.
    * Deleting a vector converts any vectors that depend on it into 'base' vectors (freezing their last calculated value).

### 📊 UI & Feedback

* **Control Panel:** Centralized UI for adding/editing vectors, selecting operations, viewing results, and controlling scene options.
* **Live Magnitude & Angle:** Displays the real-time magnitude (length) of selected operand vectors A and B, and the angle between them.
* **Result Display:** Shows scalar results (like the dot product) and status messages.
* **Dependency Display:** The vector list clearly indicates how result vectors were formed (e.g., `(V1 + V2)`, `(Proj_V2(V1))`).

### ⚙️ Scene Control

* **Axes Toggle:** Show or hide the main X (red), Y (green), and Z (blue) coordinate axes.
* **Grid Toggle:** Show or hide the ground grid for better spatial reference.

### 💾 Persistence

* **Export Scene:** Save the current state of all vectors (including their definitions and dependencies) to a `.json` file.
* **Import Scene:** Load vectors from a previously exported `.json` file, replacing the current scene.

## 💻 Technologies

* HTML
* CSS (Tailwind CSS)
* JavaScript
* three.js (for 3D graphics and vector math)

## 🔮 Potential Future Features

* Matrix Transformations
* Planes and Lines
* Vector Fields
* Step-by-step Operation Visualization
* And more!

## Use It Here https://git-aarya.github.io/VectorPlayground/
