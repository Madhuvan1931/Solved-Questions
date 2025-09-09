# 📈 Best Time to Buy and Sell Stock (LeetCode 121)

## 📌 Problem Statement
You are given an array `prices` where `prices[i]` is the price of a given stock on the **i-th day**.  

- You may choose **one day to buy** and **a different future day to sell**.  
- Return the **maximum profit** you can achieve.  
- If no profit is possible, return **0**.  

---

## 📝 Example
### Input:  
`prices = [7,1,5,3,6,4]`  

### Output:  
`5`  

### Explanation:  
- Buy on Day 2 (price = 1)  
- Sell on Day 5 (price = 6)  
- Profit = 6 - 1 = 5  

If `prices = [7,6,4,3,1]`, output = `0` (no profit possible).  

---

## 🔎 Approach / Logic
1. Keep track of the **minimum price so far** (`minPrice`).  
2. At each day, calculate the possible **profit = price - minPrice`.  
3. Update the **maximum profit** if the current profit is higher.  
4. If prices are always decreasing, the result will be **0**.  

- **Time Complexity:** O(n) → Single pass through array.  
- **Space Complexity:** O(1) → Only two variables used.  

---
