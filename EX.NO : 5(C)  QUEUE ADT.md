
# EX.NO : 5(C)  QUEUE ADT 

# PROGRAM STATEMENT : 
To write a CPP Program to insert 5 operator elements in to Queue ADT. 
 
# ALGORITHM:   
1. Create a queue of characters using queue<char>. 
2. Input 5 characters using a loop and push each character into the queue. 
3. Print the message "Queue Elements are:". 
4. Use a while loop to traverse the queue until it is empty. 
5. For each iteration, print the front element of the queue using que.front(). 
6. Remove the front element from the queue using que.pop() 
7. End the program 
 
# PROGRAM: 
```
#include <iostream>
#include <queue>
using namespace std;
int main() {
    queue<char> opQueue;
    char input;
    for (int i = 0; i < 5; ++i) {
        cin >> input;
        opQueue.push(input);
    }
    cout << "Queue Elements are:";
    while (!opQueue.empty()) {
        cout << opQueue.front() << " ";
        opQueue.pop();
    }
    cout << endl;
    return 0;
}
```
# Output:

 ![Screenshot 2025-05-27 113753](https://github.com/user-attachments/assets/27689f5c-1273-46ee-85ac-dcce7a178a0b)


# Result:
Thus, the C++ program to insert 5 operator elements in to Queue ADT is created successfully. 

 
