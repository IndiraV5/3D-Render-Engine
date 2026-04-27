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

![Frame1](https://github.com/IndiraV5/3D-Render-Engine/blob/master/assets/frame1.png)

## Frame2

![Frame2](https://github.com/IndiraV5/3D-Render-Engine/blob/master/assets/frame2.gif)

## Frame3
The third frame introduces projection and depth handling, allowing the triangle to be rendered in a more realistic 3D perspective. But the blue triangle is still rendered without proper depth handling, causing it to appear on top of the red triangle regardless of their actual positions in 3D space.

![Frame3](https://github.com/IndiraV5/3D-Render-Engine/blob/master/assets/frame3.gif)

## Frame4
The fourth frame blue triangle is rendered with proper depth handling, allowing it to be correctly occluded by the red triangle when it is behind it in 3D space. This demonstrates the implementation of a Z-buffer to manage depth and ensure correct rendering order.

![Frame4](https://github.com/IndiraV5/3D-Render-Engine/blob/master/assets/frame4.gif)

## Frame5
The fifth frame implements basic lighting, calculating surface brightness based on the normal direction of the triangles.

![Frame5](https://github.com/IndiraV5/3D-Render-Engine/blob/master/assets/frame5.gif)

## Frame6
The final frame integrates all previous features and demonstrates sphere rendering with proper rotation, projection, depth handling, and lighting. The result is a fully functional software-based 3D rendering engine that can render complex scenes in real-time.

![Frame6](https://github.com/IndiraV5/3D-Render-Engine/blob/master/assets/frame6.gif)   


## 🛠️ Tech Stack
- Java
- Swing (Rendering UI)
- Custom 3D Math Engine