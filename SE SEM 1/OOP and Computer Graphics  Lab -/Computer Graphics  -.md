---
tags:
  - COMP_PROGRAM
Year: "2024"
Curriculum: s
Semester: "[[SE SEM 1]]"
Course: Computer
Lab: "[[OOP and Computer Graphics  Lab -]]"
lang: cpp
Major: "[[Computer Graphics  -]]"
TREE: "[[CIRICULUM_TREE_CG_SE_SEM3]]"
---
---
# Computer Science [[SE SEM 1]] : C++ Computer Graphics - Detailed Topics
---
## **Unit I: Graphics Primitives and Scan Conversion Algorithms (6 Hours)**

### **Fundamentals:**

- Introduction to computer graphics: Definition, applications in various fields (e.g., animation, engineering design, user interfaces)
- Graphics Primitives: Basic building blocks of computer graphics (points, lines, polygons)
    - Pixel: Smallest unit of a display image
    - Resolution: Number of pixels displayed horizontally and vertically
    - Aspect Ratio: Ratio of width to height of the display area
    - Frame Buffer: Memory location storing the image data for the display
- Display Devices: Types of display technologies (e.g., CRT, LCD, OLED)

## **Introduction to OpenGL:**

- Overview of OpenGL (Open Graphics Library): A popular graphics API for 3D rendering
- OpenGL Architecture: Understanding the core components of OpenGL (rendering pipeline, functions, libraries)
- Primitives and Attributes: Specifying geometric objects and their properties in OpenGL (points, lines, polygons, colors, textures)
- Simple Modeling and Rendering: Creating basic 2D and 3D shapes using OpenGL commands
- Introduction to GLUT (OpenGL Utility Toolkit): A library simplifying interaction with OpenGL for window management and input handling
- Basic User Interaction: Implementing simple mouse and keyboard interactions within a graphics application (e.g., object selection, camera movement)

## **Scan Conversion Algorithms:**

- Converting mathematical object descriptions into pixel representations for display
- Line Drawing Algorithms:
    - Digital Differential Analyzer (DDA): Basic line drawing algorithm
    - Bresenham's Line Algorithm: Efficient and widely used line drawing algorithm
- Circle Drawing Algorithms:
    - DDA and Bresenham's Circle Algorithm: Adapting line algorithms for circles
    - Midpoint Circle Algorithm: Efficient algorithm for drawing circles

## **Exemplar/Case Studies:**

**Study the OpenGL Architecture Review Board (ARB) Extensions:** Explore how ARB extensions add functionality to the core OpenGL library.

**Mapping of Course Outcomes for Unit I (CO1):** Link learning objectives to specific graphics primitives, scan conversion algorithms, and OpenGL concepts covered.

---
## **Unit II: Polygons, Windowing, and Clipping (7 Hours)**

## **Polygons:**

- Introduction: Fundamental geometric shapes with multiple sides and closed paths
- Types of Polygons:
    - Convex Polygons: All interior angles are less than 180 degrees
    - Concave Polygons: At least one interior angle is greater than 180 degrees
    - Complex Polygons: Polygons with holes or self-intersections
- Inside-Outside Testing: Techniques for determining if a point lies inside or outside a polygon

## **Polygon Filling:**

- Techniques for coloring the interior area of a polygon
- Flood-Fill Algorithm: Recursive or iterative approach for filling connected regions
- Seed-Fill Algorithm: Filling based on a starting point (seed)
- Scan-Line Fill Algorithm: Filling based on horizontal scan lines

## **Windowing and Clipping:**

- Viewing Transformations: Transforming objects to fit within the viewing window
- 2D Clipping Algorithms:
    - Cohen-Sutherland Line Clipping Algorithm: Efficiently clips lines against a rectangular window
    - Sutherland-Hodgman Polygon Clipping Algorithm: Clips arbitrary polygons against a window
    - Weiler-Atherton Polygon Clipping Algorithm: Another approach for polygon clipping

## **Exemplar/Case Studies:**

**Develop a simple 2D graphics application using OpenGL:** Implement basic shapes, drawing, and filling functionalities.

**Mapping of Course Outcomes for Unit II (CO2):** Link learning objectives to specific polygon properties, filling algorithms, and windowing/clipping concepts covered.


---


---
# [[CIRICULUM_TREE_CG_SE_SEM3]]

---


## [[Unit III 2D and 3D Transformations and Projections]] (7 Hours)

- **Transformations:** Mathematical operations for manipulating geometric objects in computer graphics
- **Homogeneous Coordinates:** A representation that simplifies transformation calculations
- **2D Transformations:**
    - Translation: Moving an object along the x and y axes
    - Scaling: Increasing or decreasing the size of an object
    - Rotation: Rotating an object about a fixed point
    - Shear: Distorting an object by skewing it
    - Rotation About an Arbitrary Point: Techniques for rotating objects around any point
- **3D Transformations:**
    - Introduction: Extending 2D transformations to the third dimension
    - Translation, Scaling, Rotation, and Shear: Applying these transformations in 3D space
    - Rotation About an Arbitrary Axis: Rotating objects around any axis in 3D
- **Projections:** Techniques for mapping 3D objects onto a 2D viewing plane
    - Parallel Projections:
        - Oblique Projections:
            - Cavalier Projection: Specific type of oblique projection
            - Cabinet Projection: Another type of oblique projection
        - Orthographic Projections: Parallel projections with no distortion
            - Isometric Projection: Equal scaling on all axes
            - Diametric Projection: Object shown at a 45-degree angle
            - Trimetric Projection: Unequal scaling on the axes
    - Perspective Projection: Simulates how we perceive depth, creating vanishing points

**Exemplar/Case Studies:**

- **Study the use of transformations and projections in education and training software:** Analyze how these concepts are applied in educational simulations or training programs that involve 3D visualization.
- **Mapping of Course Outcomes for Unit III (CO3):** Link learning objectives to specific transformation, projection, and homogeneous coordinate concepts covered.



## **[[Unit IV Light, Color, Shading, and Hidden Surfaces]] (6 Hours)**

- **Light and Color:** Fundamental concepts for creating realistic images in computer graphics
    - Properties of Light: Understanding how light interacts with objects (reflection, refraction)
    - CIE Chromaticity Diagram: A visual representation of the human color spectrum
    - Color Models: Mathematical frameworks for representing colors (RGB, HSV, CMY)
- **Illumination Models:** Simulating how light affects the appearance of objects
    - Ambient Light: General background illumination
    - Diffuse Reflection: Light scattered evenly from a surface
    - Specular Reflection: Shiny highlights on a surface
    - Phong Model: A popular illumination model for realistic shading
    - Combining Diffuse and Specular Reflections with Multiple Light Sources: Creating complex lighting effects
    - Warn Model (alternative illumination model, optional)
- **Shading Algorithms:** Techniques for applying illumination models to create smooth transitions of color and depth
    - Flat Shading: Assigning a single color to each polygon face
    - Gouraud Shading: Smoother shading by interpolating colors at polygon vertices
    - Phong Shading: Most realistic shading, calculating color at each pixel based on illumination model
- **Hidden Surface Removal:** Identifying and removing objects that are obscured by other objects in the scene
    - Introduction: Importance of hidden surface removal for realistic rendering
    - Back-Face Detection and Removal: Simple culling technique for discarding invisible faces
    - Hidden Surface Removal Algorithms:
        - Depth Buffer (Z-Buffer): Efficient algorithm storing depth information for each pixel
        - Depth Sorting (Painter's Algorithm): Sorting objects based on their distance from the viewer
        - Area Subdivision (Warnock's Algorithm): Recursive subdivision of the viewing plane

**Exemplar/Case Studies:**

- **Study a popular graphics design software:** Explore how lighting, color, shading, and hidden surface removal are implemented in professional design tools (e.g., Adobe Photoshop, Blender).
- **Mapping of Course Outcomes for Unit IV (CO4):** Link learning objectives to specific light, color, shading, and hidden surface removal concepts covered.

---
## [[Unit V Curves and Fractals]] (6 Hours)**

- **Curves:** Mathematical representations for smooth and complex shapes in computer graphics
    - Introduction: Need for curves beyond basic primitives (lines, polygons)
    - Interpolation and Approximation: Techniques for creating smooth curves through a set of points
    - Blending Functions: Functions used to control the shape of a curve between pointss
- **Parametric Curves:** Defined by equations that specify the x, y, and (optionally) z coordinates of a point on the curve based on a parameter (t)
    - B-Spline Curves: Popular type of parametric curve with smooth continuity properties
    - Bezier Curves: Another type of parametric curve widely used in design applications
- **Fractals:** Self-similar geometric patterns with infinite detail
    - Introduction: Exploring the mathematical beauty and complexity of fractals
    - Classification: Different types of fractals based on their generation process
    - Fractal Generation Algorithms: Techniques for creating specific fractal patterns
        - Snowflake Fractal (Koch snowflake)
        - Triadic Curve (Koch curve)
        - Hilbert Curve (space-filling curve)
    - Applications of Fractals: Utilizing fractals in various domains (e.g., natural object modeling, texture generation)

**Exemplar/Case Studies:**

- **Case Study on Measuring the Length of a Coastline Using Fractals:** Analyze how the fractal nature of coastlines can be captured using appropriate fractal dimensions.
- **Mapping of Course Outcomes for Unit V (CO5):** Link learning objectives to specific curve, fractal, interpolation, and approximation concepts covered.

---
## [[Unit VI Introduction to Animation and Gaming]] (6 Hours)


- **2D Animation Fundamentals:**
    - Introduction: Overview of traditional and computer-based animation techniques
    - Storyboarding and Animation Planning: Creating a visual roadmap for the animation sequence
    - Keyframe Animation: Specifying key poses for objects at specific points in time
    - Animation Languages: Tools for defining animation sequences (optional)
    - Morphing: Transforming one object into another through a smooth transition
- **Gaming Concepts:**
    - Introduction: Exploring the core elements and technologies behind video games
    - Gaming Platforms: Overview of popular hardware and software platforms used for game development (consider mentioning a broader range than just NVIDIA and i8060)
    - Advances in Gaming: Discussing emerging trends and technologies in the gaming industry (e.g., virtual reality, artificial intelligence)

**Exemplar/Case Studies:**

- **Study of an Open-Source Animation/Game Development Tool (e.g.,** _**Unity**_**,** _Maya_**,** _**Blender**_**):** Explore the functionalities and workflows offered by a popular open-source tool for creating animations or games.
- **Mapping of Course Outcomes for Unit VI (CO5):** Link learning objectives to specific animation and gaming concepts covered.

**Note:**

- Removed the mention of i8060 as a specific gaming platform. It's better to discuss broader categories like graphics cards or gaming consoles.



