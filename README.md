# coalitiestatengeneraal

Create the Conda environment used by the deployment/build. `environment.yml` includes the required PyPI packages so they will be installed during environment creation.

To create the environment locally (macOS / zsh):

```bash
# create environment from the environment.yml
conda env create -f environment.yml

# activate it
conda activate my-dashboard-env
```

Notes:
- The `environment.yml` contains a `pip:` section listing `parliamentarch` and `ipywidgets` so they are available without pip installing from within the notebook.
- If your deployment uses a different builder (e.g., Docker, Binder), ensure it consumes this `environment.yml` or add equivalent pip installs in the build step.
