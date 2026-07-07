# 2D Steady-State Heat Equation (C++)

Finite-difference solver for the steady-state heat equation on rectangular domains,
supporting Dirichlet and mixed (3×Dirichlet + 1×Neumann) boundary conditions.

## Features
- Mesh generation on rectangular domains
- Linear system assembly for Dirichlet and mixed boundaries
- Choice of linear solver:
  - LU (Eigen)
  - Jacobi
  - Gauss–Seidel
- Convergence tests for Dirichlet and mixed boundary cases

## Build & Run
Requirements:
- C++17 compiler
- CMake
- Eigen

```bash
mkdir -p build
cd build
cmake ..
cmake --build . -j



In order to run the code go the "build" folder, compile the src code using cmake and then the following executables are prepared:

- heat_equation_app: This is the executable for the main solver. It asks the user for the domain values (only rectangular domains), meshsize and the boundary input.
	This generates two text files (mesh.csv and numerical_solution.csv) which are stored in build/results/heat_equation_app_solutions and these can be plotted using the Matlab file "plottingfile.m".
	
- TEST_dirichlet: Runs the convergence test for the Dirichlet BC on a square grid.The results are the mesh-sizes and the corresponding errors which are displayed on the terminal.

- TEST_Neumann: Runs the convergence test for the Neumann-Dirichlett (Mixed) BC on a square grid. The results are the mesh-sizes and the corresponding errors which are displayed on the terminal.

