---
title: Blog with Jupyter Notebooks! (version02)
date: '2023-11-21'
summary: Easily blog from Jupyter notebooks! (version02)
---

---
jupyter:
  kernelspec:
    display_name: Python 3 (ipykernel)
    language: python
    name: python3
  language_info:
    codemirror_mode:
      name: ipython
      version: 3
    file_extension: .py
    mimetype: text/x-python
    name: python
    nbconvert_exporter: python
    pygments_lexer: ipython3
    version: 3.9.12
  nbformat: 4
  nbformat_minor: 5
---

::: {#c52e0467 .cell .code execution_count="1"}
``` python
from sklearn import datasets
iris = datasets.load_iris()
```
:::

::: {#c432c81d .cell .code execution_count="4"}
``` python
import matplotlib.pyplot as plt
_, ax = plt.subplots()
scatter = ax.scatter(iris.data[:, 0], iris.data[:, 1], c=iris.target)
ax.set(xlabel=iris.feature_names[0], ylabel=iris.feature_names[1])
_ = ax.legend(scatter.legend_elements()[0], iris.target_names, loc="lower right", title="Classes")
```

::: {.output .display_data}
![](vertopal_d6668e6edd8043e585e5b4562dc883f3/f796dbbe402c19e6fbccb3c0cbe25d1d8e0e1f89.png)
:::
:::

::: {#a742be64 .cell .code execution_count="5"}
``` python
# unused but required import for doing 3d projections with matplotlib < 3.2
import mpl_toolkits.mplot3d  # noqa: F401

from sklearn.decomposition import PCA

fig = plt.figure(1, figsize=(8, 6))
ax = fig.add_subplot(111, projection="3d", elev=-150, azim=110)

X_reduced = PCA(n_components=3).fit_transform(iris.data)
ax.scatter(
    X_reduced[:, 0],
    X_reduced[:, 1],
    X_reduced[:, 2],
    c=iris.target,
    s=40,
)

ax.set_title("First three PCA dimensions")
ax.set_xlabel("1st Eigenvector")
ax.xaxis.set_ticklabels([])
ax.set_ylabel("2nd Eigenvector")
ax.yaxis.set_ticklabels([])
ax.set_zlabel("3rd Eigenvector")
ax.zaxis.set_ticklabels([])

plt.show()
```

::: {.output .display_data}
![](vertopal_d6668e6edd8043e585e5b4562dc883f3/5ebf427a7a90faa17d588773642d2096d0ec5507.png)
:::
:::
