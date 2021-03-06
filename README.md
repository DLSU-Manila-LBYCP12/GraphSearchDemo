# GraphSearchDemo

DFS and BFS Demo:

Algorithm based on : https://youtu.be/bIA8HEEUxZI 

## Sample Run 1:
```java
// Testing Depth First Search
         graph.recursiveDFS("A");
         System.out.println("Recursive DFS Result: " + graph.getVisitedNodes());
 
         graph.iterativeDFS("A");
         System.out.println("Iterative DFS Result: " + graph.getVisitedNodes());

```


```
cd C:\Users\cobalt\Documents\NetBeansProjects\GraphSearchDemo; "JAVA_HOME=C:\\Program Files\\Java\\jdk1.8.0_112" cmd /c "\"\"C:\\Program Files\\NetBeans 8.2\\java\\maven\\bin\\mvn.bat\" -Dexec.args=\"-classpath %classpath ph.edu.dlsu.graphsearchdemo.UndirectedGraph\" -Dexec.executable=\"C:\\Program Files\\Java\\jdk1.8.0_112\\bin\\java.exe\" -Dmaven.ext.class.path=\"C:\\Program Files\\NetBeans 8.2\\java\\maven-nblib\\netbeans-eventspy.jar\" -Dfile.encoding=UTF-8 org.codehaus.mojo:exec-maven-plugin:1.2.1:exec\""
Running NetBeans Compile On Save execution. Phase execution is skipped and output directories of dependency projects (with Compile on Save turned on) will be used instead of their jar artifacts.
Scanning for projects...
                                                                        
------------------------------------------------------------------------
Building GraphSearchDemo 1.0-SNAPSHOT
------------------------------------------------------------------------

--- exec-maven-plugin:1.2.1:exec (default-cli) @ GraphSearchDemo ---
Nodes are: [A, B, C, D, E, F, G, H]
Adjacency list: 
A: [B, D, G]
B: [A, E, F]
C: [F, H]
D: [A, F]
E: [B, G]
F: [B, C, D]
G: [A, E]
H: [C]
Recursive DFS Result: [A, B, E, G, F, C, H, D]
Stack: [A]
Visited: [A]
Stack: [A, B]
Visited: [A, B]
Stack: [A, B, E]
Visited: [A, B, E]
Stack: [A, B, E, G]
Visited: [A, B, E, G]
Stack: [A, B, E]
Visited: [A, B, E, G]
Stack: [A, B]
Visited: [A, B, E, G]
Stack: [A, B, F]
Visited: [A, B, E, G, F]
Stack: [A, B, F, C]
Visited: [A, B, E, G, F, C]
Stack: [A, B, F, C, H]
Visited: [A, B, E, G, F, C, H]
Stack: [A, B, F, C]
Visited: [A, B, E, G, F, C, H]
Stack: [A, B, F]
Visited: [A, B, E, G, F, C, H]
Stack: [A, B, F, D]
Visited: [A, B, E, G, F, C, H, D]
Stack: [A, B, F]
Visited: [A, B, E, G, F, C, H, D]
Stack: [A, B]
Visited: [A, B, E, G, F, C, H, D]
Stack: [A]
Visited: [A, B, E, G, F, C, H, D]
The stack is finally empty!

Iterative DFS Result: [A, B, E, G, F, C, H, D]
------------------------------------------------------------------------
BUILD SUCCESS
------------------------------------------------------------------------
Total time: 0.871s
Finished at: Thu Jul 27 14:22:10 CST 2017
Final Memory: 5M/109M
------------------------------------------------------------------------

```
## Sample Run 2:
```
    graph.iterativeBFS("A");
    System.out.println("Iterative BFS Result: " + graph.getVisitedNodes());
```

```
cd C:\Users\cobalt\Documents\NetBeansProjects\GraphSearchDemo; "JAVA_HOME=C:\\Program Files\\Java\\jdk1.8.0_112" cmd /c "\"\"C:\\Program Files\\NetBeans 8.2\\java\\maven\\bin\\mvn.bat\" -Dexec.args=\"-classpath %classpath ph.edu.dlsu.graphsearchdemo.UndirectedGraph\" -Dexec.executable=\"C:\\Program Files\\Java\\jdk1.8.0_112\\bin\\java.exe\" -Dmaven.ext.class.path=\"C:\\Program Files\\NetBeans 8.2\\java\\maven-nblib\\netbeans-eventspy.jar\" -Dfile.encoding=UTF-8 org.codehaus.mojo:exec-maven-plugin:1.2.1:exec\""
Running NetBeans Compile On Save execution. Phase execution is skipped and output directories of dependency projects (with Compile on Save turned on) will be used instead of their jar artifacts.
Scanning for projects...
                                                                        
------------------------------------------------------------------------
Building GraphSearchDemo 1.0-SNAPSHOT
------------------------------------------------------------------------

--- exec-maven-plugin:1.2.1:exec (default-cli) @ GraphSearchDemo ---
Nodes are: [A, B, C, D, E, F, G, H]
Adjacency list: 
A: [B, D, G]
B: [A, E, F]
C: [F, H]
D: [A, F]
E: [B, G]
F: [B, C, D]
G: [A, E]
H: [C]
Queue: [A]
Visited: [A]
Queue: [B, D, G]
Visited: [A, B, D, G]
Queue: [D, G, E, F]
Visited: [A, B, D, G, E, F]
Queue: [G, E, F]
Visited: [A, B, D, G, E, F]
Queue: [E, F]
Visited: [A, B, D, G, E, F]
Queue: [F]
Visited: [A, B, D, G, E, F]
Queue: [C]
Visited: [A, B, D, G, E, F, C]
Queue: [H]
Visited: [A, B, D, G, E, F, C, H]
The queue is finally empty!

Iterative BFS Result: [A, B, D, G, E, F, C, H]
------------------------------------------------------------------------
BUILD SUCCESS
------------------------------------------------------------------------
Total time: 1.117s
Finished at: Thu Jul 27 15:52:02 CST 2017
Final Memory: 5M/109M
------------------------------------------------------------------------
```
