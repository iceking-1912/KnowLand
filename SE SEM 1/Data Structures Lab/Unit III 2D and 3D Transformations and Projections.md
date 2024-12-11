
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


---

### **Unit III: 2D, 3D Transformations and Projections**

#### **2D Transformations**

**Q1. Define homogeneous coordinates. Explain their significance in 2D transformations. [5 Marks]**  
**Answer:**

- **Homogeneous Coordinates**:  
    In homogeneous coordinates, each point in a 2D plane is represented by a 3D vector (x,y,1)(x, y, 1), where xx and yy are the Cartesian coordinates, and 11 is the homogeneous coordinate.
    - **Significance**:
        1. Homogeneous coordinates allow transformations (translation, scaling, rotation) to be represented using matrix multiplication.
        2. They provide a unified way to handle both linear and affine transformations.
        3. Transformation matrices can easily be combined, simplifying the transformation process.

---

**Q2. Derive the transformation matrix for 2D rotation about an arbitrary point. [6 Marks]**  
**Answer:**  
To rotate a point (x,y)(x, y) about an arbitrary point (x0,y0)(x_0, y_0) by an angle θ\theta, we follow these steps:

1. **Translate the point (x0,y0)(x_0, y_0) to the origin**: $$T_{1} = \begin{bmatrix} 1 & 0 & -x_0 \\ 0 & 1 & -y_0 \\ 0 & 0 & 1 \end{bmatrix}$$
2. **Rotate the point by angle θ\theta about the origin**: $$R = \begin{bmatrix} \cos(\theta) & -\sin(\theta) & 0 \\ \sin(\theta) & \cos(\theta) & 0 \\ 0 & 0 & 1 \end{bmatrix}$$
3. **Translate the point back**: $$$T_{2} = \begin{bmatrix} 1 & 0 & x_0 \\ 0 & 1 & y_0 \\ 0 & 0 & 1 \end{bmatrix}$$$
4. **Combined transformation matrix**: 
5. $M = T_{2} \cdot R \cdot T_{1}$

---

**Q3. Explain the steps for scaling a 2D object using a given reference point. [5 Marks]**  
**Answer:**

1. **Translate the object** such that the reference point moves to the origin: 
2. $T_{1} = \begin{bmatrix} 1 & 0 & -x_0 \\ 0 & 1 & -y_0 \\ 0 & 0 & 1 \end{bmatrix}$
3. **Scale the object** by the scaling factors SxS_x and SyS_y: 
4. $S = \begin{bmatrix} S_x & 0 & 0 \\ 0 & S_y & 0 \\ 0 & 0 & 1 \end{bmatrix}$
5. **Translate back to the original position**: 
6. $T_{2} = \begin{bmatrix} 1 & 0 & x_0 \\ 0 & 1 & y_0 \\ 0 & 0 & 1 \end{bmatrix}$
7. **Final transformation matrix**: $M=T2⋅S⋅T1M = T_{2} \cdot S \cdot T_{1}$

---

#### **3D Transformations**

**Q1. What is the difference between 2D and 3D transformations? [4 Marks]**  
**Answer:**

- **2D Transformations**: Operate in a two-dimensional space using coordinates (x,y)(x, y). Transformations include translation, scaling, rotation, and shear.
- **3D Transformations**: Operate in three-dimensional space with coordinates (x,y,z)(x, y, z). Transformations involve translation, scaling, rotation, and shear, but in 3D, these transformations can occur along the z-axis as well as the x and y axes.

---

**Q2. Derive the transformation matrix for 3D rotation about an arbitrary axis. [6 Marks]**  
**Answer:**

- **Rotation about an arbitrary axis** (for example, the axis defined by a unit vector $$$\hat{v}=(vx,vy,vz)$$$ is achieved by using Rodrigues' rotation formula:
- $$$R = I + \sin(\theta) [\hat{v}]_{\times} + (1 - \cos(\theta)) [\hat{v}]_{\times}^2$$
- where $[v^]×[\hat{v}]_{\times}$ is the skew-symmetric matrix of v^\hat{v}, II is the identity matrix, and θ\theta is the angle of rotation.  
    This formula produces a matrix that rotates points in 3D space about the axis v^\hat{v}.

---

**Q3. Explain how shear transformation is applied in 3D space with an example. [5 Marks]**  
**Answer:**

- **Shear Transformation**: A shear operation distorts the shape of an object in a specified direction, typically along one of the axes, while keeping other coordinates fixed.
- **Shear in 3D**: A shear transformation can be applied along the x, y, or z axes. For example, applying shear along the x-axis in the y-direction would result in: $$$M = \begin{bmatrix} 1 & S_{xy} & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1 \end{bmatrix}$$$ where SxyS_{xy} is the shear factor.

---

#### **Projections**

**Q1. Explain the difference between Cavalier and Cabinet projections. [5 Marks]**  
**Answer:**

- **Cavalier Projection**: A type of oblique projection where the projection lines are drawn at 45° to the horizontal, and the scale along the axis is preserved (i.e., no foreshortening). The object appears distorted but proportional along the viewing plane.
- **Cabinet Projection**: Another type of oblique projection where the projection lines are also at 45°, but the scale along the axis is halved (i.e., foreshortened). This gives a more realistic view by reducing distortion.

---

**Q2. What are vanishing points? Explain 1-point, 2-point, and 3-point perspective projections. [6 Marks]**  
**Answer:**

- **Vanishing Points**: Points where parallel lines in a 3D space appear to converge in a 2D projection.
    - **1-point Perspective**: All parallel lines converge to a single vanishing point along the horizon (e.g., a road stretching into the distance).
    - **2-point Perspective**: Two sets of parallel lines converge to two vanishing points along the horizon (e.g., a building viewed at an angle).
    - **3-point Perspective**: Adds a third vanishing point either above or below the horizon for a more dramatic view (e.g., looking up at a tall building).

---

**Q3. Compare orthographic projections (isometric, diametric, and trimetric). [5 Marks]**  
**Answer:**

- **Isometric Projection**: All three axes are equally foreshortened (typically at a 30° angle to the horizontal plane).
- **Diametric Projection**: Two axes are equally foreshortened, and one is not (usually at a 45° angle).
- **Trimetric Projection**: The three axes have different levels of foreshortening, creating a non-uniform perspective.

---
