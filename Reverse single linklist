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
void reverse(struct node *head)
{
    struct node *temp =NULL;
    temp=head;
    if(temp==NULL)
    {
        return;
    }
    else
    {
       reverse(temp->link);
       printf("%d  ", temp->info);
    }
}

int main()
{

    struct node *head = NULL;
    head = (struct node *)malloc(sizeof(struct node));
    head = NULL;
    int n;
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
    printf("\nThe reverse linklist is :  ");
    reverse(head);
    return 0;
}
