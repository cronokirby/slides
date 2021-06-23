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

---

### Guessing Passwords

---

### Side-Channel Overview

{{% /section %}}

---

### Threat Model

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

---

### in `go/crypto`

---

### End Section

{{% /section %}}

---

### Our Library

---

### Performance

---

### `go/crypto`

---

### Further Work

---

### Final Slide
