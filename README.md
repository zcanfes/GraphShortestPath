## Description

Five CmpE students would like to go to the Ancient Anti-Taurus Montains Range, and they are trying to reach the Kizilkaya summit. You are asked to help them with their journey.

In Anti-Taurus Mountains, there are N registered nodes (i.e., reference points to find the way in the mountains) and M undirected two-way edges.

**Nodes:** The nodes are numbered with integers from 1 to N inclusively. Node 1, Ironpicket camping area, is the starting point for all mountaineers, who comes to Anti-Taurus Mountains. The summit is on the K^th node (so the mountaineers wants to reach node K).

**Edges:** Each undirected edge has a time value, which indicates the duration to cover the edge. 

5 CmpE students try different approches to reach the summit.

- The goal of the **first student** is to reach the summit as fast as possible in terms of time, so s(he) follows the shortest path.
- The **second student** does not like to walk through long edges, so goal of the second student is to reach the summit by walking through the edges that takes shorter time. Therefore, (s)he wants to minimize the duration of the maximum edge (s)he takes in his/her way to the summit.
- The **third student** does not care about the time each edge takes, so all edges are same for him/her. (S)he wants to visit as less node as possible. In another words, his/her goal is to find a way to the summit that passes through the minimum number of edges.
- The **fourth student** is greedy and when (s)he is in a node, (s)he chooses the shortest edge out of that node. However, (s)he can use the same edge only once. When (s)he reaches the summit, his/her journey finishes. Note that when there are two shortest edges with same length, (s)he picks the one with the lower edge number(i).
- The **fifth student** has a secret power, (s)he can teleport between adjacent nodes, so it takes 0 time to travel between them. However, to recharge that secret power, (s)he needs to pass two edges, and (s)he does not have that secret power at the beginning of his/her journey. Unlike other four students, (s)he can use the same edge multiple times, so in the first move, (s)he may go N_1->N_2 and N_2->N_1 to recharge his/her secret power. (S)he cannot store his/her secret power and must use it right away after after gaining it.

**Important note:** Only **fifth student** can use the same edge multiple times. Other four students can use the same edge only once.

All five students need your help to find the path they should follow. Your task is to calculate the path that each student should follow.

- The first student wants to know the shortest time to reach the summit.
- The second student wants to know the minimum possible duration of the maximum edge he passes through in his/her journey.
- The third student wants to know the minumum number of edges (s)he needs to pass to reach the summit.
- The fourth student wants to know the time to reach the summit if (s)he uses the greedy algorithm mentioned above. If (s)he cannot reach the summit, you should print the value "-1".
- The fifth student wants to know the shortest time to reach the summit. At start, (s)he does not have any power, so (s)he needs to pass two edges to recharge it. 

To implement this project, you will be provided some code written by the assistants, which handles the reading input and output files.

The files you will be provided are HelpStudents.h, HelpStudents.cpp, and main.cpp.

The file you should fill is: HelpStudents.cpp. You are also allowed to change the content of HelpStudents.h. Therefore, any code written outside HelpStudents.cpp and HelpStudents.h will be useless for this project.

## Input

In the first row of the input, there are 4 numbers. ```(T N M K)``` 
- First number specifies which type of student(T) needs your help.
- Second number is N, which represents the number of registered nodes.
- Third number is M, which represents the number of edges.
- Fourth number is K, which is the node number that represents the summit.

Next M lines have 3 numbers per row. ```(A_i B_i W_i)```
- Each row states that there is a path between node A_i and node B_i with weight W_i (i.e., required time to pass this path). 


## Output

Contains a single number, an answer according to the student's goal stated in the description.


## Constraits

N (number of nodes) <= 100000

M (number of edges) <= 100000

W_i <= 1000000 (**Note that some answers may exceed integer range. You must use ```long long int``` type for the answers.** )

## Sample Input 1

```
1 6 9 5
1 2 5
1 3 1
3 2 10
1 5 25
2 4 6
4 5 3
3 6 5
2 6 7
5 6 10
```

## Sample Output 1

```
14
```

## Sample Input 2

```
2 6 9 5
1 2 5
1 3 1
3 2 10
1 5 25
2 4 6
4 5 3
3 6 5
2 6 7
5 6 10
```

## Sample Output 2

```
6
```

## Sample Input 3

```
3 6 9 5
1 2 5
1 3 1
3 2 10
1 5 25
2 4 6
4 5 3
3 6 5
2 6 7
5 6 10
```

## Sample Output 3

```
1
```

## Sample Input 4

```
4 6 9 5
1 2 5
1 3 1
3 2 10
1 5 25
2 4 6
4 5 3
3 6 5
2 6 7
5 6 10
```

## Sample Output 4

```
43
```

## Sample Input 5

```
5 6 9 5
1 2 5
1 3 1
3 2 10
1 5 25
2 4 6
4 5 3
3 6 5
2 6 7
5 6 10
```

## Sample Output 5

```
2
```
