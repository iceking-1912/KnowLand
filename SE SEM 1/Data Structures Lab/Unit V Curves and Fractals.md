

- **Curves:** Mathematical representations for smooth and complex shapes in computer graphics
    - Introduction: Need for curves beyond basic primitives (lines, polygons)
    - Interpolation and Approximation: Techniques for creating smooth curves through a set of points
    - Blending Functions: Functions used to control the shape of a curve between points
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



---

### **1. What are fractals? Explain the Triadic Koch Curve with an example. [7 Marks]**

#### Answer:

**Definition of Fractals** (2 Marks):

- Fractals are self-similar, infinitely complex geometrical figures generated by iterative processes.
- They exhibit scale invariance and are used to model natural phenomena like mountains, trees, and coastlines.

**Triadic Koch Curve** (4 Marks):

- The Koch curve is generated by dividing a line segment into three equal parts.
- Replace the middle segment with an equilateral triangle, excluding its base.
- Repeat this process iteratively.

**Example and Diagram** (1 Mark):

- Starting with a straight line of length LLL, after one iteration, the length becomes 43L\frac{4}{3}L34​L.  
    _(Include a simple diagram of the Koch curve's first two iterations.)_

---

### **2. Write a detailed note on the Hilbert Curve. [7 Marks]**

#### Answer:

**Definition** (2 Marks):

- The Hilbert curve is a space-filling fractal that maps a 1D line onto a 2D space.
- It preserves locality, meaning points that are close on the line remain close in 2D.

**Construction** (4 Marks):

1. Divide the space into four quadrants.
2. Connect these quadrants in an "U" shape.
3. Recursively subdivide each quadrant into smaller parts and connect them similarly.
4. Continue this process to increase detail.

**Applications** (1 Mark):

- Used in image compression, spatial indexing in databases, and optimizing memory usage in computer systems.

_(Include a diagram showing the first two iterations of the Hilbert curve.)_

---

### **3. Compare Bezier and B-Spline Curves. List their properties. [6 Marks]**

#### Answer:

**Definitions** (2 Marks):

- **Bezier Curve**: A parametric curve defined by control points and Bernstein polynomials.
- **B-Spline Curve**: A generalization of the Bezier curve, constructed using piecewise polynomials over a knot vector.

**Comparison Table** (4 Marks):

|**Aspect**|**Bezier Curve**|**B-Spline Curve**|
|---|---|---|
|**Control Points**|Affects the entire curve globally.|Local influence of control points.|
|**Flexibility**|Less flexible for complex shapes.|More flexible with additional knots.|
|**Degree**|Fixed for the entire curve.|Can vary across segments.|
|**Continuity**|Cn−1C^{n-1}Cn−1 continuity.|Higher continuity with more knots.|

---

### **4. Explain the blending function for B-Spline curves. [7 Marks]**

#### Answer:

**Definition** (2 Marks):

- The blending function is a set of basis functions used to compute the B-Spline curve.

**Formula** (2 Marks):
The recursive definition of the B-spline basis functions can be simplified into a clearer, step-by-step process:

### 1. **Base Case $N_{i,0}(t)$:**

For k = 0, the basis function $Ni,0(t)$ $N_{i,0}(t)$ is defined as:

$Ni,0​(t)={10​if ti​≤t<ti+1​otherwise​$ 

This means that Ni,0(t)N_{i,0}(t) is 1 between the knots tit_i and ti+1t_{i+1}, and 0 otherwise.

### 2. **Recursive Case (Ni,k(t)N_{i,k}(t)):**

For higher values of kk, the B-spline basis function is defined recursively:

$Ni,k(t)=t−titi+k−tiNi,$

$k−1(t)+ti+k+1−tti+k+1−ti+1Ni+1,k−1(t)N_{i,k}(t)$ = $\frac{t - t_i}{t_{i+k} - t_i} N_{i,k-1}(t) + \frac{t_{i+k+1} - t}{t_{i+k+1} - t_{i+1}} N_{i+1,k-1}(t)$

This formula combines two terms:

- The first term is the scaled basis function from the left segment.
- The second term is the scaled basis function from the right segment.

### Simple Summary:

- For k=0k = 0, $Ni,0(t)N_{i,0}(t)$ is 1 between $tit_i$ and $ti+1t_{i+1}$, and 0 otherwise.
- For $k>0k > 0, Ni,k(t)N_{i,k}(t)$ is a weighted sum of the functions $Ni,k−1(t)N_{i,k-1}(t)$ and $Ni+1,k−1(t)N_{i+1,k-1}(t),$ with the weights depending on the position of tt relative to the knots.


**Properties** (2 Marks):

1. Basis functions are non-negative.
2. Each segment is influenced by k+1k+1k+1 control points.

**Example** (1 Mark):

- Construct a quadratic B-Spline curve with three control points and show the blending functions graphically.

---

### **5. Write a short note on Interpolation and Approximation. [5 Marks]**

#### Answer:

**Definitions** (3 Marks):

- **Interpolation**: A curve passes exactly through given data points.
- **Approximation**: A curve does not pass through all points but closely follows their distribution.

**Comparison** (1 Mark):

- Interpolation is used for precise data fitting (e.g., polynomials).
- Approximation is used for smoothing noisy data (e.g., B-splines).

**Applications** (1 Mark):

- **Interpolation**: Digitizing curves, CAD systems.
- **Approximation**: Animation paths, terrain modeling.

---

### **6. Discuss the applications of fractals in computer graphics. [5 Marks]**

#### Answer:

**Applications** (5 Marks):

1. **Modeling Natural Objects**: Mountains, clouds, trees, and coastlines.
2. **Texture Generation**: Fractal noise adds realism to surfaces.
3. **Compression**: Fractal algorithms are used in image compression techniques.
4. **Procedural Generation**: Creating complex scenes in games and simulations.
5. **Art and Animation**: Generating visually appealing abstract designs.

---

### **1. What are fractals? Explain the types of fractals. [5 Marks]**

**Answer:**

- Fractals are self-similar patterns created through iterative processes.
- **Types of Fractals**:
    1. **Geometric Fractals**: Koch Curve, Sierpinski Triangle.
    2. **Algebraic Fractals**: Mandelbrot and Julia Sets.
    3. **Random Fractals**: Used in modeling clouds and terrains.

---

### **2. What is the significance of fractals in graphics? [5 Marks]**

**Answer:**

1. **Realistic Modeling**: Used to create natural landscapes.
2. **Texture Generation**: Adds realism to surfaces.
3. **Procedural Design**: Efficiently creates complex scenes.
4. **Compression**: Used in fractal-based image compression.

---

### **3. Compare Bezier and B-Spline curves. [6 Marks]**

**Answer:**

|**Aspect**|**Bezier Curve**|**B-Spline Curve**|
|---|---|---|
|Control Points|Global influence|Local influence|
|Flexibility|Less flexible|More flexible with knots|
|Applications|Simple animations|Complex designs and CAD|

---

### **4. What is interpolation? How is it used in computer graphics? [5 Marks]**

**Answer:**

- **Interpolation**: A method to estimate values between known data points.
- **Use in Graphics**:
    1. Smooth animation paths.
    2. Curve fitting in CAD.
    3. Resampling images for scaling.

---

### **5. Write a short note on the Hilbert curve. [5 Marks]**

**Answer:**

- The Hilbert curve is a space-filling fractal that maps 1D lines onto 2D space.
- **Features**:
    1. Preserves locality.
    2. Used in memory allocation and spatial indexing.  
        _(Include a simple U-shaped diagram for visualization.)_

---

### **6. Explain blending functions in B-Spline curves. [6 Marks]**

**Answer:**

- **Blending Function**: Determines the contribution of each control point to the curve.
- Properties:
    1. Non-negative and local.
    2. Defined recursively for smooth transitions.
- Used to generate smooth and flexible curves in graphics.

---

### **7. Discuss the applications of curves in animation. [5 Marks]**

**Answer:**

1. **Path Representation**: Smooth movements.
2. **Object Morphing**: Transition effects.
3. **Keyframe Interpolation**: Filling intermediate frames.
4. **Surface Design**: Creating organic shapes.

---

### **8. What is the difference between deterministic and random fractals? [5 Marks]**

**Answer:**

|**Aspect**|**Deterministic Fractals**|**Random Fractals**|
|---|---|---|
|Definition|Exact, self-similar patterns|Patterns with randomness|
|Examples|Koch Curve, Sierpinski Triangle|Clouds, mountains|

---


### **Unit V: Curves and Fractals**

#### **Curves**

**Q1. Explain interpolation and approximation methods with examples. [5 Marks]**  
**Answer:**

- **Interpolation**:  
    Interpolation involves finding a curve that passes exactly through a set of known data points.
    - **Example**: Linear interpolation connects two points with a straight line, while cubic spline interpolation fits a smooth curve through a series of data points.
- **Approximation**:  
    Approximation fits a curve that doesn’t necessarily pass through all data points but tries to minimize the overall error.
    - **Example**: The least-squares method fits a polynomial to a set of data points by minimizing the sum of squared deviations from the points.

---

**Q2. Write the properties of B-Spline curves. How do they differ from Bezier curves? [6 Marks]**  
**Answer:**

- **Properties of B-Spline Curves**:
    
    1. **Local Control**: A control point affects only a portion of the curve, not the entire curve.
    2. **Piecewise Defined**: B-Splines are made up of piecewise polynomial segments.
    3. **Higher Continuity**: B-Splines provide higher-order continuity, such as C2C^2.
    4. **Flexible Knot Insertion**: Additional control points (knots) can be added for more detailed control.
- **Difference from Bezier Curves**:
    
    1. **Local vs Global Control**: Bezier curves have global control, meaning a single control point affects the entire curve. B-Splines have local control.
    2. **Degree**: Bezier curves are limited to cubic (degree 3) curves, while B-Splines can represent higher-degree curves.
    3. **Continuity**: B-Splines can maintain higher continuity compared to Bezier curves.

---

**Q3. Define blending functions. Explain their role in generating B-Spline curves. [6 Marks]**  
**Answer:**

- **Blending Functions**:  
    Blending functions are used to determine the influence of each control point in a B-Spline curve. Each control point has an associated blending function, which is non-negative and sums to 1.
    
- **Role in B-Splines**:
    
    1. Blending functions ensure that the curve is smooth and continuous.
    2. They calculate the weighted contribution of each control point to the curve.
    3. The curve is defined by these weighted blending functions, ensuring that the curve passes smoothly through the control points.

---

#### **Fractals**

**Q1. What are fractals? Discuss their classification with examples. [5 Marks]**  
**Answer:**

- **Fractals**:  
    Fractals are complex geometric shapes that exhibit self-similarity at different scales, meaning the same patterns repeat at every level of magnification.
    
- **Classification of Fractals**:
    
    1. **Geometric Fractals**: These are generated using simple geometric rules.
        - **Example**: The Sierpinski Triangle, where each triangle is subdivided into smaller triangles recursively.
    2. **Algebraic Fractals**: These are generated using recursive mathematical formulas.
        - **Example**: The Mandelbrot Set, created by iterating a complex function.
    3. **Random Fractals**: These exhibit self-similarity but have random elements, often used to model natural phenomena.
        - **Example**: The coastline of a landmass, which appears jagged at all scales.

---

**Q2. Explain the process of generating the Triadic Koch curve with a diagram. [6 Marks]**  
**Answer:**

- **Triadic Koch Curve**:  
    The Koch curve is generated by iterating a simple rule on each line segment:
    
    1. Divide each line segment into three equal parts.
    2. Replace the middle segment with two new segments that form an equilateral triangle (the "bump").
    3. Repeat the process recursively for each new segment.
- **Diagram**:  
    A simple diagram can show the first few iterations, where each segment is divided and replaced by a triangular "bump."
    

---

**Q3. What is the Hilbert curve? Explain its use in spatial indexing. [5 Marks]**  
**Answer:**

- **Hilbert Curve**:  
    The Hilbert curve is a space-filling fractal that maps a 1D line onto a 2D space. It is constructed by recursively subdividing a square into smaller squares and connecting them in a continuous path.
- **Use in Spatial Indexing**:
    1. The Hilbert curve is used to map multidimensional data into 1D while preserving the locality of the data, meaning points that are close in 2D space will also be close in 1D.
    2. This is useful in applications like databases and image compression, where data locality is important for efficient storage and retrieval.

---
