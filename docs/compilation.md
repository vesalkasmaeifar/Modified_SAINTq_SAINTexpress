# **Compiling SAINTq & SAINTexpress from Source**

## **Overview**
This document provides step-by-step instructions to compile **SAINTq** and **SAINTexpress** from source. The compilation process is straightforward—simply run `make -j` in the main directory of each software, and the compiled binaries will be generated in the `bin/` directory.

---

## **1. Clone the Repository**
If you haven’t already, clone the repository to your local machine:
```bash
git clone https://github.com/vesalkasmaeifar/Modified_SAINTq_SAINTexpress.git
cd Modified_SAINTq_SAINTexpress
```

---

## **2. Compile SAINTq**
Navigate to the **SAINTq** directory and run:
```bash
cd SAINTq
make -j
```
This will compile the modified SAINTq source code.  
The compiled binaries will be located in the **`bin/`** directory.

---

## **3. Compile SAINTexpress**
Navigate to the **SAINTexpress** directory and run:
```bash
cd ../SAINTexpress
make -j
```
This will compile the modified SAINTexpress source code.  
The compiled binaries will be located in the **`bin/`** directory.

---


For further details, see [`docs/modifications.md`](modifications.md) for information on changes made to the original SAINTq and SAINTexpress source code.
