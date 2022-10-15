# linked-list
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
****************************************
//creation of linked list
#include<bits/stdc++.h>
using namespace std;
struct node
{
    int data;
    struct node *next;
    node(int x)
    {
        data=x;
        next=NULL;
    }
};
int main()
{
    int n;cin>>n;
    struct node* head=NULL;
    struct node* temp;
    for(int i=0;i<n;i++)
    {
        int x;
        cin>>x;
        struct node* newnode=new node(x);
        
        
        if(head==NULL)
        {
            head=newnode;
            temp=newnode;
            temp->next=NULL;
        }
        else
        {
            head=newnode;
            head->next=temp;
            temp=head;
            
            
        }
    }
    temp=head;
    while(temp!=NULL)
    {
        cout<<temp->data<<"->";
        temp=temp->next;
    }
}
******************************??????????????????????????????????????????????????????? arey yar its new one
#include <bits/stdc++.h>
using namespace std;
struct node
{
    int data;
    struct node *next;
    node(int x)
    {
        data=x;
        next=NULL;
    }
};
struct node * head=NULL;
struct node *temp=head;
struct node *temp1=head;
void print(node *head)
{
    while(head!=NULL)
    {
        cout<<head->data<<"->";
        head=head->next;
    }
}

int main() {
	// your code goes here
	int t;
	cin>>t;
	for(int i=0;i<t;i++)
	{
	    int data;cin>>data;int n;cin>>n;
	    struct node *newnode=new node(data);
	    //newnode=node(data);
	    if(n==1 and head==NULL)
	    {
	        head=newnode;
	        temp=newnode;
	        temp->next=NULL;
	    }
	    else if(n==1 and head!=NULL)
	    {
	        temp->next=newnode;
	        temp=newnode;
	        temp->next=NULL;
	    }
	      else if(n==0 and  head==NULL)
	    {
	        head=newnode;
	        temp=newnode;
	        temp->next=NULL;
	    }
	    else if(n==0 and head!=NULL)
	    {
	        newnode->next=head;
	        head=newnode;
	    }
	}
	print(head);
	
	return 0;
}

