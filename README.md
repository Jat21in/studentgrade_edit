# studentgrade_edit
#include <stdio.h>
int main() {
    printf("****************** Welcome To Program To Display Student Grade *************************");
    printf("\n");
    char studentname[100] ;
    char studentclass[3];
    char studentgrade ;
    int rollno ;
    float marks[5];
    double totalmarks , percentagemarks ;
   
    printf("Enter Student's Name :");
    fgets(studentname, 100 , stdin);

    printf("Enter Roll Number :");
    scanf("%d ",& rollno);
   
    printf("Enter Class :");
    fgets(studentclass , 3 ,stdin);

    
    printf("Enter Marks in 5 Subjects :");
    scanf("%f /n",& marks[0]);
    scanf("%f /n",& marks[1]);
    scanf("%f /n",& marks[2]);
    scanf("%f /n",& marks[3]);
    scanf("%f /n",& marks[4]);

    totalmarks = marks[0]+marks[1]+marks[2]+marks[3]+marks[4];

    percentagemarks = (totalmarks/500.0)*100;

    if(percentagemarks >= 95 )
       studentgrade= 'A';
    else if ((percentagemarks >=85 ) && (percentagemarks < 95))
       studentgrade ='a' ;
    else if ((percentagemarks >=75 ) && (percentagemarks < 85))
       studentgrade = 'B' ;
    else if ((percentagemarks >=55 ) && (percentagemarks < 75))
       studentgrade = 'C' ;
    else if ((percentagemarks >=40 ) && (percentagemarks < 55))
       studentgrade = 'D' ;
    else 
        studentgrade = 'E' ;

    printf("Student's Name is :");
    puts(studentname);
    printf("Class: ");
    puts(studentclass);
    printf("Roll Number is : %d \n",rollno);
    printf("Total Marks : %d",totalmarks);
    printf("Percentage Marks : %d", percentagemarks);
    printf("Grade : %c", studentgrade);

    return 0;
}
