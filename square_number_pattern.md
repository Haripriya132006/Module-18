# 🧮 Number Pattern Generator (Concentric Square Pattern)
## 📌 AIM
To print a square pattern of size (2 * n - 1) where numbers decrease toward the center of the pattern and increase back outward, forming a symmetric, concentric square pattern.

## 📖 Description
Given a single integer input n, this program prints a square matrix of size (2 * n - 1) filled with concentric layers of numbers starting from n at the outer layer and decreasing by 1 at each inner layer until 1 is reached at the center.

## 📋 Input Format
A single integer n (1 ≤ n ≤ 100)

## 📤 Output Format
A square pattern with each number separated by a single space.

The number at each position depends on the minimum distance to any edge from that cell.

## 💡 Logic Explanation
The output is a square of dimension (2 * n - 1) × (2 * n - 1).

For each cell (i, j), determine its distance from all four edges (top, left, bottom, right).

The minimum of these distances tells how "deep" the cell is in the square layers.

Subtract this minimum from n to get the value to be printed.

## 🧠 Algorithm
Read input n.

Compute size = 2 * n - 1.

For each position (i, j) in the grid:

Compute min_distance = min(i, j, size - 1 - i, size - 1 - j).

Print n - min_distance.

Print each row on a new line.

## 💻 C Code
```
#include <stdio.h>

int main() {
    int n;
    scanf("%d", &n);
    
    int size = 2 * n - 1;  // Matrix size (rows and columns)

    for (int i = 0; i < size; i++) {
        for (int j = 0; j < size; j++) {
            int min = i < j ? i : j;  // Minimum of row or column index
            min = min < size - i ? min : size - i - 1;  // Compare with bottom
            min = min < size - j ? min : size - j - 1;  // Compare with right

            printf("%d ", n - min);
        }
        printf("\n");  // New line after each row
    }

    return 0;
}

```

## Output
![alt text](image-4.png)

## ✅ Result
This C program correctly prints a concentric square number pattern for any valid input n.

