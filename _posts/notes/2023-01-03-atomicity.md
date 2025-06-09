---
layout: post
title: "Atomicity"
date: 2023-01-03
categories: notes
tags: [programming, database, concepts]
---

Atomicity refers to the smallest, irreducible building block material. The core concept is that an atomic operation is one that cannot be divided further.

In computing, particularly in database systems, atomicity is one of the ACID properties. It guarantees that each transaction is treated as a single "unit", which either succeeds completely or fails completely.

## Examples in Different Contexts

### Databases
In database operations, atomicity ensures that if one part of a transaction fails, the entire transaction fails and the database state is left unchanged.

### Concurrent Programming
In concurrent programming, an atomic operation is one that appears to the rest of the system to occur instantaneously.

### Chemistry
In chemistry, an atom is the smallest unit of a chemical element that can exist.
