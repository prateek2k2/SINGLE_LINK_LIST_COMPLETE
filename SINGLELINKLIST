#include <stdio.h>
#include <stdlib.h>
struct node
{
    int info;
    struct node *link;
};
void display(struct node *head)
{
    if (head == NULL)
    {
        printf("No node is found");
    }
    else
    {
        struct node *temp = head;
        printf("The link list is\n");
        while (temp != NULL)
        {
            printf("%d ", temp->info);
            temp = temp->link;
        }
    }
}
void traverse(struct node *head)
{
    if (head == NULL)
    {
        printf("No node is found");
    }
    else
    {
        struct node *temp = head;
        printf("The traverse link list is\n");
        while (temp != NULL)
        {
            printf("%d", temp->info);
            temp = temp->link;
        }
    }
}
void check_list(struct node *head)
{
    if (head == NULL)
    {
        printf("Empty linklist\n");
    }
    else
    {
        printf("Link list is not empty");
    }
}
void insert_begin(struct node *head, int value)
{
    struct node *new_node = (struct node *)malloc(sizeof(struct node));
    if (new_node == NULL)
    {
        printf("Overflow");
    }
    else
    {
        new_node->info = value;
        new_node->link = head;
        head = new_node;
    }
    printf("The linklist after inserting at begin is \n");
    display(head);
}
void insert_end(struct node *head, int value)
{
    struct node *new_node1 = (struct node *)malloc(sizeof(struct node));
    new_node1->link = NULL;
    new_node1->info = value;
    struct node *temp = head;
    if (new_node1 == NULL)
    {
        printf("Overflow");
    }
    else
    {
        if (head == NULL)
        {
            head = new_node1;
        }
        else
        {

            while (temp->link != NULL)
            {
                temp = temp->link;
            }
            temp->link = new_node1;
        }
        temp = head;
        printf("The linklist after inserting at end is \n");
    }
    display(head);
}
void insert_any(struct node *head, int value, int pos)
{
    int i = 1;
    struct node *new_node2 = (struct node *)malloc(sizeof(struct node));
    new_node2->link = NULL;
    new_node2->info = value;
    struct node *temp = (struct node *)malloc(sizeof(struct node));

    if (new_node2 == NULL)
    {
        printf("OVERFLOW");
    }
    else
    {
        if (head == NULL)
        {
            if (pos == 0)
            {
                head = new_node2;
            }
        }
        else if (pos == 0)
        {
            new_node2->link = head;
            head = new_node2;
        }
        else
        {
            temp = head;
            while (i < pos - 1 && temp->link != NULL)
            {
                temp = temp->link;
                i++;
            }
            if (pos - 1 == i)
            {
                new_node2->link = temp->link;
                temp->link = new_node2;
            }
            else
            {
                printf("Out of range");
            }
        }
    }
    printf("Element after instertion: ");
    display(head);
}
void del_first(struct node *head)
{
    struct node *temp = head;
    if (head == NULL)
    {
        printf("NO ELEMENT");
    }
    else
    {
        temp = head;
        head = head->link;
        free(temp);
    }
    printf("List after deletion\n");
    display(head);
}
void del_end(struct node *head)
{
    struct node *temp = head;
    if (head == NULL)
    {
        printf("NO ELEMENT");
    }
    else if (head->link == NULL)
    {
        free(head);
        head = NULL;
    }
    else
    {
        for (temp = head; temp->link->link; temp = temp->link)
        {
        }
        free(temp->link);
        temp->link = NULL;
    }
    printf("Delete from the end\n");
    display(head);
}
void del_any_pos(struct node *head, int pos)
{
    int i = 1;
    struct node *temp = head;
    if (head == NULL)
    {
        printf("List is empty");
    }
    else
    {
        if (pos == 0)
        {
            free(head);
            head->link = NULL;
        }
        else
        {
            temp = head;
            for (i = 1; i < pos - 1; i++)
            {
                temp = temp->link;
            }
            struct node *del = temp->link;
            temp->link = temp->link->link;
            printf("\nElement deleted is : %d\n", del->info);
            del->link = NULL;
            free(del);
        }
    }
    temp = head;
    printf("Element after deletion is ");
    display(head);
}
void count_node(struct node *head)
{
    int c = 0;
    if (head == NULL)
    {
        printf("No node is found");
    }
    else
    {
        struct node *temp = head;
        while (temp != NULL)
        {
            c = c + 1;
            temp = temp->link;
        }
    }
    printf("The number of node present is  %d\n", c);
}
void search(struct node *head, int val, int n)
{
    int i, c = 0;
    struct node *temp = head;
    if (head == NULL)
    {
        printf("List is empty");
    }
    else
    {
        temp = head;
        while (temp != NULL)
        {
            temp = temp->link;
            c = c + 1;
            if (temp->info == val)
            {
                printf("Value found at node  %d at address %d", c, temp->link);
            }
        }
    }
}
void del_key(struct node *head)
{
    printf("Enter Key: ");
    int key;
    scanf("%d", &key);
    struct node *temp = (struct node *)malloc(sizeof(struct node));
    temp = head;
    if (temp == NULL)
    {
        printf("The list is empty");
    }
    else if (temp->info == key)
    {
        struct node *ptr;
        ptr = temp->link;
        head = ptr;
        free(temp);
    }
    else
    {
        for (temp = head; temp->link->info != key; temp = temp->link)
        {
            ;
        }
        if (temp->link == NULL)
        {
            printf("The key is not found");
        }
        else
        {

            struct node *p1 = temp->link;
            temp->link = p1->link;
            free(p1);
        }
    }
    display(head);
}

int main()
{
    int val, pos;
    int option;
    struct node *head = NULL;
    head = (struct node *)malloc(sizeof(struct node));
    head = NULL;
    int n, i;
    struct node *N = NULL;
    struct node *M = NULL;
    printf("Enter -1 to stop\n");
    printf("Enter the data:  ");
    scanf("%d", &n);
    while (n != -1)
    {
        M = (struct node *)malloc(sizeof(struct node));
        if (head == NULL)
        {
            N = (struct node *)malloc(sizeof(struct node));
            N->info = n;
            N->link = NULL;
            head = N;
        }
        else
        {
            M = (struct node *)malloc(sizeof(struct node));
            M->info = n;
            M->link = NULL;
            N->link = M;
            N = M;
        }
        printf("Enter the data:  ");
        scanf("%d", &n);
    }
    display(head);
    printf("\nEnter your choice \n1 To trasverse\n2 To check list\n3 To insert at the beginning\n4 To insert at the end\n5 To instert at any position \n6 To delete first element \n7 To delete from end\n8 To delete element at any pos\n9 Count the number of node\n10 Search the elemnet from the linklist\n11 To delete a key from node\n ");
    scanf("%d", &option);
    switch (option)
    {
    case 1:
    {
        traverse(head);
        break;
    }
    case 2:
    {
        check_list(head);
        break;
    }
    case 3:
    {
        printf("Enter the element to insert at the begin\n ");
        scanf("%d", &val);
        insert_begin(head, val);
        break;
    }
    case 4:
    {
        printf("Enter the element at the end of the list\n ");
        scanf("%d", &val);
        insert_end(head, val);
        break;
    }
    case 5:
    {
        printf("Enter the element to be inserted at any option");
        scanf("%d", &val);
        printf("Enter the position");
        scanf("%d", &pos);
        insert_any(head, val, pos);
        break;
    }
    case 6:
    {
        del_first(head);
        break;
    }
    case 7:
    {
        del_end(head);
        break;
    }
    case 8:
    {
        printf("Enter the position from which element is to be deleted:");
        scanf("%d", &pos);
        del_any_pos(head, pos);
        break;
    }
    case 9:
    {
        count_node(head);
        break;
    }
    case 10:
    {
        printf("Enter the value to be search  :");
        scanf("%d", &val);
        search(head, val, n);
        break;
    }
    case 11:
    {
        ;
        del_key(head);
        break;
    }
    default:
    {
        printf("Wrong Key :");
        break;
    }
        return 0;
    }
}
