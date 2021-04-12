+++
title = "Constant Time Big Numbers 2"
outputs = ["Reveal"]
date = "2021-04-11T10:36:29+02:00"
+++

### Constant Time Big Numbers 2:
### Electric Boogaloo

Lúcás C. Meier

Supervisor: Bryan Ford

---

### Overview

- Performance improvements
- Constant-Time Ceiling
- A day in my shoes: Exponentiation

---

{{% section %}}

### Performance Improvements

---

### Notable Techniques

- Limb by Limb modular reduction
- **Montgomery Multiplication**

---

### The Ceiling

{{% /section %}}

---

### In my shoes

---

{{% section %}}

### Exponentiation

$$x^d \mod m$$

---

### Large Results

---

### Very Naive Algorithm

```go
func ModExp(x, d)
```

---

### Binary Exponentiation

---

### Timing Leak

{{% /section %}}

---

{{% section %}}

### Making Things Constant-Time

{{% /section %}}

---

{{% section %}}

# Improving Multiplication

{{% /section %}}

---

### Questions
