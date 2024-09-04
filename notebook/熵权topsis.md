# 熵权法计算权重
1. 数据准备
2. 正向化和标准化
3. 非负平移
4. 计算对象占该列的比重
5. 计算每一项指标的熵值
6. 计算差异系数
7. 计算权重
## 正向化和标准化方法 --极差法
正向指标公式：
$$
            Z'{ij} = \tfrac{x_{ij}-x_{j}^{min}}{x_{j}^{max}-x_{j}^{min}}
$$
负向指标：
$$
            Z'{ij} = \tfrac{x_{j}^{max} - x_{ij}}{x_{j}^{max}-x_{j}^{min}}
$$
适度指标：
$$
\begin{gathered}z_{ij}^{\prime}=\begin{cases}1-\frac{a-x_{ij}}{\max(a-x_j^{\min}, x_j^{\max}-b)}&, x_{ij}<a\\1&, a\leq x_{ij}\leq b\\1-\frac{x_{ij}-b}{\max(a-x_j^{\min}, x_j^{\max}-b)}&, x_{ij}>b\end{cases}\end{gathered}
$$

## 计算比重
$$P_{ij}=z_{ij}/\sum_{i=1}^nz_{ij},(j=1,2,\cdots,m)$$

## 计算熵值
$$E_j=-\dfrac{1}{\ln n}\sum_{i=1}^nP_{ij}\ln P_{ij},(j=1,2,\cdots,m)$$ 
* n为样本数，m为指标数
## 计算差异系数
$$G_j=1-E_j$$

## 计算权重
$$W_j=\frac{G_j}{\sum_{j=1}^mG_j}$$