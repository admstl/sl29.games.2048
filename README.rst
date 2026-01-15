sl29.games.2048
=================
An implementation of the 2048 game for educational purpose.

📦 Overview
-----------

The goal of this project is to offer a minimal, educational example of how to:

- Implement a basic **game** in Python (`2048`)
- Package it properly with **PEP 621** conventions (`pyproject.toml`)
- Write and run **unit tests** with `pytest`
- Generate **documentation** automatically using `Sphinx`

🧩 Installation
---------------

It is recommended to work inside a **virtual environment** to avoid dependency conflicts.

🔧 Create and activate a virtual environment
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: bash

   python3 -m venv games2048
   source games2048/bin/activate

Install in development mode
~~~~~~~~~~~~~~~~~~~~~~~~~~~

For development, testing, and documentation:

.. code-block:: bash

   pip install -e .[dev,test,doc]

This will install:

- The package itself
- Development tools (e.g. Jupyter, linters)
- Test dependencies (pytest, pytest-cov)
- Documentation tools (Sphinx, sphinx-rtd-theme, etc.)

Production installation
~~~~~~~~~~~~~~~~~~~~~~~

To install the package as a standard Python package:

.. code-block:: bash

   pip install -e .

or build and install from a wheel:

.. code-block:: bash

   python -m build
   pip install dist/sl29.games.2048-*.whl

Usage Example
-------------

Here’s how to use the game once installed:

.. code-block:: python

   from sl29.games.2048 import Game  # Assuming the main class is Game
   game = Game()
   game.start()
   # Play the game...

Running Tests
-------------

Run all tests:

.. code-block:: bash

   pytest

Run tests with coverage:

.. code-block:: bash

   pytest --cov=sl29.games.2048

Generate HTML coverage report:

.. code-block:: bash

   pytest --cov=sl29.games.2048 --cov-report=html

The HTML report will be generated in the `htmlcov/` directory. Open `htmlcov/index.html` in your web browser to view the coverage details.

Building the Documentation
--------------------------

The documentation is built with Sphinx and assumes you installed the optional doc dependencies.

.. code-block:: bash

   cd doc
   make html

The generated HTML files will be in `doc/_build/html/index.html`. Open this file in your web browser to view the documentation.
