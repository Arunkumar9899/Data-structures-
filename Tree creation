#include<stdio.h>
#include<stdlib.h>
#include<malloc.h>
struct node
{
    int data;
    struct node *l,*r;

}*root=NULL,*newnode;

struct node* create(struct node*root,int ele)
{
    if(root==NULL)
    {
        newnode=(struct node*)malloc(sizeof(struct node));
        newnode->data=ele;
        newnode->l=NULL;
        newnode->r=NULL;
        return(newnode);
    }
    else if(ele < root->data)
        root->l=create(root->l,ele);
    else if(ele > root->data)
        root->r=create(root->r,ele);
     return(root);
}
void inorder(struct node *root)
{
    if(root==NULL)
        return;
        inorder(root->l);
        printf("%d ",root->data);
        inorder(root->r);
}
void preorder(struct node *root)
{
    if(root!=NULL)
    {
        printf("%d ",root->data);
        preorder(root->l);
        preorder(root->r);
    }
}
void postorder(struct node *root)
{
    if(root!=NULL)
    {
        postorder(root->l);
        postorder(root->r);
        printf("%d ",root->data);

    }
}
void main()
{
    int ch,ele;
    do
    {
    printf("\n\n1.create\n2.inorder\n3.preorder\n4.postorder\n5.exit");
    printf("\n\nEnter your choice");
    scanf("%d",&ch);
    switch(ch)
    {
        case 1:
            printf("enter the element");
            scanf("%d",&ele);
            root=create(root,ele);
            break;
        case 2:
            inorder(root);
            break;
        case 3:
            preorder(root);
            break;
        case 4:
            postorder(root);
            break;
        case 5:
            exit(0);
        default:
            printf("\nWrong Choice!!");
    }
    }while(ch>=0 && ch<=5);
}
