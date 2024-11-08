### Here are the steps:

1. Create a project directory.
2. Inside the project directory, create the following subdirectories and files:
   - `src/` - Directory for source code.
   - `tests/` - Directory for test code.
   - `README.md` - Project description.
   - `requirements.txt` - List of dependencies.
   - `setup.py` - Script for installing the project.

Here is the structure and content for each file:

### Project Structure
```
my_project/
├── src/
│   └── main.py
├── tests/
│   └── test_main.py
├── README.md
├── requirements.txt
└── setup.py
```

### Create the directories and files

1. **Create the project directory and subdirectories:**
   ```sh
   mkdir my_project
   cd my_project
   mkdir src tests
   ```

2. **Create `main.py` in the `src` directory:**
   ```python
   # src/main.py
   def hello_world():
       return "Hello, world!"

   if __name__ == "__main__":
       print(hello_world())
   ```

3. **Create `test_main.py` in the `tests` directory:**
   ```python
   # tests/test_main.py
   import unittest
   from src.main import hello_world

   class TestMain(unittest.TestCase):
       def test_hello_world(self):
           self.assertEqual(hello_world(), "Hello, world!")

   if __name__ == "__main__":
       unittest.main()
   ```

4. **Create `README.md`:**
   ```markdown
   # My Project

   This is a simple Python project.
   ```

5. **Create `requirements.txt`:**
   ```txt
   # requirements.txt
   # List your project dependencies here
   ```

6. **Create `setup.py`:**
   ```python
   # setup.py
   from setuptools import setup, find_packages

   setup(
       name="my_project",
       version="0.1",
       packages=find_packages(where="src"),
       package_dir={"": "src"},
   )
   ```

### Running the Project

1. **Run the main script:**
   ```sh
   python src/main.py
   ```

2. **Run the tests:**
   ```sh
   python -m unittest discover -s tests
   ```

This will set up a basic Python project structure with a simple script and a unit test.
