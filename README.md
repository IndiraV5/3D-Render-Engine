# 3D Software Rendering Engine (Java)

A lightweight software-based 3D rendering engine built completely in Java using Swing and pure math (no OpenGL / no libraries).
This project demonstrates how real-time 3D graphics work internally — including transformation, rasterization, and lighting.

``
3D Engine/
│
├── src/
│   └── engine3d/
│       ├── Main.java          → Entry point of application
│       ├── DemoViewer.java    → Swing panel for rendering
│       ├── Renderer.java      → Core rendering engine
│       ├── Vertex.java        → 3D point representation
│       ├── Triangle.java     → 3D triangle mesh unit
│       ├── Matrix3.java      → 3x3 transformation matrix
│       └── Utils.java        → Lighting & mesh utilities
│
└── out/ (generated after compile)
``
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

🖥️ How to Run
1. Compile
`javac -d out src/engine3d/*.java`
2. Run
`java -cp out engine3d.Main`
