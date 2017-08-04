# basicdatabase
/*its a C code for basis database showing file handling*/
/*user name is projectx and password is life

#include <stdio.h>
struct student {
char name[1000000];
long int rollno;
};
int main()
{
char name[]="projectx";
char pass[]="life";
char loginname[100];
char loginpass[100];
char end;
int ret1,ret2,num=0,i;

    printf("Enter your UserName to login =>");
    scanf("%s",&loginname);
    printf("Enter your Password to login =>");
    scanf("%s",&loginpass);

    ret1=strcmp(name,loginname);
    ret2=strcmp(pass,loginpass);

    if (ret1==0 && ret2==0)
        {
            printf("(1) Add Student\n");
            printf("(2) Show Student List\n");
            printf("(3) Edit Student Info\n");
            printf("(4) Put Student Details In Text File\n");
            printf("Please Select One Option =");
            scanf("%d",&num);
            for(;;)
            {

            if (num==1)
            {
                 struct student student1;
                 printf("Enter Student Name = ");
                 scanf("%s",&student1.name);
                 printf("Enter Student Rollno =");
                 scanf("%ld",&student1.rollno);


                printf("\n(1) Add Student\n");
                printf("(2) Show Student List\n");
                printf("(3) Edit Student Info\n");
                printf("(4) Put Student Details In Text File\n");
                printf("Please Select One Option =");
                scanf("%d",&num);

            }
            if (num==2)
            {   struct student student1;
                printf("Student Name = %s",student1.name);
                printf("  & Rollno = %ld\n\n",student1.rollno);
                printf("(1) Add Student\n");
                printf("(2) Show Student List\n");
                printf("(3) Edit Student Info\n");
                printf("(4) Put Student Details In Text File\n");
                printf("Please Select One Option =");
                scanf("%d",&num);
            }
            if(num==3)
            {
                struct student student1;
                printf("Enter New Name = ");
                scanf("%s",&student1.name);
                printf("Enter New Rollno = ");
                scanf("%ld",&student1.rollno);
                printf("\n(1) Add Student\n");
                printf("(2) Show Student List\n");
                printf("(3) Edit Student Info\n");
                printf("(4) Put Student Details In Text File\n");
                printf("Please Select One Option =");
                scanf("%d",&num);
            }
            if(num==4)
            {
                struct student student1;
                FILE *fp;
                fp=fopen("C:\\Users\\mm\\Desktop\\student.txt","a");
                fprintf(fp,"Student Name = %s\t",student1.name);
                fprintf(fp," & Rollno = %ld\n",student1.rollno);
                fclose(fp);
                printf("Your File Has Been Saved ON Following Address =>C:\\Users\\mm\\Desktop\\student.txt");
                printf("\n(1) Add Student\n");
                printf("(2) Show Student List\n");
                printf("(3) Edit Student Info\n");
                printf("(4) Put Student Details In Text File\n");
                printf("Please Select One Option =");
                scanf("%d",&num);
            }

            }

        }
        else
        {
            printf("Wrong Username Or Password");
        }
return 0;
}
