---

# De Novo Molecular Design Enabled by Direct Preference Optimization and Curriculum Learning

本仓库为 **ECML-PKDD 2025** 论文 *"De Novo Molecular Design Enabled by Direct Preference Optimization and Curriculum Learning"* 的代码实现。

---

## 环境配置

### 方法一：通过 `environment.yml` 创建

```bash
conda env create -f environment.yml
```

然后手动修改以下文件：

* 路径：`lib/python3.10/site-packages/guacamol/utils/chemistry.py`

  * **删除**：

    ```python
    from scipy import histogram
    ```
  * **修改**：将所有 `histogram` 替换为 `np.histogram`

### 方法二：直接解压已有环境

```bash
tar -xzf molDPO.tar.gz -C ~/miniconda3/envs/molDPO
~/miniconda3/envs/molDPO/bin/conda-unpack
conda activate molDPO
```

> ⚠️ 请将 `miniconda3` 替换为你实际的 conda 安装路径。

---

## 使用方法

运行主程序：

```bash
python DPO_guacamol.py
```

* 如果启用课程学习（Curriculum Learning）：

  * 第一个课程需设置参数 `first_course=True`
  * 后续课程需设置 `first_course=False`

---

## 致谢

框架代码（如 `model.py`、`vocabulary.py`）来源于对比基线方法 **[MolRL-MGPT](https://github.com/HXYfighter/MolRL-MGPT)**。

---

## 联系方式

如有问题，欢迎通过邮件联系我。

---