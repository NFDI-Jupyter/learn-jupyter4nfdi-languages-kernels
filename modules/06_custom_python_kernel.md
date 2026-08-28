# Create a custom Python kernel

## Learning objectives

- Create a Python virtual environment.
- Install `ipykernel`.
- Register the environment as a Jupyter kernel.



A custom Python kernel is useful when you want a notebook to run in a specific Python environment.

The workflow is:

**1: create a virtual environment**

Open a terminal in JupyterLab and run:

```bash
python3 -m venv ~/test-kernel
```

Activate it:

```bash
source ~/test-kernel/bin/activate
```


**2: install `ipykernel`**

```bash
python -m pip install --upgrade pip
python -m pip install ipykernel
```

You can now install any additional packages required by your project into the same environment.

For example:

```bash
python -m pip install pandas
```

**3: register the kernel**

```bash
python -m ipykernel install --user   --name test-kernel   --display-name "Python (test-kernel)"
```

The two names have different purposes:

- `--name` is Jupyter's internal kernelspec name;
- `--display-name` is the label shown to users in JupyterLab.

Use a unique and meaningful `--name`.

**4: select the custom new kernel**

Return to a notebook and choose the new kernel from the kernel selector.

If it does not appear immediately, refresh JupyterLab.

## Test the environment

In a notebook using **Python (test-kernel)**, run:

```python
import sys
print(sys.executable)
```

The path should point to the Python executable inside your `~/test-kernel` environment.


