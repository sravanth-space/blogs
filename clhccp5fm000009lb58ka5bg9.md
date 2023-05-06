---
title: "Rules for Solving a Coding Question in an Interview"
datePublished: Sat May 06 2023 19:01:08 GMT+0000 (Coordinated Universal Time)
cuid: clhccp5fm000009lb58ka5bg9
slug: rules-for-solving-a-coding-question-in-an-interview
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/U5y077qrMdI/upload/268b8e7fd18f9bb7a9bd95d2653d3b83.jpeg

---

* If we are dealing with **top/maximum/minimum/closest** 'K' elements among 'N' elements, we will be using a **Heap**.
    
* If the given input is a **sorted array** or a list, we will either be using **Binary Search** or the **Two Pointers** strategy.
    
* If we need to try all **combinations** (or permutations) of the input, we can either use **Backtracking** or **Breadth First Search**.
    
* Most of the questions related to Trees or Graphs can be solved either through **Breadth First Search** or **Depth First Search**.
    
* Every **recursive** solution can be converted to an **iterative** solution using a **stack**.
    
* For a problem involving arrays, if there exists a solution in **O(n^2)** time and **O(1)** space, there must exist two other solutions
    
    * Using a **HashMap** or **Set** for O(n) time and space.
        
    * Using **sorting** for O(n.log n) time O(1) space.
        
* If a problem in asking for **optimization**(e.g. maximization or minimization), we will be using **Dynamic Programming.**
    
* If we need to find some common **substring** among a set of strings, we will be using a **HashMap** or **Trie**.
    
* If we need to **search/manipulate** a bunch of strings then **Trie** will be the best data structure.
    
* If the problem is related to **LinkedList** and we can't use extra space, then use the **Fast & Slow Pointer** approach.