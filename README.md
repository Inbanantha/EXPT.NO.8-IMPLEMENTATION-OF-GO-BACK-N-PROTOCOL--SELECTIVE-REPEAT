# EXPT.NO.9-IMPLEMENTATION-OF-GO-BACK-N-PROTOCOL-SELECTIVE-REPEAT
# AIM:
To write and execute a program for Go-Back-N protocol-Selective Repeat.
# EQUIPMENTS REQUIRED:
Personal Computer Turbo C Compiler
# PROCEDURE:
8.	Connect two computers in Wired/Wireless LAN.
9.	Make sure that two computers are in one network and could able to ping each other.
10.	In the codeblocker open new c file and type the program.
11.	In the menu choose->Project->Properties->Project Build options->Linker settings->Add netproto and pthread.
12.	Execute the program in both server and client.
13.	Enter the IP address of the remote machine, port address of both local & remote machine and error rate.
14.	Choose the file and verify the go back protocol operation.

# PROGRAM:
```
#include <stdio.h> 
int main() 
{ 
int i, j, n; 
printf("GO BACK N ARQ\n"); 
printf("Enter number of frames: "); 
scanf("%d", &n); 
char frame[n + 1][10]; 
for (i = 1; i <= n; i++) 
{ 
printf("Content for frame %d: ", i); 
scanf("%s", frame[i]); 
} 
printf("\nEnter frame number with NO ACK (unacknowledged frame): "); 
scanf("%d", &j); 
for (i = 1; i <= n; i++) 
{ 
if (i != j) 
printf("\nSending frame %d: %s\nFRAME ACKNOWLEDGED.\n", i, frame[i]); 
else 
printf("\nFrame %d not acknowledged...\n", j); 
} 
if (j <= n) 
{ 
printf("\nNo acknowledgement for frame %d.\n", j); 
printf("Resending frames starting from frame %d...\n", j);
for (i = j; i <= n; i++) 
{ 
printf("Resending frame %d: %s\nFRAME ACKNOWLEDGED.\n", i, frame[i]); 
} 
} 
printf("\nAll frames received successfully!\n"); 
return 0; 
}
```
OUTPUT:
<img width="1918" height="1027" alt="Screenshot 2025-10-14 114004" src="https://github.com/user-attachments/assets/bdbc72b1-c950-4f0d-badf-243676a74f77" />

 






# RESULT:
Thus the Go-Back-N protocol- Selective Repeat was implemented and the output is verified successfully.
