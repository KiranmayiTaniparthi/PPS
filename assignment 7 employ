#include <stdio.h>

struct employee
{
    char name[50], post[50], id[50];
    float bas, ta, hra, gross;
};

int main()
{
    int i, n;
    struct employee a[100];

    printf("Enter the number of employees: ");
    scanf("%d", &n);

    for(i = 0; i < n; i++)
    {
        printf("\nEnter details of Employee %d\n", i+1);

        printf("Enter Employee ID: ");
        scanf("%49s", a[i].id);

        printf("Enter Name: ");
        scanf("%49s", a[i].name);

        printf("Enter Basic Salary: ");
        scanf("%f", &a[i].bas);

        a[i].ta = (23 * a[i].bas) / 100;
        a[i].hra = (30 * a[i].bas) / 100;

        a[i].gross = a[i].bas + a[i].ta + a[i].hra;

        if(a[i].bas >= 100000)
        {
            sprintf(a[i].post, "Manager");
        }
        else if(a[i].bas >= 80000)
        {
            sprintf(a[i].post, "Sub Manager");
        }
        else if(a[i].bas >= 60000)
        {
            sprintf(a[i].post, "Senior Clerk");
        }
        else
        {
            sprintf(a[i].post, "Junior Clerk");
        }
    }

    printf("\n\n---------------- EMPLOYEE PAYROLL REPORT ----------------\n");

    printf("\n%-10s %-15s %-12s %-12s %-12s %-12s %-15s\n",
           "ID", "Name", "Basic", "TA", "HRA", "Gross", "Post");

    printf("-----------------------------------------------------------------------------------------------\n");

    for(i = 0; i < n; i++)
    {
        printf("%-10s %-15s %-12.2f %-12.2f %-12.2f %-12.2f %-15s\n",
               a[i].id, a[i].name, a[i].bas,
               a[i].ta, a[i].hra, a[i].gross, a[i].post);
    }

    printf("-----------------------------------------------------------------------------------------------\n");

    return 0;
}
