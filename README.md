#include<stdio.h>
#include<malloc.h>
#include<string.h>
#define Linklist struct student
struct student
{
   int number;
   char name[10];
   Linklist *next;
} ;
Linklist* creat_node()
{
   Linklist *node=NULL,*temp=NULL;
   int number;
   char name[10];
   printf("Input number and name:\n");
   scanf("%d%s",&number,name);
   while(number!=0)
   {
    node=(Linklist*)malloc(sizeof(Linklist));
    node->number=number;
    strcpy(node->name,name);
    node->next=temp;
    temp=node;
    printf("Input number and name:\n");
    scanf("%d%s",&number,name);
   } 
   return temp;
}
