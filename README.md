# Tymbert Environment Setup

This repository provides a Conda environment configuration file (`environment.yml`) for setting up the `tymbert` environment. Follow the steps below to install and configure it correctly on your system.

## Prerequisites

- Install [Miniconda](https://docs.conda.io/en/latest/miniconda.html) or [Anaconda](https://www.anaconda.com/products/distribution)
- Ensure Conda is added to your system's PATH

## Installation Steps

1. **Clone the Repository**
   ```bash
   git clone <your-repo-url>
   cd <your-repo-directory>
   ```

2. **Create the Conda Environment**
   Run the following command to create the `tymbert` environment from the `environment.yml` file:
   ```bash
   conda env create -f environment.yml
   ```

3. **Update the Environment Prefix**
   The `environment.yml` file may contain an absolute path under the `prefix` field, which may not match your system's Conda installation directory. To fix this:
   
   - Open the `environment.yml` file in a text editor
   - Locate the `prefix:` field at the bottom of the file (if present)
   - Change it to your own Conda environment path, which can be found using:
     ```bash
     conda info --envs
     ```
   - Alternatively, create the environment without using the prefix by running:
     ```bash
     conda env create --name tymbert --file environment.yml
     ```

4. **Activate the Environment**
   ```bash
   conda activate tymbert
   ```

5. **Verify Installation**
   Check that the necessary dependencies are installed:
   ```bash
   conda list
   ```

## Updating the Environment
If you make changes to `environment.yml` and need to update the existing environment:
```bash
conda env update --name tymbert --file environment.yml --prune
```

## Deactivating and Removing the Environment
To deactivate the environment:
```bash
conda deactivate
```
To remove the environment completely:
```bash
conda env remove --name tymbert
```

## License
This project is licensed under the MIT License. See the `LICENSE` file for details.

