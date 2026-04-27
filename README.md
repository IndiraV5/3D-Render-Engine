# 3D Software Rendering Engine (Java)

A lightweight software-based 3D rendering engine built completely in Java using Swing and pure math (no OpenGL / no libraries).
This project demonstrates how real-time 3D graphics work internally — including transformation, rasterization, and lighting.


## 📁 Project Structure

```
3D Engine/
│
├── Frames/
│   ├── Frame1.java   → Rotation in X-Y direction
│   ├── Frame2.java   → Extended rotation + improvements
│   ├── Frame3.java   → Projection / 3D depth handling
│   ├── Frame4.java   → Lighting implementation
│   ├── Frame5.java   → Clipping / edge handling
│   └── Frame6.java   → Final integrated engine version
│
├── .gitignore
└── README.md
```

## ⚙️ How It Works

1. Scene Setup
A cube is created using 4 triangles.

2. Rotation
Each frame applies:

Heading (Y-axis rotation)
Pitch (X-axis rotation)

3. Projection
3D coordinates are transformed into 2D screen space.

4. Rasterization
Each triangle is converted into pixels.

5. Z-Buffering
Ensures correct depth rendering (no overlapping glitches).

6. Lighting
Surface brightness calculated using normal direction:
brightness = |normal.z|


## Frame1
The first frame demonstrates basic rotation of a cube in the X-Y plane. It sets up a simple window and renders a rotating cube using Swing's painting capabilities.
![alt text](frame1.png)

## Frame2
The second frame extends the rotation capabilities and includes improvements to the rendering pipeline.



## 🛠️ Tech Stack
- Java
- Swing (Rendering UI)
- Custom 3D Math Engine