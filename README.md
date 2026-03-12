# Data-structure-practical-program-16
from collections import deque

def BFS(graph, start):
    visited = []
    queue = deque()

    visited.append(start)
    queue.append(start)

    while queue:
        node = queue.popleft()
        print(node, end=" ")

        for neighbour in graph[node]:
            if neighbour not in visited:
                visited.append(neighbour)
                queue.append(neighbour)

# Graph representation
graph = {
    0: [1, 2],
    1: [3, 4],
    2: [5],
    3: [],
    4: [],
    5: []
}

BFS(graph, 0)
0 1 2 3 4 5
