
# SLE-4: Final Viva and Architecture Decision Record (ADR)

## Project Information

- **Course:** 02AML204 – Introduction to Artificial Intelligence
- **Student Name:** Samruddhi Jotiram Misal
- **PRN:** 25UAM046
- **Division:** A
- **Date:** 12 October 2026
- **GitHub Repository:** [IAI_SLE-4](https://github.com/misalsamruddhi599-tech/IAI_SLE-4)

## 1. Project Overview

This project focuses on the empirical performance comparison of Breadth-First Search (BFS) and Depth-First Search (DFS) algorithms using a synthetic graph containing 1,200 nodes.

The project evaluates the algorithms using execution time and node expansion count across three test cases: Best Case, Average Case, and Worst Case.

## 2. Objectives

- To understand BFS and DFS search algorithms.
- To compare their execution times.
- To measure the number of expanded nodes.
- To design a four-level C4 software architecture.
- To document the algorithm selection using an Architecture Decision Record (ADR).
- To prepare for the final viva examination.

## 3. Algorithms Used

### Breadth-First Search (BFS)

BFS explores nodes level by level. It uses a FIFO queue implemented using `collections.deque`.

### Depth-First Search (DFS)

DFS explores deeper nodes first. It uses a LIFO stack implemented using a Python list.

## 4. Experimental Setup

- **Graph size:** 1,200 nodes
- **Graph structure:** Forward connections to the next four available nodes
- **Performance measurement:** Python `timeit` module
- **Execution runs:** 3
- **Additional workload:** 2,000-iteration compute delay loop
- **Metrics:** Execution time and expanded nodes

## 5. Test Cases

| Test Case | Goal Node |
|---|---:|
| Best Case | 1 |
| Average Case | 600 |
| Worst Case | 1199 |

## 6. Empirical Results

| Test Case | Algorithm | Execution Time | Expanded Nodes |
|---|---|---:|---:|
| Average | BFS | 33.80 ms | 601 |
| Average | DFS | 12.25 ms | 241 |
| Worst | BFS | 61.66 ms | 1200 |
| Worst | DFS | 24.66 ms | 483 |

The values shown above are the recorded benchmark results for the specified test cases.

## 7. Architecture Decision Record (ADR)

**Decision:** Select DFS as the preferred traversal strategy for the tested graph structure.

**Reason:** DFS showed lower execution time and fewer node expansions than BFS in the reported average and worst cases.

**Trade-off:** DFS does not guarantee the shortest path in general. Its performance depends on graph structure and traversal order.

**Status:** Accepted for the specified benchmark.

## 8. C4 Architecture Model

The project uses four levels of the C4 architecture model:

1. **System Context:** Shows the system and its external users or dependencies.
2. **Container:** Describes the major applications and modules.
3. **Component:** Explains the internal components and their interactions.
4. **Code:** Describes the implementation-level structure.

Architecture diagrams are maintained as part of the project documentation.

## 9. SLE Journey

- **SLE-1:** Project setup, repository initialization, and AI Agent implementation.
- **SLE-2:** Empirical profiling of BFS and DFS.
- **SLE-3:** Design of the four-level C4 architecture.
- **SLE-4:** ADR documentation, performance-based decision justification, and viva preparation.

## 10. AI Contribution

ChatGPT and Gemini were used for documentation organization, coding guidance, and architecture documentation support.

The student reports having executed the benchmark scripts locally, checked the results, and created the C4 architecture diagrams.

## 11. Conclusion

For the tested synthetic graph, DFS demonstrated lower execution time and fewer expanded nodes in the reported average and worst cases. The decision is specific to the benchmark and should not be generalized to every graph or search problem.

## 12. Repository Contents

The repository may contain:

- Python implementation files
- BFS and DFS profiling scripts
- C4 architecture diagrams
- Architecture Decision Record
- README documentation
- Contribution log

Refer to the files available in the repository for the actual implementation and supporting documentation.
