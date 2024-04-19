# Python Unit Testing

This repository provides a comprehensive guide on unit testing in Python using frameworks like `unittest` and `pytest`. It covers the basics of setting up test cases, running tests, and interpreting results to ensure your Python code works as expected.

## Prerequisites

- Python installed on your machine
- Basic understanding of Python programming

## Installation

### Setting Up Testing Environment

1. **Install pytest**:
   ```bash
   pip install pytest
   ```

## Writing Test Cases

### Using `unittest`

- `unittest` is a built-in Python module. No installation is required.
- Create a file named `test_calculation.py`:

  ```python
  import unittest

  def add(x, y):
      return x + y

  class TestCalculation(unittest.TestCase):
      def test_add(self):
          self.assertEqual(add(10, 5), 15)
          self.assertEqual(add(-1, 1), 0)
          self.assertEqual(add(-1, -1), -2)

  if __name__ == '__main__':
      unittest.main()
  ```

### Using `pytest`

- `pytest` is a powerful third-party testing framework.
- Example test using `pytest` in `test_calculation.py`:

  ```python
  def add(x, y):
      return x + y

  def test_add():
      assert add(10, 5) == 15
      assert add(-1, 1) == 0
      assert add(-1, -1) == -2
  ```

## Running Tests

- **With `unittest`**:
  ```bash
  python -m unittest test_calculation.py
  ```

- **With `pytest`**:
  ```bash
  pytest test_calculation.py
  ```

## Best Practices

- Write tests for every new function or feature.
- Run tests locally before pushing changes to the repository.
- Use continuous integration (CI) tools to automate testing on different environments.

## Contributing

Contributions that improve existing tests, add new test cases, or enhance documentation are welcome. Please fork the repository, make your changes, and submit a pull request.

## License

This project is licensed under the MIT License. See the LICENSE file for more details.
