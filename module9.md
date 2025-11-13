EXP NO:11 C PROGRAM TO DISPLAY STACK ELEMENTS USING AN ARRAY.

Aim:
To write a C program to display stack elements using an array.
Algorithm:
1.	Include Necessary Header Files
2.	Declare Global Variables
3.	Define the Display Function
4.	Main Function (or Other Relevant Code)
5.	Initialize the stack and top as needed.
6.	Perform stack operations (push, pop, etc.).
7.	Use the display function to visualize the stack's contents
 
Program:

    #include <stdio.h>
    #define SIZE 5
    int stack[SIZE], top = -1;
    
    void display() {
        if (top == -1)
            printf("Stack is empty\n");
        else {
            printf("Stack elements: ");
            for (int i = top; i >= 0; i--)
                printf("%d ", stack[i]);
            printf("\n");
        }
    }
    
    int main() {
        stack[++top] = 10;
        stack[++top] = 20;
        stack[++top] = 30;
        display();
        return 0;
    }


Output:

<img width="520" height="233" alt="image" src="https://github.com/user-attachments/assets/bb3e53b8-73e5-46bf-ab30-9506b07147e7" />




Result:
Thus, the program to display stack elements using an array is verified successfully.
 

EXP NO:12  PROGRAM TO PUSH THE GIVEN ELEMENT IN TO A STACK USING ARRAY.
Aim:
To create a C program to push the given element in to a stack using array.
Algorithm:
1.	Declare global variables for the stack size, top index, and the stack itself.
2.	Define the push function to add a floating-point number to the stack.
3.	Initialize the stack size, top index, and the stack itself.
4.	Call the push function as needed.
 
Program:

    #include <stdio.h>
    #define SIZE 5
    float stack[SIZE];
    int top = -1;
    
    void push(float x) {
        if (top == SIZE - 1)
            printf("Stack overflow\n");
        else {
            stack[++top] = x;
            printf("%.2f pushed\n", x);
        }
    }
    
    int main() {
        push(10.5);
        push(20.2);
        push(30.7);
        return 0;
    }


Output:

<img width="521" height="244" alt="image" src="https://github.com/user-attachments/assets/1b589e08-3aa0-4078-9c60-a8337086d846" />





Result:
Thus, the program to push the given element in to a stack using array is verified successfully


 
EXP NO:13 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING ARRAY.
Aim:
To write a C program to display queue elements using array

Algorithm:
1.	Declare global variables for the queue, rear, front, and iteration.
2.	Define the display function to print the elements of the queue.
3.	Initialize the queue, rear, and front as needed.
4.	Call the display function and perform other queue operations as needed.
 
Program:

    #include <stdio.h>
    #define SIZE 5
    int queue[SIZE], front = -1, rear = -1;
    
    void display() {
        if (front == -1)
            printf("Queue is empty\n");
        else {
            printf("Queue elements: ");
            for (int i = front; i <= rear; i++)
                printf("%d ", queue[i]);
            printf("\n");
        }
    }
    
    int main() {
        queue[++rear] = 5;
        if (front == -1) front = 0;
        queue[++rear] = 10;
        queue[++rear] = 15;
        display();
        return 0;
    }


Output:

<img width="465" height="237" alt="image" src="https://github.com/user-attachments/assets/3f9046d9-db1e-400f-ab86-0f04c2d790e9" />



Result:
Thus, the program to display queue elements using array is verified successfully.


 
EXP NO:14 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING ARRAY.
Aim:
To write a C program to insert elements in queue using array.

Algorithm:
1.	Declare global variables for the size, rear, front, and the queue itself.
2.	Define the enqueue function to add a float to the queue.
3.	Initialize the rear, front, and size of the queue as needed.
4.	Call the enqueue function as needed.

Program:

    #include <stdio.h>
    #define SIZE 5
    float queue[SIZE];
    int front = -1, rear = -1;
    
    void enqueue(float x) {
        if (rear == SIZE - 1)
            printf("Queue overflow\n");
        else {
            if (front == -1) front = 0;
            queue[++rear] = x;
            printf("%.2f inserted\n", x);
        }
    }
    
    int main() {
        enqueue(10.5);
        enqueue(20.2);
        enqueue(30.1);
        return 0;
    }


Output:

<img width="474" height="222" alt="image" src="https://github.com/user-attachments/assets/2625035e-32d4-4eaa-bfae-2f786089ea56" />


Result:
Thus, the program to insert elements in queue using array is verified successfully.



 
EXP NO:15 C FUNCTION TO DELETE ELEMENTS IN QUEUE USING ARRAY



Aim:

To create a function in C that deletes an element from a queue implemented using an array.

Algorithm:

1.	Check if the Queue is Empty
o	If the front pointer is -1, it means the queue is empty, and there are no elements to delete. Print a message indicating that the queue is empty.
2.	Delete the Front Element
o	If the queue is not empty, the element at the front index is deleted.
o	Increment the front pointer by 1 to remove the element and point to the next element in the queue.
3.	Check if the Queue Becomes Empty After Deletion:
o	After deletion, check if the front pointer has passed the rear pointer (front > rear). If this is true, reset both front and rear to -1, indicating that the queue is now empty.
4.	End the Function.



Program:

    #include <stdio.h>
    #define SIZE 5
    int queue[SIZE], front = -1, rear = -1;
    
    void dequeue() {
        if (front == -1)
            printf("Queue is empty\n");
        else {
            printf("Deleted: %d\n", queue[front++]);
            if (front > rear) front = rear = -1;
        }
    }
    
    int main() {
        queue[++rear] = 10;
        if (front == -1) front = 0;
        queue[++rear] = 20;
        queue[++rear] = 30;
        dequeue();
        dequeue();
        return 0;
    }


Output:

<img width="658" height="258" alt="image" src="https://github.com/user-attachments/assets/0ca19169-06d1-461e-b171-a67362cfe959" />



Result:
Thus, the function that deletes an element from a queue implemented using an array is verified successfully.
