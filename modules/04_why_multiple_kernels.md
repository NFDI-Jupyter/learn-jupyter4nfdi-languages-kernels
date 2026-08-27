# Why use more than one kernel?

A kernel can represent is related to a programming language, but it can also be related to a particular software environment.

For example, you can have kernels:

- Python (default)
- Python (project-a)
- Python (teaching)
- Python (legacy-analysis)

All of them execute Python, but they can use different environments, that is have access to different software installed.

Multiple kernels can help you work with:

- different package sets;
- different package versions;
- project-specific dependencies;
- experimental packages without changing your default environment;
- teaching environments prepared with everything learners need;
- older projects that depend on versions that would conflict with newer work.

Project A needs:

```text
pandas 2.x
scikit-learn 1.7
```

Project B uses code written for much older dependency versions. Trying to put all requirements into one environment can create dependency conflicts.
So that is why a different kernel is useful. You can maintain two environments and register each as a separate kernel. When opening a notebook, choose the relevant kernel. A kernel name visible in JupyterLab should help users understand what to select.
`Python (survey-analysis)` is more useful than `env3`.

