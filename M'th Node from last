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
void del(struct node *head, int n)
{
    struct node *temp = head;
    int l = 0;
    if (head == NULL)
    {
        printf("\nThe linked list is empty\n");
    }
    else
    {

        while (temp != NULL)
        {

            temp = temp->link;
            l++;
        }
        if (n > l)
        {
            printf("Invalid input");
        }
        else
        {
            int i;
            for (i = 0; i < l - n; i++)
            {
                head = head->link;
            }
            printf("The %dth node from the last is %d", n, head->info);
        }
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
    int m;
    display(head);
    printf("\nEnter the M'th Node : ");
    scanf("%d", &m);
    del(head, m);
    return 0;
}
