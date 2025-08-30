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


import math

def minimax(curDepth, nodeIndex, maxTurn, scores, targetDepth):
    """
    Minimax recursive function.
    curDepth   : current depth in game tree
    nodeIndex  : index of current node in scores[]
    maxTurn    : True if current move is by maximizer, False if minimizer
    scores     : leaf node values
    targetDepth: maximum depth of the game tree
    """
    
    # Base case: target depth reached → return the score at this node
    if curDepth == targetDepth:
        return scores[nodeIndex]

    if maxTurn:
        # Maximizer's move → choose the maximum of the next two states
        return max(
            minimax(curDepth + 1, nodeIndex * 2, False, scores, targetDepth),
            minimax(curDepth + 1, nodeIndex * 2 + 1, False, scores, targetDepth)
        )
    else:
        # Minimizer's move → choose the minimum of the next two states
        return min(
            minimax(curDepth + 1, nodeIndex * 2, True, scores, targetDepth),
            minimax(curDepth + 1, nodeIndex * 2 + 1, True, scores, targetDepth)
        )

if __name__ == "__main__":
    scores = [3, 5, 2, 9, 12, 5, 23, 20]

    # Tree depth = log2(len(scores))
    treeDepth = int(math.log(len(scores), 2))

    print("The optimal value is:", minimax(0, 0, True, scores, treeDepth))












### Output:
<img width="1920" height="1080" alt="Screenshot (26)" src="https://github.com/user-attachments/assets/c45bf199-ca69-45a1-8cff-efa0254014d2" />




### Result:
Thus the breadth first search order was found sucessfully.
