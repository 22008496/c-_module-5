# EX.NO : 5(A)  STACK ADT

# PROGRAM STATEMENT : 
To Write a CPP Program to insert five character elements in to Stack ADT (use STL for Stack. 
 
# ALGORITHM:   
1. Start the program. 
2. Initialize a stack of characters named mystack. 
3. Read an integer n as the size of the stack. 
4. Print the size of the stack. 
5. Use a loop to read n characters and push each character onto the stack. 
6. Use a loop to pop and print each character from the stack until the stack is empty. 
7. End the program. 
 
# PROGRAM: 
```
#include<iostream>
#include<stack>
using namespace std;
int main()
{
    stack<char> s;
    int n;
    char ch;
    cin >> n;
    for(int i = 0; i < n; ++i) {
        cin >> ch;
        s.push(ch);
    }
    cout << "Size of the stack: " << s.size() << endl;
    while(!s.empty()) {
        cout << s.top() << " ";
        s.pop();
    }
    cout << endl;
    return 0;
}
```

# output:

![Screenshot 2025-05-27 112555](https://github.com/user-attachments/assets/ac8e57e1-f1c6-4c83-a44d-3b6430f6ccc4)

# Result:

Thus, the C++ program to insert five character elements in to Stack ADT is created successfully. 


