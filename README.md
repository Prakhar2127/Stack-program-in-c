// Stack-program-in-c
#include <stdio.h>
#include <stdlib.h>
#define MAX 5

int stack[MAX];
int top = -1;

int push()
{
        if(top == MAX-1)
    {
        printf("\nOverflow Condition\n");
    }
    else 
    {
        int x;
        printf("Enter a value: ");
        scanf("%d",&x);
        top++;
        stack[top]=x;
    }
}
int pop()
{
    int var;
    if(top == -1)
    {
        printf("Underflow condition");
    }
    else{
        var=stack[top];
        top--;
        printf("The poped value is: %d",var);
    }
}
int peek()
{
    if(top == -1){
        printf("The stack is empty");
    }
    else{
        printf("The top element is: %d",stack[top]);
    }
}
int display()
{
    for(int i=top; i>=0; i--)
    {
        printf("%d\n",stack[i]);
    }
}
int main()
{
    int a;
    do
    {
    printf("\nINDEX:\n1)Push Operation\n2)Pop Operation\n3)Display the top value\n4)Display the stack\n5)Exit\n");
    scanf("%d",&a);

    switch(a)
    {
        case 1: push();
                break;
        case 2: pop();
                break;
        case 3: peek();
                break;
        case 4: display();
                break;
        case 5: exit(0);
    }
    }
    while(a!=0);
}
