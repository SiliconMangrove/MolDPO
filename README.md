---

# De Novo Molecular Design Enabled by Direct Preference Optimization and Curriculum Learning

This repository contains the code implementation for the **ECML-PKDD 2025** paper *"De Novo Molecular Design Enabled by Direct Preference Optimization and Curriculum Learning"*.

---

## Environment Setup

### Method 1: Create via `environment.yml`

```bash
conda env create -f environment.yml
```

Then manually modify the following file:

* Path: `lib/python3.10/site-packages/guacamol/utils/chemistry.py`

  * **Delete**:

    ```python
    from scipy import histogram
    ```
  * **Modify**: Replace all occurrences of `histogram` with `np.histogram`

### Method 2: Directly unpack the prebuilt environment

Download the conda-packaged environment from [environment link](https://drive.google.com/file/d/1jg6md4Cwv1C7dHXO8loggGJjo0d6n_BA/view?usp=sharing).

```bash
tar -xzf molDPO.tar.gz -C ~/miniconda3/envs/molDPO
~/miniconda3/envs/molDPO/bin/conda-unpack
conda activate molDPO
```

> ⚠️ Please replace `miniconda3` with your actual conda installation path.

---

## Usage

Run the main program:

```bash
python DPO_guacamol.py
```

* If curriculum learning is enabled:

  * The first course should be set with parameter `first_course=True`
  * Subsequent courses should be set with `first_course=False`

---

## Acknowledgements

Framework code (such as `model.py`, `vocabulary.py`) is adapted from the baseline method **[MolRL-MGPT](https://github.com/HXYfighter/MolRL-MGPT)**.

---

## Contact

If you have any questions, feel free to contact me via email.

---

