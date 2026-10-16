# MIT 18.06SC Linear Algebra — Implementación en Python & NumPy

![Python](https://img.shields.io/badge/Python-3.10%2B-blue?logo=python&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-2.0%2B-013243?logo=numpy&logoColor=white)
![SciPy](https://img.shields.io/badge/SciPy-Scientific_Computing-8CAAE6?logo=scipy&logoColor=white)
![Pytest](https://img.shields.io/badge/Tests-Pytest-0A9EDC?logo=pytest&logoColor=white)
![Status](https://img.shields.io/badge/Estado-En_Progreso-orange)

Implementación desde cero (_from scratch_) y mediante **NumPy/SciPy** de los algoritmos fundamentales del curso **18.06SC Linear Algebra** del MIT impartido por **Gilbert Strang**: descomposición $PA=LU$, proyecciones ortogonales, regresión por mínimos cuadrados, ortogonalización de Gram-Schmidt, autovalores/autovectores y compresión de imágenes mediante SVD, validados con tests unitarios en `Pytest`.

---

## Enfoque y Metodología

Cada sesión del curso se aborda en tres capas complementarias:

1. **Intuición Geométrica (`notebooks/`):** Visualización de transformaciones lineales, subespacios y proyecciones en 2D/3D con `Matplotlib` junto con las demostraciones matemáticas en **LaTeX**.
2. **Algoritmos desde cero (`src/`):** Implementación en Python puro / operaciones matriciales elementales para comprender la mecánica interna y el coste computacional ($O(n^3)$, estabilidad numérica y pivoteo).
3. **Verificación Industrial (`tests/`):** Validación automatizada con `pytest` comparando los algoritmos propios frente a las rutinas optimizadas en C/Fortran de `numpy.linalg` y `scipy.linalg`.

---

## Estructura del Repositorio

```text
mit-18.06-linear-algebra-python/
├── notebooks/
│   ├── unit_1_ax_equals_b/                # Clases 01 a 13: Sistemas lineales, LU y los 4 subespacios
│   ├── unit_2_least_squares_determinants/ # Clases 14 a 20: Ortogonalidad, Gram-Schmidt y Determinantes
│   └── unit_3_eigenvalues_svd/            # Clases 21 a 34: Autovalores, Markov, matrices simétricas y SVD
├── src/                                   # Módulos en Python con implementaciones desde cero
├── projects/                              # Mini-proyectos aplicados al mundo real
├── tests/                                 # Suite de tests unitarios (Pytest)
└── requirements.txt                       # Dependencias del entorno
```

---

## Proyectos Aplicados Destacados

| Proyecto                                                    | Conceptos de 18.06 aplicados                                                                   | Archivo                                      |    Estado    |
| :---------------------------------------------------------- | :--------------------------------------------------------------------------------------------- | :------------------------------------------- | :----------: |
| **1. Resolución de Redes Eléctricas y Grafo de Incidencia** | Espacio nulo $N(A)$, leyes de Kirchhoff matriciales y eliminación Gaussiana                    | `projects/01_graphs_and_networks.ipynb`      | ⏳ Pendiente |
| **2. Predictor por Mínimos Cuadrados y QR**                 | Proyección en el espacio columna $C(A)$, ecuaciones normales $A^TA\hat{x}=A^Tb$ y Gram-Schmidt | `projects/02_least_squares_regression.ipynb` | ⏳ Pendiente |
| **3. Compresión de Imágenes con SVD y Algoritmo PageRank**  | Descomposición en Valores Singulares ($A = U\Sigma V^T$) y Cadenas de Markov ($\lambda = 1$)   | `projects/03_svd_image_compression.ipynb`    | ⏳ Pendiente |

---

## Progreso del Curso (MIT 18.06SC)

### Unidad 1: Sistemas $Ax = b$ y los Cuatro Subespacios

| Sesión | Tema de la Clase (Gilbert Strang)                                             | Notebook / Código                         |    Estado    |
| :----: | :---------------------------------------------------------------------------- | :---------------------------------------- | :----------: |
| **01** | The Geometry of Linear Equations (Visión por filas vs. columnas)              | `01_geometry_of_linear_equations.ipynb`   | 🔄 En curso  |
| **02** | Elimination with Matrices ($Ax = b \rightarrow Ux = c$)                       | `02_elimination_with_matrices.ipynb`      | ⏳ Pendiente |
| **03** | Multiplication and Inverse Matrices ($A^{-1}$ y Gauss-Jordan)                 | `03_multiplication_and_inverse.ipynb`     | ⏳ Pendiente |
| **04** | Factorization into $A = LU$ y $PA = LU$                                       | `04_lu_factorization.ipynb`               | ⏳ Pendiente |
| **05** | Transposes, Permutations, Vector Spaces $\mathbb{R}^n$                        | `05_transposes_permutations_spaces.ipynb` | ⏳ Pendiente |
| **06** | Column Space $C(A)$ and Nullspace $N(A)$                                      | `06_column_space_and_nullspace.ipynb`     | ⏳ Pendiente |
| **07** | Solving $Ax = 0$: Pivot Variables, Special Solutions ($R = \mathrm{rref}(A)$) | `07_solving_ax_0_rref.ipynb`              | ⏳ Pendiente |
| **08** | Solving $Ax = b$: Row Reduced Form $R$ ($x = x_p + x_n$)                      | `08_solving_ax_b_complete.ipynb`          | ⏳ Pendiente |
| **09** | Independence, Basis, and Dimension                                            | `09_independence_basis_dimension.ipynb`   | ⏳ Pendiente |
| **10** | The Four Fundamental Subspaces: $C(A), N(A), C(A^T), N(A^T)$                  | `10_four_fundamental_subspaces.ipynb`     | ⏳ Pendiente |
| **11** | Matrix Spaces; Rank 1; Small World Graphs                                     | `11_matrix_spaces_rank1.ipynb`            | ⏳ Pendiente |
| **12** | Graphs, Networks, Incidence Matrices                                          | `12_graphs_networks_incidence.ipynb`      | ⏳ Pendiente |
| **13** | Quiz 1 Review                                                                 | `13_unit1_review_exam.ipynb`              | ⏳ Pendiente |

### Unidad 2: Mínimos Cuadrados, Determinantes y Autovalores

| Sesión | Tema de la Clase (Gilbert Strang)                      | Notebook / Código                         |    Estado    |
| :----: | :----------------------------------------------------- | :---------------------------------------- | :----------: |
| **14** | Orthogonal Vectors and Subspaces ($N(A) \perp C(A^T)$) | `14_orthogonal_vectors_subspaces.ipynb`   | ⏳ Pendiente |
| **15** | Projections onto Subspaces: $P = A(A^TA)^{-1}A^T$      | `15_projections_onto_subspaces.ipynb`     | ⏳ Pendiente |
| **16** | Projection Matrices and Least Squares                  | `16_least_squares_regression.ipynb`       | ⏳ Pendiente |
| **17** | Orthogonal Matrices and Gram-Schmidt ($A = QR$)        | `17_gram_schmidt_qr.ipynb`                | ⏳ Pendiente |
| **18** | Properties of Determinants                             | `18_properties_of_determinants.ipynb`     | ⏳ Pendiente |
| **19** | Determinant Formulas and Cofactors                     | `19_determinant_formulas_cofactors.ipynb` | ⏳ Pendiente |
| **20** | Cramer's Rule, Inverse Matrix, and Volume              | `20_cramers_rule_inverse_volume.ipynb`    | ⏳ Pendiente |

### Unidad 3: Matrices Definidas Positivas y Aplicaciones (SVD)

| Sesión | Tema de la Clase (Gilbert Strang)                                 | Notebook / Código                       |    Estado    |
| :----: | :---------------------------------------------------------------- | :-------------------------------------- | :----------: |
| **21** | Eigenvalues and Eigenvectors ($Ax = \lambda x$)                   | `21_eigenvalues_eigenvectors.ipynb`     | ⏳ Pendiente |
| **22** | Diagonalization and Powers of $A$ ($A = S\Lambda S^{-1}$)         | `22_diagonalization_powers.ipynb`       | ⏳ Pendiente |
| **23** | Differential Equations and $\exp(At)$                             | `23_differential_equations_expAt.ipynb` | ⏳ Pendiente |
| **24** | Markov Matrices; Fourier Series                                   | `24_markov_matrices_fourier.ipynb`      | ⏳ Pendiente |
| **25** | Symmetric Matrices and Positive Definiteness ($A = Q\Lambda Q^T$) | `25_symmetric_positive_definite.ipynb`  | ⏳ Pendiente |
| **26** | Complex Matrices; Fast Fourier Transform (FFT)                    | `26_complex_matrices_fft.ipynb`         | ⏳ Pendiente |
| **27** | Positive Definite Matrices and Minima                             | `27_positive_definite_minima.ipynb`     | ⏳ Pendiente |
| **28** | Similar Matrices and Jordan Form                                  | `28_similar_matrices_jordan.ipynb`      | ⏳ Pendiente |
| **29** | Singular Value Decomposition ($A = U\Sigma V^T$)                  | `29_singular_value_decomposition.ipynb` | ⏳ Pendiente |
| **30** | Linear Transformations and Their Matrices                         | `30_linear_transformations.ipynb`       | ⏳ Pendiente |
| **31** | Change of Basis; Image Compression                                | `31_change_of_basis_compression.ipynb`  | ⏳ Pendiente |
| **32** | Quiz 3 Review                                                     | `32_unit3_review.ipynb`                 | ⏳ Pendiente |
| **33** | Left and Right Inverses; Pseudoinverse ($A^+$)                    | `33_pseudoinverse_moore_penrose.ipynb`  | ⏳ Pendiente |
| **34** | Final Course Review                                               | `34_final_course_review.ipynb`          | ⏳ Pendiente |

---

## Instalación y Ejecución Local

Para reproducir los cuadernos y ejecutar la suite de tests en tu máquina (compatible con Apple Silicon / macOS y Linux):

```bash
# 1. Clonar el repositorio
git clone [https://github.com/11hidalgo/mit-18.06-linear-algebra-python.git](https://github.com/11hidalgo/mit-18.06-linear-algebra-python.git)
cd mit-18.06-linear-algebra-python

# 2. Crear y activar el entorno virtual
python3 -m venv .venv
source .venv/bin/activate

# 3. Instalar dependencias
pip install -r requirements.txt

# 4. Ejecutar tests unitarios
pytest
```

---

## Referencias

- **Curso Oficial:** [MIT 18.06SC Linear Algebra (OpenCourseWare)](https://ocw.mit.edu/courses/18-06sc-linear-algebra-fall-2011/)
- **Libro de texto:** Gilbert Strang, _Introduction to Linear Algebra_, 5th Edition, Wellesley-Cambridge Press.
