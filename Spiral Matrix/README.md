# Spiral Matrix Traversal in Java

## 📌 Introduction
This project demonstrates how to **print a 2D matrix in spiral order** using Java.  
The spiral order means starting from the top-left corner of the matrix, traversing the outer boundary, and then moving inward layer by layer until all elements are printed.

Example spiral traversal:

Matrix:
1 2 3 4
5 6 7 8
9 10 11 12
13 14 15 16

Spiral Order:
1 → 2 → 3 → 4 → 8 → 12 → 16 → 15 → 14 → 13 → 9 → 5 → 6 → 7 → 11 → 10

---

## 🧠 How I Designed the Logic
I broke the traversal into **four directions** inside a loop:

1. **Top Row (Left → Right)**  
   Print the first row from the current starting column to the ending column.

2. **Right Column (Top → Bottom)**  
   Print the last column from the next row down to the ending row.

3. **Bottom Row (Right → Left)** *(only if rows remain)*  
   Print the bottom row from right to left.

4. **Left Column (Bottom → Top)** *(only if columns remain)*  
   Print the first column upwards.

After finishing one boundary, I **shrink the matrix boundaries** by moving:
- `startRow++`, `endRow--`
- `startCol++`, `endCol--`

This repeats until all elements are printed.

---
