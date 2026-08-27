# Notebook, kernel, and environment

## Learning goal

Distinguish between 
- the notebook interface, 
- the kernel, 
- and the software environment.


The notebook interface is where you write code and Markdown; run cells and see outputs. The kernel is the process that executes code.
For example:
- a Python kernel executes Python;
- an R kernel executes R;
- a Julia kernel executes Julia.

The kernel also holds the current computational state, such as variables that have already been created.

The environment contains the installed software available to the kernel, such as:
- installed packages;
- package versions;
- libraries;
- command-line tools;
- sometimes a particular version of the programming language itself.

**Note**
Two kernels can both run Python but use different Python environments.
For example:

- Project A might contain `pandas==2.x`;
- Project B might contain an older package version.

So changing a kernel can change:
1. the programming language;
2. the software environment;
3. or both.

