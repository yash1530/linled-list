# linled-list
//ctreation of ll
#include <bits/stdc++.h>
using namespace std;

struct node
{
    int data;
    node *next;
    node(int x)
    {
        data=x;
        next=NULL;
    }
};
void pll(node *head)
{
    node *cur=head;
    while(cur!=NULL)
    {
        cout<<cur->data<<" ";
        cur=cur->next;
    }
}
int main()
{
    node *head=new node(10);
    head->next=new node(20);
    head->next->next=new node(30);
    head->next->next->next=new node(40);
    pll(head);

	
	return 0;
}
****************************************************************************************************
  inserting element at first and end in ll
	#include<bits/stdc++.h>
using namespace std;
struct node{
    int data;
    node *next;
    node(int x)
    {
        data=x;
        next=NULL;
    }
    
};
void yash(node *&head,int n)
{
   /* node *temp=new node(n);
    temp->next=head;
    head=temp;*/
    node *temp=new node(n);
    node *cur=head;
    if(head==NULL)
    {
        head=temp;
    }
    else
    {
        while(cur->next!=NULL)
        {
            cur=cur->next;
        }
        cur->next=temp;
    }
    
}
int vin(node *head)
{
    node *temp=head;
    while(temp!=NULL)
    {
        cout<<temp->data<<" ";
        temp=temp->next;
    }
}
int main()
{
    node *head=NULL;
    yash(head,1);
    yash(head,2);
    yash(head,3);
   // head->next->next=new node(30);
    vin(head);
    
    
}

