# Calculator for Complex Numbers, Quaternions, and Coquaternions

## Computer Science (2024/2025)

## In the scope of the *Project* course

#### By:

  * **Bruna Micaela Rodrigues Araújo (AE8679)**
  * **João Nuno Rodrigues Fernandes (A87971)**
  * **Rui Alexandre Dias Neto (A80433)**

-----

### Description:

This project aims to develop a complete and functional calculator, implemented as a web application, capable of operating on complex numbers, quaternions, and coquaternions. The application offers three distinct calculators, each with an interface and a set of operations adapted to the corresponding algebra.

The web interface is interactive and intuitive, allowing for easy navigation between the different calculation modes. Each calculator maintains a separate history of operations and supports the use of previous results in new calculations, providing a fluid and efficient user experience.

-----

### Technologies Used:

The calculator was developed using a set of modern technologies to ensure robustness, interactivity, and an efficient implementation:

  * **Backend:**

      * **Python 🐍:** The main language for all server-side logic and algebraic manipulation.
      * **Flask 🌐:** A micro-framework used to build the web application, manage routes, and serve the HTML pages.
      * **NumPy 🔢:** A fundamental library for calculations in the real and complex number calculator, offering high performance and a wide range of mathematical functions.

  * **Frontend:**

      * **HTML ✨:** Used for the semantic structuring of the calculator pages.
      * **CSS 🌈:** Responsible for the styling and responsive design, ensuring a pleasant and consistent visual presentation.
      * **JavaScript 🛠️:** Adds dynamic interactivity to the interface, enabling display manipulation, history management, and real-time support for keyboard shortcuts.

  * **Expression Processing:**

      * **re (Regular Expressions) 🔍:** A module used intensively for parsing and transforming the mathematical expressions entered by the user, converting them into a format that can be evaluated by the backend.

  * **Deployment:**

      * **Docker 🐳:** The application is fully containerized, which simplifies its setup and execution in any environment, ensuring the consistency of dependencies and the system.

-----

### Main Features:

The application is divided into three calculators, each with specific features:

#### 1\. Real and Complex Number Calculator

  * Complete arithmetic operations.
  * Support for **complex numbers** in the `a + bi` format.
  * Trigonometric (sin, cos, tan) and hyperbolic (sinh, cosh, tanh) functions, including their inverses.
  * Angle calculation mode in **Radians (RAD)** and **Degrees (DEG)**.
  * Specific functions for complex numbers: real part (`real`), imaginary part (`imag`), argument (`arg`), conjugate (`conj`), and modulus (`abs`).
  * Calculation of logarithms (natural and base 10), exponentials, square roots, and powers.

#### 2\. Quaternion Calculator

  * Full implementation of **Hamilton's quaternion algebra** ($q = a + bi + cj + dk$).
  * **Non-commutative** multiplication ($ij = k$, but $ji = -k$).
  * Left (`divL`) and right (`divR`) division.
  * Trigonometric, hyperbolic, logarithmic, exponential, and power functions extended to quaternions.
  * Specific operations such as `conjugate`, `norm` (Euclidean norm), `inverse`, `vectorial` (vector part), `arg`, and normalization.

#### 3\. Coquaternion (Split-Quaternion) Calculator

  * Implementation of **coquaternion algebra**, which uses the Minkowski metric ($i² = -1, j² = +1, k² = +1$).
  * Calculation of functions (exponential, trigonometric, etc.) based on the coquaternion's classification as **timelike**, **spacelike**, or **lightlike**.
  * Operations such as `norm` (Minkowski norm), `conjugate`, `inverse`, and `vectorial`.
  * Helper functions like `absIJK` (norm of the vector part) and `sign`.

#### Common Features

  * **Intuitive Web Interface:** A clean and functional design with buttons for all operations.
  * **Calculation History:** Each calculator stores the last 20 operations.
  * **Reuse Calculations:** It is possible to load expressions or results from the history directly to the display.
  * **Keyboard Support:** The calculator can be fully operated via the keyboard.
  * **Navigation Menu:** Allows for easy switching between the three calculator types.

-----

### How to Run the Project

There are two ways to run the application: using Docker (recommended) or locally in a Python virtual environment.

#### 1\. Using Docker (Recommended Method)

With Docker installed, simply run the following commands in the project's root directory:

1.  **Build the Docker image:**

    ```bash
    docker build -t hypercomplex-calculator .
    ```

2.  **Run the container:**

    ```bash
    docker run -p 5000:5000 hypercomplex-calculator
    ```

The application will be accessible at `http://localhost:5000`.

#### 2\. Locally (Virtual Environment)

Requires Python 3.10 or higher.

1.  **Create and activate a virtual environment:**

    ```bash
    # Create
    python -m venv venv

    # Activate (Windows)
    .\venv\Scripts\activate

    # Activate (macOS/Linux)
    source venv/bin/activate
    ```

2.  **Install the dependencies:**

    ```bash
    pip install -r requirements.txt
    ```

3.  **Run the Flask application:**

    ```bash
    flask run
    ```

The application will be accessible at `http://127.0.0.1:5000`.
