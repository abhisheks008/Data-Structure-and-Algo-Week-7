#include<stdio.h>
#include<stdlib.h>
struct node
{
int data;
struct node *next;
};
struct node *even=NULL;
struct node *odd=NULL;
struct node *ll=NULL;
void insert(int data)
{
struct node *link,*present;
link=(struct node *)malloc(sizeof(struct node));
link->data=data;
link->next=NULL;
if(ll==NULL)
{
ll=link;
ll->next=link;
return;
}
present=ll;
while(present->next!=ll)
present=present->next;
present->next=link;
link->next=ll;
}
void display(struct node *h)
{
struct node *ptr=h;
while(ptr->next!=h)
{
printf("%d ",ptr->data);
ptr=ptr->next;
}
printf("%d ",ptr->data);
}
void split()
{
struct node *ll1;
struct node *link;
struct node *present;
ll1=ll;
while(ll1->next!=ll)
{
struct node *link = (struct node*) malloc(sizeof(struct node));
link->data =ll1->data;
link->next = NULL;
if(ll1->data%2==0)
{
if(even==NULL)
{
even=link;
even->next=link;
ll1=ll1->next;
continue;
}
else
{
present=even;
while(present->next!=even)
{
present=present->next;
}
present->next=link;
link->next=even;
}
ll1=ll1->next;
}
else
{
if(odd==NULL)
{
odd=link;
odd->next=link;
ll1=ll1->next;
continue;
}
else
{
present=odd;
while(present->next!=odd)
{
present=present->next;
}
present->next=link;
link->next=odd;
}
ll1=ll1->next;
}
}
link = (struct node*) malloc(sizeof(struct node));
link->data = ll1->data;
link->next = NULL;
if(ll1->data%2 == 0)
{
present = even;
while(present->next!=even)
{
present=present->next;
}
present->next=link;
link->next=even;
}
else
{
present=odd;
while(present->next!=odd)
{
present=present->next;
}
present->next=link;
link->next=odd;
}
}
int main()
{
int data,i;
for(i=1;i<=7;i++)
{
scanf("%d",&data);
insert(data);
data=0;
}
split();
display(odd);
printf("\n");
display(even);
return 0;
}
