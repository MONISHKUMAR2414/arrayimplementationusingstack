# arrayimplementationusingstack


#include <stdio.h>

#define MAX 5

int stack[MAX], top = -1;

int IsFull();
int IsEmpty();

void Push(int x);
void Pop();
void Display();
void Top();

int main() {

    int choice, e;

    do {
        printf("1. PUSH\n2. POP\n3. DISPLAY\n4. TOP\n"); 

        printf("Enter the Choice: ");
        scanf("%d", &choice);

        switch (choice) {

            case 1:
                printf("Enter the Element: ");
                scanf("%d", &e);
                Push(e);
                break;

            case 2:
                Pop();
                break;

            case 3:
                Display();
                break;

            case 4:
                Top();
                break;

        }

    } while (choice <= 4);
    return 0;

}

int IsFull(){
    
    if (top == MAX -1)
      return 1;
      
    else 
      return 0;
      
     
}


int IsEmpty(){
    if (top==-1)
     return 1;
     
    else 
      return 0;
      
}


void Push(int x){
    if (IsFull())
        printf("The Stack is Over flow\n");
    
    else{
        top = top +1;
       stack[top]= x;
    } 
       
      
}

void Pop(){
    if (IsEmpty())
    printf("The Stack is Under flow \n");
    
    else {
        printf("%d\n", stack [top]);
        top = top -1;
        
    }
}

void Top(){
    
     if (IsEmpty())
        printf("The Stack is Under flow \n");
    
    else {
         printf("%d\n", stack [top]);
    }
}


void Display(){
    int i;
    
     if (IsEmpty())
        printf("The Stack is Under flow \n");
    else{
        for (i= MAX-1; i<0; i--){
            
            printf("%d\t", stack[i]);
        }
        }
}
        

