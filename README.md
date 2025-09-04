# Coupled Convection–Diffusion and Creeping Flow Simulation

This project demonstrates the numerical simulation of **coupled convection–diffusion** with **creeping (Stokes) flow** using finite element methods. It was developed as part of the course **SEE609: Mathematical and Computational Tools for Engineering**.

---

## 📌 Project Overview
The study focuses on:
- **Grid independence** analysis for dynamic viscosity.
- **Velocity field distribution** in creeping flow.
- **Concentration transport** due to convection–diffusion effects.

By increasing the mesh resolution, we analyze how physical quantities such as viscosity, velocity, and concentration evolve, and determine when the results become independent of grid size.

---

## ⚙️ Problem Setup
- **Governing Equations:**
  - Navier–Stokes (creeping flow / low Reynolds number simplification).
  - Convection–diffusion equation for scalar concentration transport.
- **Boundary Conditions:**
  - Inlet: Top wall inflow.
  - Outlet: Right wall outflow.
  - No-slip and concentration constraints on other boundaries.

---

## 📊 Results

### 1. Grid Independence Test
| Elements (n) | log(Δx)  | Avg. Dynamic Viscosity |
|--------------|----------|-------------------------|
| 20           | -1.30103 | 0.002901 |
| 40           | -1.60206 | 0.002800 |
| 80           | -1.90309 | 0.002773 |
| 160          | -2.20412 | 0.002765 |
| 320          | -2.50515 | 0.002763 |

➡️ As the number of elements increases, viscosity stabilizes. Grid independence is achieved near **n = 320**.

---

### 2. Velocity Distribution
- Velocity increases near the outlet due to **conservation of mass** and **boundary constraints**.
- This behavior is typical in creeping flow with narrowed exit boundaries.

---

### 3. Concentration Distribution
| Elements (n) | Max. Concentration |
|--------------|---------------------|
| 20           | 4.17 |
| 40           | 3.94 |
| 80           | 3.87 |
| 160          | 3.85 |
| 320          | 3.84 |

➡️ Concentration is transported by the fluid flow from **left to right**, with diffusion spreading the scalar field. Results stabilize at higher mesh resolutions.

---

## 🖥️ Tools & Methods
- **Finite Element Method (FEM)**
- **Numerical Grid Refinement**
- **Post-processing:** Viscosity, velocity, and concentration plots

---

## 📚 Key Learnings
- Verified **grid independence** for reliable simulation.
- Observed **velocity increase near outlet** due to mass conservation.
- Understood **advection–diffusion interplay** in scalar transport.

---