# Ex.No: 2  Implementation of Depth First Search
### DATE: 14-08-2024      
### NAME: NANDA KISHORE R
### REGISTER NUMBER : 212222060157
### AIM: 
To write a python program to implement Depth first Search. 
### Algorithm:
1. Start the program
2. Create the graph by using adjacency list representation
3. Define a function dfs and take the set “visited” is empty 
4. Search start with initial node. Check the node is not visited then print the node.
5. For each neighbor node, recursively invoke the dfs search.
6. Call the dfs function by passing arguments visited, graph and starting node.
7. Stop the program.



### Program:

```
graph={
    '5':['3', '7'],
    '3':['2', '4'],
    '7':['8'],
    '2':[],
    '4':['8'],
    '8':[],
}
visited = set() # set to keep track of visited nodes of graph
def dfs(visited, graph, node): # function for dfs
    if node not in visited:
        print(node)
        visited.add(node)
        for neighbour in graph[node]:
            dfs(visited, graph, neighbour)
#driver code
print("Following is the depth-first search")
dfs(visited, graph,'5') #function calling
```




### Output:
<img src="https://github.com/user-attachments/assets/c1b15511-0713-41d2-a650-4d97ee18945b" width="600">


### Result:
Thus the depth first search order was found sucessfully.
