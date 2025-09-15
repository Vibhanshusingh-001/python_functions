
###  1. `sys`

* **Purpose**: Provides access to variables and functions used or maintained by the Python interpreter.
* **Common Uses**:

  * Access command-line arguments: `sys.argv`
  * Exit the program: `sys.exit()`
  * Get the Python version: `sys.version`
* **Example**:

  ```python
  import sys
  print(sys.version)
  sys.exit()
  ```

---

###  2. `subprocess`

* **Purpose**: Allows running external system commands or other programs from within Python code.
* **Common Uses**:

  * Execute shell commands
  * Capture the output of commands
  * Replace older modules like `os.system()`
* **Example**:

  ```python
  import subprocess
  result = subprocess.run(['ls', '-l'], capture_output=True, text=True)
  print(result.stdout)
  ```

---

### 3. `glob`

* **Purpose**: Provides a way to retrieve files and directories matching specific patterns using wildcard characters.
* **Common Uses**:

  * File search using patterns (e.g., all `.csv` files)
  * Path matching
* **Example**:

  ```python
  import glob
  csv_files = glob.glob('data/*.csv')
  print(csv_files)
  ```

---

###  4. `pandas`

* **Purpose**: Powerful library for data manipulation and analysis.
* **Key Features**:

  * Provides DataFrame structure for tabular data
  * Handles missing data, merging, grouping, and statistical operations
  * Import/export from various formats (CSV, Excel, SQL, etc.)
* **Example**:

  ```python
  import pandas as pd
  df = pd.read_csv('data.csv')
  print(df.head())
  ```

---

###  5. `os`

* **Purpose**: Provides a way to interact with the operating system for tasks such as reading/writing files, handling directories, and working with environment variables.
* **Common Uses**:

  * Create directories: `os.mkdir()`
  * Get environment variables: `os.getenv()`
  * File/path operations
* **Example**:

  ```python
  import os
  cwd = os.getcwd()
  print(f'Current working directory: {cwd}')
  os.mkdir('new_folder')
  ```

---

###  6. `time`

* **Purpose**: Useful for time-related tasks like delays, measuring execution time, timestamps.
* **Common Uses**:

  * Delay execution: `time.sleep()`
  * Measure execution time
  * Get current time
* **Example**:

  ```python
  import time
  start = time.time()
  time.sleep(2)
  end = time.time()
  print(f'Elapsed time: {end - start} seconds')
  ```

---

###  7. `numpy`

* **Purpose**: The fundamental package for scientific computing in Python. Handles large, multi-dimensional arrays and matrices, along with a collection of mathematical functions.
* **Key Features**:

  * Efficient array computations
  * Linear algebra, Fourier transforms, random numbers
* **Example**:

  ```python
  import numpy as np
  arr = np.array([1, 2, 3, 4])
  print(arr.mean())  # Output: 2.5
  ```

---

###  8. `platform`

* **Purpose**: Provides information about the underlying system/platform (OS, version, architecture).
* **Common Uses**:

  * Check OS type
  * Detect Python version
  * Retrieve hardware details
* **Example**:

  ```python
  import platform
  print(platform.system())  # e.g., 'Windows', 'Linux'
  print(platform.release())  # e.g., '10'
  ```

---

###  Summary:

These packages cover key areas:

* **System interaction**: `sys`, `os`, `subprocess`
* **File management**: `glob`, `os`
* **Time management**: `time`
* **Data handling**: `pandas`, `numpy`
* **Platform info**: `platform`
