
# EX.NO : 5(D)  QUEUE APPLICATIONS
 
# PROGRAM STATEMENT : 
 write a C++ program to implement FCFS algorithm(no of.process p1,p2 and p3 and its burst time are 10,5 & 8) find out waiting time ,Turn Around time  & Average turn around time of the the process? 
# ALGORITHM:   
 
1. Start the program. 
2. Define findWaitingTime to take process IDs, count of processes n, and burst times bt. 
3. Initialize wt for waiting times and set wt[0] = 0. 
4. Use a loop to calculate each waiting time as wt[i] = bt[i-1] + wt[i-1]. 
5. Print "Processes", "BT time", and "WT time" table headings. 
6. Use a loop to print each process's ID, burst time, and waiting time, adding each to total_wt. 
7. Print average waiting time as total_wt / n. 
8. In main, define processes, n, and bt, then call findWaitingTime. 
9. End the program. 
 
# PROGRAM:
```
#include <iostream>
using namespace std;
int main() {
    const int n = 3;
    int burst_time[n] = {10, 5, 8};
    int waiting_time[n], turn_around_time[n];
    int total_TA = 0;
    waiting_time[0] = 0;
    turn_around_time[0] = burst_time[0];
    for (int i = 1; i < n; i++) {
        waiting_time[i] = waiting_time[i - 1] + burst_time[i - 1];
        turn_around_time[i] = waiting_time[i] + burst_time[i];
    }
    for (int i = 0; i < n; i++) {
        total_TA += turn_around_time[i];
    }
    cout << "Processes   BT time   WT time   TA time\n";
    for (int i = 0; i < n; i++) {
        cout << "       " << i + 1 << "       " << burst_time[i]
             << "       " << waiting_time[i]
             << "       " << turn_around_time[i] << endl;
    float avg_TA = (float)total_TA / n;
    cout << "Average turn around time = " << avg_TA << endl;
    return 0;
}
```
# output:

![Screenshot 2025-05-27 114301](https://github.com/user-attachments/assets/7ee47ce7-315a-4240-87af-3ef814c8a019)
 

# Result:
Thus, write a C++ program to implement FCFS algorithm(no of.process p1,p2 and p3 and its burst time are 10,5 & 8) find out waiting time ,Turn Around time  & Average turn around time of the the process? 
 
