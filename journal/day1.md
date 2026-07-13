# Day 1

Date

2026-07-12

---

## Goal

Set up a professional Modern C++ development environment and begin the design phase of the exchange engine.

---

## Completed

### Environment

- Created GitHub repository
- Installed Modern C++ toolchain
- Configured CMake
- Successfully compiled and executed the first program

Output

```
Exchange Engine Started
```

---

## System Design

Today focused entirely on understanding the business domain before writing code.

Topics explored

- What is an Order Book?
- Matching Engine responsibilities
- Price-Time Priority
- Partial Fills
- Order lifecycle
- Difference between Order and Trade

---

## Important Decisions

### Orders and Trades are different objects

Reason

A single order can generate multiple trades.

Status

Accepted

---

### Price-Time Priority

Matching priority is

1. Better price
2. Earlier timestamp

Status

Accepted

---

### Partial Fill

Orders remain in the book until their remaining quantity reaches zero.

Status

Accepted

---

### Price Representation

Do not use floating-point numbers.

Prices will be represented as scaled integers.

Example

```
$10.35

↓

1035
```

Reason

Avoid floating-point precision errors.

Status

Accepted

---

## What I Learned

Today I realized software engineering begins with understanding the business problem, not writing code.

I also learned that professional exchanges do not simply store a list of orders. They organize orders according to Price-Time Priority and carefully separate the concepts of Orders and Trades.

Another important lesson was that financial systems generally avoid floating-point numbers for representing money because precision errors can lead to incorrect comparisons and calculations.

---

## Challenges

At first, I assumed Orders should contain trade information.

After discussing several examples involving partial fills, I realized a single Order can generate multiple Trades.

This led to separating the Order and Trade domain models.

---

## Next Goal

Design the Order class.

Topics to explore

- Order fields
- enum class
- Constructors
- Header vs Source files
- Encapsulation
- const correctness
- Scaled integer implementation