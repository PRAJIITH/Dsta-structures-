#include<stdio.h>
#include<malloc.h>
#include<stdlib.h>
struct node
{
    struct node *left;
    int data;
    struct node *right;
}*root=NULL,*newnode;
struct node *insert(struct node *root,int ele)
{
    if(root==NULL)
    {
        newnode=(struct node*)malloc(sizeof(struct node));
        newnode->data=ele;
        newnode->left=NULL;
        newnode->right=NULL;
        return(newnode);
    }
    else if(ele>root->data)
    {
        root->right=insert(root->right,ele);
    }
    else if(ele<root->data)
    {
        root->left=insert(root->left,ele);
    }
    return(root);
} 
void inorder(struct node *root)
{
    if(root!=NULL)
    {
        inorder(root->left);
        printf("%d\t",root->data);
        inorder(root->right);
    }
}
void preorder(struct node *root)
{
    if(root!=NULL)
    {
        printf("%d\t",root->data);
        preorder(root->left);
        preorder(root->right);
    }
}
void postorder(struct node*root)
{
    if(root!=NULL)
    {
        postorder(root->left);
        postorder(root->right);
        printf("%d\t",root->data);
    }
}

int main()
{
        int cho,ele;
        while(1)
        {
            printf("\n***MAIN MENU***\n");
            printf("\n1.insert\n2.inorder\n3.preorder\n4.postorder\n5.exit");
            printf("\nenter your choice:");
            scanf("%d",&cho);
            switch(cho)
            {
                case 1:printf("\nenter the element:");
                        scanf("%d",&ele);
                        root=insert(root,ele);
                break;
                case 2:inorder(root);
                break;
                case 3:preorder(root);
                break;
                case 4:postorder(root);
                break;
                case 5:exit(0);
                default:printf("enter the choice between 1 to 4");
            }   
        }
        return 0;
}
