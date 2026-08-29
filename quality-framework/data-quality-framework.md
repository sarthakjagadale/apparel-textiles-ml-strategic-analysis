# Data Quality Framework

## Objective

The purpose of this framework is to evaluate whether collected data is
reliable and suitable for future Machine Learning applications in the
Apparel & Textiles industry.

---

## 1. Accuracy

Accuracy measures whether the data correctly represents the real-world
value.

### Example

Compare textile export values with official published totals.

### Checks

- Compare with authoritative sources
- Identify incorrect values
- Investigate abnormal records

---

## 2. Completeness

Completeness measures how much required information is available.

### Example

Check whether important fields such as:

- Date
- Product category
- Country
- Export value
- Quantity

contain missing values.

### Target

Core fields should generally have at least 95% completeness unless
there is a documented reason for lower coverage.

---

## 3. Consistency

Consistency ensures that the same information follows the same format.

### Examples

Incorrect:

```text
India
IND
ind
