# Ex.No: 1  Implementation of Breadth First Search 
### DATE:30/08/2025                                                                            
### REGISTER NUMBER :212222040093 
### AIM: 
To write a python program to implement Breadth first Search. 
### Algorithm:
1. Start the program
2. Create the graph by using adjacency list representation
3. Define a function bfs and take the set “visited” is empty and “queue” is empty
4. Search start with initial node and add the node to visited and queue.
5. For each neighbor node, check node is not in visited then add node to visited and queue list.
6.  Creating loop to print the visited node.
7.   Call the bfs function by passing arguments visited, graph and starting node.
8.   Stop the program.
### Program:

# Breadth First Search in Python

graph = {
    '5': ['3', '7'],
    '3': ['2', '4'],
    '7': ['8'],
    '2': [],
    '4': ['8'],
    '8': []
}

visited = []  # List for visited nodes
queue = []    # Initialize a queue


def bfs(visited, graph, node):
    """Breadth First Search implementation"""
    visited.append(node)
    queue.append(node)

    while queue:
        # Pop first element from queue
        m = queue.pop(0)
        print(m, end=" ")

        # Explore all neighbours of current node
        for neighbour in graph[m]:
            if neighbour not in visited:
                visited.append(neighbour)
                queue.append(neighbour)



print("Following is the Breadth-First Search traversal:")
bfs(visited, graph, '5')












### Output:
<img width="1920" height="1080" alt="Screenshot (29)" src="https://github.com/user-attachments/assets/2932b858-3e2c-4882-a834-7f3f0e8c7c26" />





### Result:
Thus the breadth first search order was found sucessfully.
