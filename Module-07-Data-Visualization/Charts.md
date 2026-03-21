
## Overview
In this module, I created different types of visualizations using various tools to represent data effectively. The focus was on selecting the right chart, using appropriate tools, and communicating insights clearly through visuals.

---

### Bar Chart (Excel)
- Used to compare values across different categories
- Tool: Excel
- X-axis: Categories
- Y-axis: Values
- Observation: Helped identify highest and lowest performing categories

---

### Line Chart (Excel – Forecasting)
- Used to visualize trends over time
- Tool: Excel
- X-axis: Time
- Y-axis: Values
- Observation: Showed increasing/decreasing trends and future predictions

---

### Correlation Heatmap (Seaborn)
- Used to identify relationships between variables
- Tool: Python (Seaborn)
- Observation: Highlighted strong positive and negative correlations

Example:
```python
import seaborn as sns
import matplotlib.pyplot as plt

sns.heatmap(df.corr(), annot=True)
plt.show()
