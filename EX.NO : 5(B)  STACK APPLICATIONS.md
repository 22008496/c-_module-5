
# EX.NO : 5(B)  STACK APPLICATIONS


# PROGRAM STATEMENT : 
To write a CPP program for Infix to Prefix Conversion using Stack STL 
 
# ALGORITHM:   
1. Define a function priority to assign precedence to operators. 
2. Create a Prefix string and a stack to hold operators. 
3. Loop through each character in the infix expression, processing operands and operators. 
4. Handle parentheses by pushing and popping from the stack. 
5. After processing the expression, pop any remaining operators from the stack to Prefix. 
6. Print the resulting Prefix expression. 
7. End the program 
 
# PROGRAM: 
```
#include <iostream>
#include <stack>
#include <algorithm>
bool isOperator(char c) {
    return (c == '+' || c == '-' || c == '*' || c == '/');
}
int precedence(char c) {
    if (c == '+' || c == '-')
        return 1;
    else if (c == '*' || c == '/')
        return 2;
    return 0;
}
std::string infixToPrefix(std::string infix) {
    std::stack<char> operators;
    std::string prefix;
    std::reverse(infix.begin(), infix.end());
    for (char& c : infix) {
        if (isalpha(c)) {
            prefix += c;
        } else if (c == ')') {
            operators.push(c);
        } else if (c == '(') {
            while (!operators.empty() && operators.top() != ')') {
                prefix += operators.top();
                operators.pop();
            }
            operators.pop(); // Pop the ')'
        } else if (isOperator(c)) {
            while (!operators.empty() && precedence(operators.top()) > precedence(c)) {
                prefix += operators.top();
                operators.pop();
            }
            operators.push(c);
        }
    }
    while (!operators.empty()) {
        prefix += operators.top();
        operators.pop();
    }
    std::reverse(prefix.begin(), prefix.end());
    return prefix;
}
int main() {
    std::string infix;
    std::cin >> infix;
    std::string prefix = infixToPrefix(infix);
    std::cout << "Prefix expression: " << prefix << std::endl;
    return 0;
}
```
# output:
 
![Screenshot 2025-05-27 113516](https://github.com/user-attachments/assets/7d37548d-9a38-472e-b359-6d2ad0668391)

# Result:
Thus, the C++ program for Infix to Prefix Conversion using Stack STL is created successfully. 
 
