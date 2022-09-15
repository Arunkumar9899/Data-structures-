#include <stdio.h>
#include <malloc.h>
#include <stdlib.h>
struct node
{
  int data;
  struct node *next;
}*p,*newnode,*head=NULL,*t;

void create()
{
    int i,n,ele;
    printf("Enter the number of elements to be created");
    scanf("%d",&n);
    for(i=0;i<n;i++)
    {
        newnode = (struct node*)malloc(sizeof(struct node));
        printf("Enter the element : ");
        scanf("%d",&ele);
        newnode->data = ele;
        newnode->next = NULL;
        if(head==NULL)
        {
            head=newnode;
            p=newnode;

        }
        else
        {
            for(p=head; p->next!= NULL; p=p->next);
            p->next=newnode;
            p=newnode;
        }
    }
}
void insert_b()
{
    int a;
    printf("enter the value");
    scanf("%d",&a);
    newnode = (struct node*)malloc(sizeof(struct node));
    newnode->data = a;
    newnode->next = head;
    head = newnode;
}
void insert_e()
{
     newnode = (struct node*)malloc(sizeof(struct node));
     int a;
     printf("enter the value");
     scanf("%d",&a);
     newnode->data = a;
     newnode->next = NULL;
     //struct node *t = head;
     while(t->next != NULL)
     {
            t = t->next;
     }
     t->next = newnode;
}
void insert_any()
{
    newnode = malloc(sizeof(struct node));
    int a,i,pos;
    printf("enter the a value and pos");
    scanf("%d%d",&a,&pos);
    newnode->data = a;
    struct node *t = head;
    for(int i=2; i < pos; i++) {
      if(t->next != NULL) {
        t = t->next;
      }
    }
    newnode->next = t->next;
    t->next = newnode;
}
void delete_b()
{
    int ele;
    p=head;
    head=p->next;
    ele=p->data;
    free(p);
    printf("The deleted element = %d",ele);
}
void delete_e()
{
   // struct node* t = head;
    int ele;
    for(p=head;p->next!=NULL;p=p->next)
        t=p;
    t->next=NULL;
    ele=p->data;
    free(p);
    printf("The deleted element = %d",ele);
}
void delete_any_position()
{
    int pos,i,ele;
    printf("\nEnter the Position: ");
    scanf("%d",&pos);

    for(p=head,i=1; i<pos; p=p->next,i++)
        t=p;
    t->next=p->next;
    ele=p->data;
    free(p);
    printf("\nThe deleted element is ->:%d ",ele);
}
void display()
{
    if(head==NULL)
        printf("SLL is Empty");
    else
        for(p=head; p!=NULL; p=p->next)
            printf("%d -> ",p->data);
}

void main()
{
    int ch;
    do
    {
    printf("\n1.Create\n2.insert_b\n3.insert_e\n4.insert_any\n5.Display\n6.delete_b\n7.delete_e\n8.delete at any position\n9.exit\n");
    printf("enter the choice");
    scanf("%d",&ch);
    switch(ch)
    {
        case 1:
            create();
            break;
        case 2:
            insert_b();
            break;
        case 3:
            insert_e();
            break;
        case 4:
            insert_any();
            break;
        case 5:
            display();
            break;
        case 6:
            delete_b();
            break;
        case 7:
            delete_e();
            break;
        case 8:
            delete_any_position();
            break;
        case 9:
            exit(0);
        default:
            printf("\n wrong input");
    }
    } while(ch>=1 && ch<=9);
}
