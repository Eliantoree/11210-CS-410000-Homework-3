# 11210-CS-410000-Homework-3
11210 CS 410000 Homework 3


**Download Link:https://programming.engineering/product/11210-cs-410000-homework-3/**

Description
5/5 – (2 votes)
There are two parts in this homework.

PART I. – Procedure call

In this part, you are goint to write a MPS assembly program for the following C program.

#include <stdio.h>

#include <math.h>

int compare(int p, int q){

if(p > q) return p + q;

else return p;

}

int smod(int p , int q){

int div, divd;

if(p > q) div = 2 + pow(2, p%4);

else div = 4 + pow(2, q%4);

div = div * 5;

divd = p * 4 + q;

return divd % div;

}

17

int main(){

int x, y, z, ans;

printf(“input x: “);

scanf(“%d”, &x);

printf(“input y: “);

scanf(“%d”, &y);

printf(“input z: “);

scanf(“%d”, &z);

ans = smod(compare(x, y), z);

printf(“result = %d\n”, ans);

return 0;

}

Input constraints:                     



Output format example:

You must use the procedure (function) call to implement. Also, your program should terminal normally (the output should show “– program is finished running — “).

PART II. – Recursive call

In this part, you are going to write a MIPS assembly program that traces the step-by-step processes of the Towers of Hanoi puzzle and calculates the total number of movements.

The example C code and Input, Output format is shown below.

Tower of Hanoi (moving disks from A to B)

Example C program

#include <stdio.h>

int cnt = 0;

void MoveTower(int disk, char source, char dest, char spare) {

if(disk == 0) {

// Move disk from source to dest

printf(“Move disk %d from %c to %c\n”, disk, source, dest);

++cnt;

}

else {

// Move the smaller disk from source to spare

MoveTower(disk – 1, source, spare, dest);

14

// Move disk from source to dest

printf(“Move disk %d from %c to %c\n”, disk, source, dest);

++cnt;

18

// Move the smaller disk from spare to dest

MoveTower(disk – 1, spare, dest, source);

}

}

23

int main() {

int numDisks;

printf(“Please input the total number of disks: “);

scanf(“%d”, &numDisks);

MoveTower(numDisks – 1, ‘A’, ‘B’, ‘C’);

29

printf(“Total number of movement = %d\n”, cnt);

return 0;

}

Input constraints:        

Output format example:

You must use the procedure (function) call to implement. Also, your program should terminal normally (the output should show “– program is finished running — “).

Submission (2 assembly programs)

Please name your assembly program with your student ID in the following format:

arch_hw3_p1_<student_ID>.asm



arch_hw3_p2_<student_ID>.asm



Use the eeclass (https://eeclass.nthu.edu.tw/) to submit your programs.

Grading Criteria

Correctness: 80%



Comment in program: 10%



Output format: 10%



Remember Plagiarism is strictly prohibited.

Appendix

https://www.cs.cmu.edu/~cburch/survey/recurse/hanoiimpl.html
