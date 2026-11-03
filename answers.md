# CMPS 2200 Recitation 07
## Answers

**Name:**_Srikanya Balaji Garuda__
**Name:**_________________________


Place all written answers from `recitation-07.md` here for easier grading.



- **2) (2 pts)** Write a recurrence for the **work** of this algorithm and solve it. Assume the input is $n$ to compute $F_n$.
$W(n) = W(n-1) + W(n-2) + O(1)$
This equals $O(n^2)$ because each call splits into 2 more calls creating a binary tree

- **3) (2 pts)** Write a recurrence for the **span** of this algorithm and solve it.
$S(n) = \max(S(n-1), S(n-2)) + O(1) = S(n-1) + O(1)$
Span measures longest path and we take maximum of 2 branches (n-1)
This equals $O(n)$, as it goes down n(linear) levels

- **4) (1 pt)** Inspecting the `counts` list, what interesting pattern emerges?
The values in counts mirror the fibonacci sequence in reverse order as the base cases are called several times to get later values in the sequence due to recursion

- **6) (2 pts)** When computing $F_n$, what is the maximum number of times that `fib_top_down(i)` will be called for any value $i$? Based on this, what is the **work** and **span** of this algorithm?
It is maximum called twice (1st time: calculation, 2nd time: realize it's cached, so return it).
$W(n) = O(n)$
$S(n) = O(n)$

- **8) (2 pts)** When computing $F_n$, what is the maximum number of times that
  $F_i$ will be read from the list for any value $i$? Based on this, what is the **work** and **span** of `fib_bottom_up`?
It is maximum called twice (first: F(n+1), second: F(n+2), as each call uses the 2 prior values)
$W(n) = O(n)$
$S(n) = O(n)$

