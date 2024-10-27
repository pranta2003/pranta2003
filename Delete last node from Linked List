#include <iostream>
using namespace std;


struct Node
{
    int data;
    Node* next;
};


void insertAtBeginning(Node*& head, int value)
{
    Node* newNode = new Node();
    newNode->data = value;
    newNode->next = head;
    head = newNode;
}

void insert(Node*& head, int value)
{
    Node* newNode = new Node();
    newNode->data = value;
    newNode->next = nullptr;

    if (head == nullptr)
    {
        head = newNode;
    }
    else
    {
        Node* temp = head;
        while (temp->next != nullptr)
        {
            temp = temp->next;
        }

        temp->next = newNode;
    }
}


void deleteLastNode(Node*& head)
{
    if (head == nullptr)
    {

        cout << "List is already empty." << endl;
        return;
    }

    if (head->next == nullptr)
    {

        delete head;
        head = nullptr;
        return;
    }


    Node* temp = head;
    while (temp->next->next != nullptr)
    {
        temp = temp->next;
    }


    delete temp->next;
    temp->next = nullptr;
}

void display(Node* head)
{
    Node* temp = head;
    while (temp != nullptr)
    {
        cout << temp->data << " -> ";
        temp = temp->next;
    }
    cout << "NULL" << endl;
}

int main()
{
    Node* head = nullptr;
    int values[3];


    cout << "Enter 3 values for the linked list: ";
    for (int i = 0; i < 3; i++)
    {
        cin >> values[i];
        insert(head, values[i]);
    }


    insertAtBeginning(head, 5);


    cout << "Linked list before deletion: ";
    display(head);

    deleteLastNode(head);

    cout << "Linked list after deletion: ";
    display(head);

    return 0;
}
