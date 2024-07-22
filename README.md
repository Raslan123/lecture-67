# lecture-67
#include <iostream>
using namespace std;
class Stack{
    public:
    int *arr;
    int size;
    int top;
    Stack(int size){
        this->size = size;
        arr = new int[size];
        top = -1;
    }
    void push(int element){
        if(size-top>1){
            top++;
            arr[top]= element;

        }else{
            cout<<"stack full";
        }
    }
    void pop(){
        if(top>=0){
           top--; 
        }
        else{
            cout<<"The stack is currently empty";
        }
    }
    void peek(){
        if(top<0)cout<<" No elements in the stack to peek "<<endl;
        else{
            cout<<" The element at the top of the stack is "<< arr[top]<<endl;
        }
    }
    bool isEmpty(){
        if(top<0){
            cout<<"The stack is currently empty "<<endl;;
            return true;
        }
        return false;
    }



};
int main(){
    Stack stack(5);
    stack.peek();
    stack.push(5);
    stack.push(10);
    stack.peek();
    stack.push(2);
    stack.pop();
    stack.peek();
    stack.push(100);

    return 0;


}
