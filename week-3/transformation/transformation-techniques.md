# Feature Transformation Techniques

## 1. Introduction

Feature transformation is the process of changing the format or
distribution of data so that Machine Learning algorithms can process
it effectively.

In the Apparel & Textiles industry, datasets can contain numerical,
categorical, text, image and time-based information.

Different types of data require different transformation techniques.

The main techniques covered in this document are:

- Normalization
- Standardization
- Log transformation
- Categorical encoding
- Binning
- Polynomial features
- Dimensionality reduction
- Feature scaling

---

# 2. Why Feature Transformation Is Important

Feature transformation can help:

- Put numerical variables on comparable scales
- Improve optimization
- Reduce the effect of extreme values
- Convert categorical information into numerical form
- Improve model compatibility
- Reduce dimensionality
- Improve model stability
- Make patterns easier for some algorithms to learn

Not every transformation is required for every Machine Learning model.

The appropriate technique depends on the dataset and algorithm.

---

# 3. Feature Scaling

Feature scaling changes numerical variables to comparable ranges.

### Example

Suppose a dataset contains:

```text
Price = ₹1,500
Sales = 25
Discount = 20
