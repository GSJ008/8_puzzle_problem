# 8 Puzzle Problem

## **AIM**
The aim of this project is to solve the **8 Puzzle Problem** using the **Depth First Search (DFS)** algorithm and demonstrate how an initial configuration of tiles can be rearranged to reach a predefined goal state by sliding the tiles into the empty space.

---

## **Algorithm (DFS)**

1. **Initialize**
   - Define the **start state** and the **goal state** of the puzzle.
   - Use a **stack** to store states to explore.
   - Maintain a set of **visited states** to avoid repetitions.

2. **Push Start State**
   - Push the start state onto the stack.
   - Mark it as visited.

3. **Loop Until Goal Found**
   - Pop the top state from the stack.
   - If it matches the goal state, terminate and return the solution path.

4. **Generate Successors**
   - Locate the empty tile (0) in the current state.
   - Move the empty tile **up, down, left, or right** to generate valid child states.
   - For each valid child:
     - If the child has not been visited, push it onto the stack and mark as visited.

5. **Repeat**
   - Continue until the stack is empty (if no solution) or goal is found.

---

## **Time Complexity**
For DFS in the 8 Puzzle Problem:

- **Worst-case time complexity:**  
  \[
  O(b^m)
  \]  
  where:  
  - \( b \) = branching factor (~2–4 for 8 Puzzle)  
  - \( m \) = maximum depth of the state space (can be up to 9! = 362,880 states)

- **Space complexity:**  
  DFS generally uses \( O(bm) \) space because it stores only the current path in memory, plus visited states.

---

## **Use Cases**
- **AI Problem Solving Demonstration**  
  Showcases uninformed search techniques in Artificial Intelligence.
- **State Space Search Teaching**  
  Helps understand depth-first traversal in a finite state space.
- **Puzzle Mechanics Implementation**  
  Sliding tile puzzle logic for games.
- **Algorithm Benchmarking**  
  Compare DFS against BFS or A* for the same problem.
- **Research in Search Strategies**  
  Understanding trade-offs between completeness, time, and space.

---

8 Puzzle Problem
AIM
Solve the 8 Puzzle Problem using Breadth First Search (BFS) to reach a goal configuration by sliding tiles into the empty space (0).

Algorithm (BFS)
Initialize

Define the start and goal state.
Use a queue to explore states level by level.
Track visited states to avoid repeats.

Start
Enqueue the start state and mark it visited.

Process
While the queue isn’t empty:

Dequeue a state.
If it’s the goal, return the solution.

Generate valid successors by sliding the empty tile up/down/left/right.
Enqueue unvisited successors.

Time Complexity
Worst-case:
O(b^d)
where:
b: branching factor (~2–4)
d: depth of the shallowest goal node

Space Complexity:
𝑂(𝑏^𝑑) — stores all nodes at each level (can grow large quickly)

Use Cases
AI Search Strategy: Demonstrates complete and optimal uninformed search.

Teaching Tool: Helps visualize level-order exploration in state-space.

Comparison Benchmark: Useful for evaluating DFS, BFS, and A* side-by-side.
