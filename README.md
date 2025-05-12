# One Hot Encoding in Machine Learning

This notebook explains and demonstrates the use of **One Hot Encoding**, a popular method to handle categorical variables by converting them into binary vectors.

---

## 🧠 What is One Hot Encoding?

One Hot Encoding transforms each categorical value into a **new column**, where each column represents a category and contains binary values:
- `1` if the row belongs to that category
- `0` otherwise

For example, a feature `Color` with values `Red`, `Blue`, `Green` becomes:

| Color_Red | Color_Blue | Color_Green |
|-----------|------------|-------------|
| 1         | 0          | 0           |
| 0         | 1          | 0           |
| 0         | 0          | 1           |

---

## ✅ When to Use

- Categorical features with **no ordinal relationship** (e.g., `Country`, `City`, `Product`)
- Works well with **linear models**, **neural networks**, and **distance-based models**

---

## ⚠️ Caution

- Can lead to **high-dimensional data** if the category count is large
- Avoid on high-cardinality columns unless necessary

---

## 🛠️ Tools Used

- `pandas.get_dummies()`
- `sklearn.preprocessing.OneHotEncoder`

---

## 🚀 Example Usage

### Using pandas:
```python
encoded_df = pd.get_dummies(df, columns=['Category'])
