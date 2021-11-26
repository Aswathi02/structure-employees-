//structure-employees
#include <stdio.h>
typedef struct
{
    char name[30];
    int age;
    double salary;
    int phonenumber;
} 
Employee;
 
int main()
{
    //number of employees
    int n=20;
    Employee employees[n];
    printf("Enter %d Employee Details \n \n",n);
    for(int i=0; i<n; i++){
        printf("Employee %d:- \n",i+1);

        //Name
        printf("Name: ");
        scanf("%[^\n]s",employees[i].name);

        //Age
        printf("Age: ");
        scanf("%d",&employees[i].age);
        // phone number
        printf("Phone number:");
        scanf("%d",&employees[i].phonenumber);
        //Salary
        printf("Salary: ");
        scanf("%lf",&employees[i].salary);
       
        //to consume extra '\n' input
        char ch = getchar();
 
        printf("\n");
    }
 
    //Displaying Employee details
    printf("-------------- All Employees Details ---------------\n");
    for(int i=0; i<n; i++){
        printf("Name \t: ");
        printf("%s \n",employees[i].name);
 
        printf("age \t: ");
        printf("%d \n",employees[i].age);
      
      printf("phone number \t:");
      printf("%d \n",employees[i].phonenumber);
        printf("Salary \t: ");
        printf("%.2lf \n",employees[i].salary);
 
        printf("\n");
    }
 
    return 0;
}
