# Exchange Engine

> Building a production-quality electronic exchange in Modern C++ from scratch.

## Overview

Exchange Engine is a long-term learning project whose goal is to build a simplified electronic exchange while learning modern C++ the same way professional systems engineers build production software.

This project is intentionally developed incrementally:

Design → Implementation → Testing → Benchmarking → Optimization

The emphasis is on understanding engineering tradeoffs instead of simply producing working code.

---

## Project Goals

Technical goals

- Learn Modern C++20
- Learn low-latency system design
- Learn concurrent programming
- Learn performance optimization
- Learn software architecture
- Learn financial exchange fundamentals

Career goals

Build a project that demonstrates the engineering skills expected by quantitative trading firms such as:

- Citadel
- Citadel Securities
- Jane Street
- Hudson River Trading
- IMC
- Optiver
- Two Sigma

---

## Current Status

Current Phase

🟢 Phase 1 — Domain Modeling

Current Progress

- ✅ Repository created
- ✅ Modern CMake project configured
- ✅ Build pipeline working
- ✅ First executable running
- ✅ Exchange architecture drafted
- ✅ Order book behavior designed
- ✅ Matching rules documented
- ✅ Price-Time Priority understood
- ✅ Partial Fill behavior designed
- ✅ Scaled Integer price representation selected

Currently Working On

Designing the `Order` class.

Next Milestone

Implement `Order.h` and `Order.cpp`.

---

## Repository Structure

```
exchange-engine/

├── benchmark/
├── docs/
├── include/
├── journal/
├── src/
├── tests/
├── CMakeLists.txt
└── README.md
```

---

## Roadmap

### Phase 0

- [x] Project setup
- [x] CMake
- [x] Build system

### Phase 1

- [ ] Order
- [ ] Trade
- [ ] Order Book
- [ ] Matching Engine

### Phase 2

- [ ] Complete Order Book
- [ ] Market Orders
- [ ] IOC
- [ ] FOK

### Phase 3

- [ ] TCP Networking
- [ ] Multiple Clients

### Phase 4

- [ ] Multithreading

### Phase 5

- [ ] Performance Optimization

### Phase 6

- [ ] Risk Engine

### Phase 7

- [ ] Market Data

### Phase 8

- [ ] FIX Gateway

---

## Documentation

Project documentation can be found inside `/docs`.

Current documents

- order-book.md
- order.md
- architecture.md

Engineering journal

- journal/day01.md

---

## Engineering Principles

- Correctness before optimization
- Readability before cleverness
- Measure before optimizing
- Benchmark every optimization
- Document every major design decision

---

## Long-Term Goal

By the completion of this project, I should be comfortable discussing:

- Modern C++
- Matching Engines
- Low Latency Systems
- Concurrent Programming
- Memory Management
- Performance Optimization
- Design Tradeoffs

without relying on memorized answers.