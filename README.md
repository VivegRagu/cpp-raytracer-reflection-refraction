# cpp-raytracer-reflection-refraction
Advanced C++ ray tracer implementing reflection, refraction, and Phong lighting model with recursive ray tracing.
# Advanced Ray Tracer - Reflection & Refraction

## 🌟 Project Overview
A comprehensive C++ ray tracing implementation featuring reflection, refraction, and Phong lighting model. This advanced renderer demonstrates physically-based rendering principles with recursive ray tracing for realistic material interactions.

## ✨ Key Features
- **Reflection Implementation**: Mirror-like surfaces with accurate reflection vector calculations
- **Refraction Simulation**: Transparent materials with Snell's Law implementation
- **Phong Lighting Model**: Ambient, diffuse, and specular lighting components
- **Recursive Ray Tracing**: Multi-bounce ray tracing for realistic material interactions
- **Material System**: Configurable materials with reflectivity and transparency properties
- **Total Internal Reflection**: Correct handling of light rays within materials

## 🏗️ Technical Implementation

### Core Components:
1. **Vector Mathematics**: Complete `vec3` class for 3D operations
2. **Ray Class**: Ray representation with origin and direction
3. **Material System**: Configurable surface properties (IOR, reflectivity, transparency)
4. **Scene Management**: Object organization and ray intersection testing

### Key Algorithms:
```cpp
// Reflection calculation
vec3 vec3::reflection(const vec3 &normal) const {
    // R = I - 2*(I·N)*N
    return *this - normal * (2.0 * dot(normal));
}

// Refraction with Snell's Law
std::optional<vec3> vec3::refraction(const vec3 &normal, double IORatio) const {
    // n1 * sinθ1 = n2 * sinθ2
    // Handles total internal reflection
}
