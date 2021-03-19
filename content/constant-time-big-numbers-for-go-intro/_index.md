+++
title = "My presentation"
outputs = ["Reveal"]
+++

### Constant Time Big Numbers
### (For Go)

Lúcás C. Meier

Supervisor: Bryan Ford

--- 

### Overview 8^)

- I tell you what I'm going to say
- I say it
- I tell you what I said

---

### Overview

- Big Numbers?
- Constant Time?
- Solutions?
- Project's Approach + Status

---

{{% section %}}

### Humans use Big Numbers!

![](./res/5.png)

---
### Big Numbers

![](./res/1.png)

{{% /section %}}

---

{{% section %}}


### Making rocks think

![](./res/4.jpg)

---


### Schoolbook Arithmetic

![](./res/6.png)


---

### Multiple Digits

![](./res/7.png)


---

![](./res/17.png)

---

### Body Parts

Digits: $\\{0, 1, \ldots, 9\\}$

Limbs: $\\{0, 1, \ldots, 2^{W} - 1\\}$

{{% /section %}}

---

{{% section %}}

### Timing Attacks

![](./res/9.png)

---

### Leaking Length

![](./res/18.png)

---

### Leaking Values

![](./res/10.png)

---

### IRL
![](./res/13.png)


{{% /section %}}

---

{{% section %}}

### Solutions

![](./res/15.png)

---

# Leave Zeros Alone!

---

### Announced Length

![](./res/16.png)

---

### Better Algorithms

Rules of thumb:

- No conditionals (sort of)
- Loop only on announced length

{{% /section %}}

---

### Current Work

A library:

https://github.com/cronokirby/safenum

- Restricted but complete API
- all constant time (I hope)
- Not necessarily optimal

---

### Future Goals

- Work with ProtonMail: toward production readiness
- Living in Go's standard library (fork)
- Upstreaming to Go?

---

### Questions?

---

![](./res/3.png)
