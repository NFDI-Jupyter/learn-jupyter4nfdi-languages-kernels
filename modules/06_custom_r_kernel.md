# Optional: register an R kernel


## Learning objectives


- Install and know how to use `ipykernel`.
- Create an R custom kernel.
- Register the environment as a Jupyter kernel.

## IRkernel

For R, a commonly used Jupyter kernel is `IRkernel`.
If IRkernel is not installed, install it first:

```r
install.packages("IRkernel")
```

If IRkernel is installed, start R and register it for your user account:

```r
IRkernel::installspec(user = TRUE)
```

To make the kernel easier to distinguish from other R kernels, give it a specific name and display name:

```r
IRkernel::installspec(
  user = TRUE,
  name = "r-project",
  displayname = "R (project)"
)
```

The kernel should then appear in Jupyter's kernel selector.


## Multiple R kernels

Just as with Python, several R kernels can coexist if they have different kernel names.

This can be useful when you maintain:

- different R versions;
- different project libraries;
- teaching and research environments with different dependencies.

