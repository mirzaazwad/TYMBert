# Tymbert Environment Setup

## Table of Contents

- [Tymbert Environment Setup](#tymbert-environment-setup)
- [Prerequisites](#prerequisites)
- [Installation Steps](#installation-steps)
- [Updating the Environment](#updating-the-environment)
- [Deactivating and Removing the Environment](#deactivating-and-removing-the-environment)
- [Jupyter Use](#jupyter-use)
- [Datasets](#datasets)
- [Additional References](#additional-references)
- [License](#license)

This repository provides a Conda environment configuration file (`environment.yml`) for setting up the `tymbert` environment. Follow the steps below to install and configure it correctly on your system.

## Prerequisites

- Install [Miniconda](https://docs.conda.io/en/latest/miniconda.html) or [Anaconda](https://www.anaconda.com/products/distribution)
- Ensure Conda is added to your system's PATH

## Installation Steps

1. **Clone the Repository**

   ```bash
   git clone https://github.com/mirzaazwad/TYMBert.git
   cd TYMBert
   ```

````

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

## Jupyter Use

After this environment is setup, use this environment as your kernel and you can use it via Jupyter Notebook or VSCode with the Jupyter extension.

## Datasets

| Dataset Name                | Description                                                              | Link                                                                                              |
| --------------------------- | ------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------- |
| SPStudy                     | A dataset for spam research, containing various studies and data points. | [GitHub - SPStudy](https://github.com/smspamresearch/spstudy/tree/main)                           |
| SMS Spam Collection Dataset | A dataset containing SMS messages labeled as spam or ham.                | [Kaggle - SMS Spam Collection](https://www.kaggle.com/datasets/uciml/sms-spam-collection-dataset) |

## Additional References

Quantization Logic and Code was used with the help of [GitHub - BERT-Quantization](https://github.com/srimoyee1212/BERT-Quantization/tree/main) by srimoyee1212

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.

