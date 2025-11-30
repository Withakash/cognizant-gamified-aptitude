# Problem Statement 1

Alice likes collecting soft toys. Every day, she adds one soft toy to her collection more than she did the day before.

* She adds **1** soft toy on the **first day**
* **2** soft toys on the **second day**
* **3** soft toys on the **third day**, and so on

A day is considered **special** if the **total number of soft toys collected up to that day** is **divisible by 5**.

You are given an integer **N**, representing the total number of days.
Your task is to **find and return the count of special days** between **1 and N (inclusive)**.

---

## Input Specification

* **input1:** An integer **N**, representing the number of days Alice collects soft toys.

## Output Specification

* Return an integer value representing the **count of special days** between **1 and N**.

---

## Example 1

**Input:**

```
6
```

### Working

| Day | Total Soft Toys | Divisible by 5? |
| --- | --------------- | --------------- |
| 1   | 1               | No              |
| 2   | 3               | No              |
| 3   | 6               | No              |
| 4   | 10              | Yes             |
| 5   | 15              | Yes             |
| 6   | 21              | No              |

**Special Days:** 4, 5
**Count:** 2

**Output:**

```
2
```

---

## Example 2

**Input:**

```
10
```

**Output:**

```
4
```

---

# Problem Statement 2# Problem Statement 2

You are a teacher organizing a field trip for your students. You have a class of **N students**, and you want to divide them into **two groups** for the trip.

However, there is a **special requirement**:

* **One group must contain only students with even-numbered IDs**
* **The other group must contain only students with odd-numbered IDs**
* **Both groups must be of the same length**

Your task is to find and return an integer value representing the **maximum number of students** that can be included **in both groups**.

---

## Input Specification

* **input1:** An integer value **N** representing the total number of students.
* **input2:** An integer array containing the **IDs of the students**.

---

## Output Specification

Return an integer value representing the **maximum number of students** that can be included in both groups.

---

## Example 1

**Input:**

```
input1: 4
input2: {5, 2, 3, 6}
```

### Explanation

There are four students with IDs {5, 2, 3, 6}.

* Even IDs: {2, 6} → count = 2
* Odd IDs: {5, 3} → count = 2

Both groups can have **2 students each**, which is the maximum possible.

**Output:**

```
2
```

---

## Example 2

**Input:**

```
input1: 3
input2: {1, 2, 1}
```

### Explanation

* Even IDs: {2} → count = 1
* Odd IDs: {1, 1} → count = 2

The groups must be of equal size, so the maximum possible group size is **1**.

**Output:**

```
1
```


