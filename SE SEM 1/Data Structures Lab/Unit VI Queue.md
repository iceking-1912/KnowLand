---
tags:
  - 2024-
  - COMP_PROGRAM
  - Data_Structures_and_Algorithms
  - cpp
parent:
  - "[[SE SEM 1]]"
Purpose:
  - Knowledge
relative:
  - "[[Fundamentals of Data Structures -]]"
  - "[[SE SEM 1]]"
---
# Unit VI Queue
###  Queue Fundamentals: FIFO (First-In-First-Out) Principle, Abstract Data Type (ADT)





```c++
# include <iostream>

// Node class representing each element in the linked list
class Node {
public:
    int data;
    Node* next;

    // Constructor to initialize node with data and set next pointer to nullptr
    Node(int value) : data(value), next(nullptr) {}
};

// Queue class implementing the Add-Queue-Dequeue (AQD) queue using a linked list
class Queue {
private:
    Node* front;  // Pointer to the front of the queue
    Node* rear;   // Pointer to the rear of the queue

public:
    // Constructor to initialize an empty queue
    Queue() : front(nullptr), rear(nullptr) {}

    // Destructor to free memory allocated for each node in the queue
    ~Queue() {
        while (front != nullptr) {
            Node* temp = front;
            front = front->next;
            delete temp;
        }
    }

    // Method to add an element at the end of the queue
    void enqueue(int value) {
        Node* newNode = new Node(value);
        if (rear == nullptr) {
            front = newNode;
            rear = newNode;
        } else {
            rear->next = newNode;
            rear = newNode;
        }
    }

    // Method to remove an element from the front of the queue
    int dequeue() {
        if (front == nullptr) {
            throw std::runtime_error("Queue is empty");
        }
        int value = front->data;
        Node* temp = front;
        front = front->next;
        if (front == nullptr) {
            rear = nullptr;
        }
        delete temp;
        return value;
    }

    // Method to check if the queue is empty
    bool isEmpty() const {
        return front == nullptr;
    }

    // Method to get the front element of the queue without removing it
    int peek() const {
        if (front == nullptr) {
            throw std::runtime_error("Queue is empty");
        }
        return front->data;
    }
};

int main() {
    Queue queue;

    // Enqueue elements onto the queue
    queue.enqueue(10);
    queue.enqueue(20);
    queue.enqueue(30);

    // Dequeue elements from the queue
    while (!queue.isEmpty()) {
        std::cout << "Dequeued: " << queue.dequeue() << std::endl;
    }

    return 0;
```


### Queue Implementation: Using Sequential Organization
###  Queue Operations: Enqueue, Dequeue, Peek, etc.
###  Queue Variations: Circular Queue, Deque (Double-Ended Queue)

Here's a detailed overview of the circular queue and deque (double-ended queue) variations:

**Circular Queue:**

A circular queue is a type of queue where elements are arranged in a circle and each element points to the next position. This allows for efficient addition and removal of elements from both ends.

**Properties:**

*   Elements can be added or removed from either end using a constant time complexity.
*   The array size remains fixed throughout the lifetime of the data structure.
*   The circular nature of the queue ensures that there are no gaps in the data.

**Operations:**

*   `enqueue(element)` - adds an element to the end of the queue
*   `dequeue()` - removes an element from the front of the queue

**Example Code (Python):**
```c++
#include <iostream>
using namespace std;
class CircularQueue {
private:
    int maxSize;
    int head;
    int tail;
    int* arr;

public:
    // Constructor to initialize the queue with maximum size and array
    CircularQueue(int max_size) {
        this->maxSize = max_size;
        this->head = 0;
        this->tail = 0;
        this->arr = new int[maxSize];
    }

    // Destructor to free dynamically allocated memory
    ~CircularQueue() {
        delete[] arr;
    }

    // Method to add an element at the front of the queue
    void enqueue(int value) {
        if (isFull()) {
            std::cout << "Circular queue is full" << std::endl;
            return;
        }
        arr[tail] = value;
        tail = (tail + 1) % maxSize;
    }

    // Method to remove an element from the front of the queue
    int dequeue() {
        if (isEmpty()) {
            std::cout << "Circular queue is empty" << std::endl;
            return -1; // Return a sentinel value to indicate failure
        }
        int temp = arr[head];
        head = (head + 1) % maxSize;
        return temp;
    }

    // Method to add an element at the rear of the queue
    void enqueueR(int value) {
        if (isFull()) {
            std::cout << "Circular queue is full" << std::endl;
            return;
        }
        arr[tail] = value;
        tail = (tail + 1) % maxSize;
    }

    // Method to remove an element from the rear of the queue
    int dequeueR() {
        if (isEmpty()) {
            std::cout << "Circular queue is empty" << std::endl;
            return -1; // Return a sentinel value to indicate failure
        }
        int temp = arr[head];
        head = (head + 1) % maxSize;
        return temp;
    }

    // Method to check if the queue is full
    bool isFull() {
        return tail == head;
    }

    // Method to check if the queue is empty
}
```

**Deque (Double-Ended Queue):**

A deque (double-ended queue) is a type of queue where elements can be added or removed from both ends.

**Properties:**

*   Elements can be added or removed from either end using constant time complexity.
*   The array size remains fixed throughout the lifetime of the data structure.
*   This allows for efficient insertion and removal of elements at any position in the deque.

**Operations:**

*   `enqueue(element)` - adds an element to the front or rear of the deque
*   `dequeue()` - removes an element from the front of the deque

**Example Code (Python):**
```c++
#include <iostream>
#include <stdexcept> // for exception handling


class CircularQueue {
private:
    int maxSize;
    int head;
    int tail;
    int* arr;
    int size; // Add a size variable to track the number of elements

public:
    // Constructor
    CircularQueue(int max_size) : maxSize(max_size), head(0), tail(0), size(0) {
        arr = new int[maxSize];
    }

    // Destructor
    ~CircularQueue() {
        delete[] arr;
    }

    //Check if queue is empty
    bool isEmpty() const { return size == 0; }

    //Check if queue is full
    bool isFull() const { return size == maxSize; }


    // Enqueue (add to rear)
    void enqueue(int value) {
        if (isFull()) {
            throw std::runtime_error("Circular queue is full"); //Throw exception instead of printing
        }
        arr[tail] = value;
        tail = (tail + 1) % maxSize;
        size++;
    }

    // Dequeue (remove from front)
    int dequeue() {
        if (isEmpty()) {
            throw std::runtime_error("Circular queue is empty"); //Throw exception instead of printing
        }
        int value = arr[head];
        head = (head + 1) % maxSize;
        size--;
        return value;
    }

    //Enqueue (add to front) - added for completeness.  This is less common for a circular queue
    void enqueueFront(int value) {
        if (isFull()) {
            throw std::runtime_error("Circular queue is full");
        }
        head = (head -1 + maxSize) % maxSize; //Decrement head, wrap around if needed
        arr[head] = value;
        size++;
    }

    //Dequeue (remove from rear) - added for completeness. This is less common for a circular queue
    int dequeueRear() {
        if (isEmpty()) {
            throw std::runtime_error("Circular queue is empty");
        }
        tail = (tail - 1 + maxSize) % maxSize; //Decrement tail, wrap around if needed
        size--;
        return arr[tail];
    }

};


int main() {
    CircularQueue q(5);
    q.enqueue(10);
    q.enqueue(20);
    std::cout << q.dequeue() << std::endl; // Output: 10

    return 0;
}
```

**Advantages and Disadvantages:**

*   Circular Queue:
    *   Advantages: Efficient addition and removal of elements from both ends.
    *   Disadvantages: Elements are stored in a circular array, which may lead to performance issues if the queue is full or empty frequently.
*   Deque (Double-Ended Queue):
    *   Advantages: Flexible data structure that supports insertion and removal at any position.
    *   Disadvantages: May not be suitable for all scenarios due to potential performance issues.

These variations of queues are essential tools in various programming applications, such as real-time systems, network protocols, and databases.
### Priority Queue: Concept and Types (Ascending/Descending)

