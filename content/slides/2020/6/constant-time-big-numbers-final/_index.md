+++
title = "Constant Time Big Numbers Final"
outputs = ["Reveal"]
date = "2021-06-22T18:49:02+02:00"
+++

### Constant Time Big Numbers
### (For Go)

Lúcás C. Meier

Supervisor: Prof. Bryan Ford

---

### Overview

- Big Numbers?
- Timing Attacks?
- Go?
- Safenum (Our Work)
- Further Work

---

{{% section %}}

### Big Numbers

![](./res/1.png)

---

### Useful in Cryptography

- $\mathbb{N}$ (Natural Numbers)
- $\mathbb{Z}/N \mathbb{Z}$ (Modular Arithmetic)
- $\mathbb{F}_p$ (Prime Fields)

---

### RSA

Public key $(e, N)$, encrypt $m$ with:

$$
m^e \mod N
$$

$N \approx 2048$ bits

---

### Too Big!

![](./res/5.png)

---

### Elliptic Curve Cryptography

![](./res/6.jpg)

---

### Prime Fields!

$\mathbb{Z}/p\mathbb{Z}$

for example:

$$
p = 2^{255} - 19
$$

Somewhat big

---

### Implementation Strategies

- Hand-written implementation
- Generated (e.g. FiatCrypto)
- Dynamic (`big.Int`, our library)

{{% /section %}}

---

{{% section %}}

![](./res/2.png)

---

### Implementations in Theory

![](./res/8.jpeg)

---

### Implementations in Practice

![](./res/7.jpg)

---

### Timing

![](./res/13.png)

---

### Guessing Passwords

![](./res/10.png)

---

![](./res/11.png)

---

![](./res/12.png)

---

### Side-Channel Overview

Subtle Behavior:

- Caches
- Branch Prediction

---

### Further Information

![](./res/14.png)

{{% /section %}}

---

### Threat Model

- Loops leak the number of iterations
- Memory accesses leak addresses
- Branching leaks condition

---

{{% section %}}

### Go

![](./res/4.jpg)

---

### `big.Int`

![](./res/9.png)

---

![](./res/3.png)

---

### Not Constant-Time

![](./res/15.png)

---

### Why? Bad Algorithms

![](./res/16.png)

---

### Why? Padding

![](./res/17.png)

---

### in `go/crypto`

- Extensively in **RSA**, and **DSA**
- **ECC**: Elliptic Curve interface uses `big.Int`
- Only **P384** uses `big.Int` for field arithmetic

---

### Mitigations

In RSA: *blinding*:

Instead of:

$$
c^d \mod N
$$

Calculate:

$$
\frac{1}{r} (c \cdot r^e)^d \mod N
$$

{{% /section %}}

---

{{% section %}}

### Our Library

![](./res/17.png)

---

![](./res/18.png)

---

### Constant-Time Choice

![](./res/8.gif)

{{% /section %}}

---

{{% section %}}

### Performance: Operations

![](./res/20.png)
![](./res/21.png)

---

### Performance: Cryptography

![](./res/22.png)

{{% /section %}}

---

### Patching RSA

![](./res/19.png)

---

{{% section %}}

### Timeline

![](./res/23.png)

---

### The most important artifact?

---

### Understanding!

![](./res/24.jpg)

{{% /section %}}

---

### Further Work

- Verifying security properties
- Improving performance: Assembly?
- More scenarios: **ECC**, **PQC**?

---

### In Summary

![](./res/7.jpg)

We made an alternative to `big.Int` for Cryptography.
It's only 2x slower.