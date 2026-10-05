# Lab 4: Concept Review
(WARNING:I can get an answer but use the wrong methods. So I'm sorry if I sound stupid in my writing, It wakes sense in my brain but my brain is using a completely different method)
This lab reviews the foundational concepts of algorithms and data structures that we have covered in the first half of the course. 

**Instructions:** To complete this lab, you may work in groups, but you must write your solutions yourself. Choose two of the topics below that you need to review and complete the corresponding problems. Where relevant, you are given the answer and must provide the justification as your solution. Once you have completed the lab, push your changes to your forked repository.

**Topics:** asymptotic analysis, and empirical comparison of algorithms

## Asymptotic Analysis

1. Use the rules from lecture 07 to prove that $T(n) = 5 \log n + 7n$ is $\mathcal{O}(n)$.
(I know why in my own method, Might sound like an idot for how I do it though) So basicall you have the 5logn and the 7n. We just kinda drop the 5logn and have the 7n but we just drop the 7 and have t(n) = O(n)
2. True/False/Possibly: $T(n)$ is $\mathcal{O}(n^2)$?

**Answer**: Yes

**Justification**:algorithm uses quadratic running time and worst case of running is T(n) (I know this from the slides.)

3. True/False/Possibly: $T(n)$ is $\Omega(n \log n)$?

**Answer**: No

**Justification**: again in my mind it doesn't work because of the nlogn

4. For any algorithm, we can give a trivial lower bound. What is that lower bound?

**Answer**: $\Omega(1)$

**Justification**:because there is always a bound at the bottom that is a possibility. Like you can just hit the bottom and work your way up from there.

5. Is there a corresponding trivial upper bound? Why or why not?

**Answer**: No

**Justification**: We have no idea how high the upper bound could be. Unlit the lower bound we were able to go down as low as possible, but for this we can't just go as high as possible.




## Empirical Comparison of Algorithms

1. A student is benchmarking an algorithm that takes a list as its input. They run it on progressively larger randomly generated lists, doubling the number of elements ($n$) and record the following execution times:

- $n = 1000$: 0.12 seconds
- $n = 2000$: 0.94 seconds
- $n = 4000$: 7.61 seconds
- $n = 8000$: 60.85 seconds

 Based on this empirical data, what is the most likely asymptotic time complexity of the algorithm? **Hint**: Calculate the doubling ratio between each pair of consecutive runs.

 **Answer**: Cubic time complexity, $\mathcal{O}(n^3)$

**Justification**: (Dumb answer) the number just grows and grows and grows by an extreme amount that the amount of time is going up.What matches this pattern with the time increase is n^3

 2. Two students write separate algorithms to compute a metric over an array of 10 million integers. Both algorithms perform exactly one mathematical operation per element, meaning both have a theoretical time complexity of $O(N)$. However, during benchmarking, Algorithm A consistently runs 15x faster than Algorithm B. Why might theoretical Big-O analysis fail to predict this massive performance gap? 

**Answer**: This could be due to something stupid like how many things are opened in the background and computer type.Big O can take into account that type of thing. I know this is most likely a stupid answer but I remember us talking about it

 3. Scenario: To measure the running time of algorithms for an empirical comparison, a developer writes the following benchmarking script:

```python
import time

large_array = [i for i in range(1000000)]
start = time.time()
myAlg(large_array)
end = time.time()

print("Time:", end - start)
```

They run this script exactly once for each algorithm on their laptop while streaming a movie in the background. Identify at least three distinct methodological flaws in this benchmarking setup that make the results unreliable.

**Answer**: The movie. The large array the computer is trying to compreheand. And Start and end both being time.time() when there are so many different times.