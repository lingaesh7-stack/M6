# EX-26-AREA-OF-RECTANGLE-USING- POINTER
## AIM
To write a C Program to find area of rectangle using pointer.

## ALGORITHM
1.	Start the program.
2.	Read two numbers.
3.	Calculate the area of rectangle using the formula area=(x)(*y)
4.	Display the result.
5.	Stop the program.

## PROGRAM

#include <stdio.h>

int main() {
    float length, breadth, area;
    float *p1, *p2;  // pointers for length and breadth

    printf("Enter length of rectangle: ");
    scanf("%f", &length);

    printf("Enter breadth of rectangle: ");
    scanf("%f", &breadth);

    // Assign addresses to pointers
    p1 = &length;
    p2 = &breadth;

    // Calculate area using pointers
    area = (*p1) * (*p2);

    printf("\nArea of Rectangle = %.2f\n", area);

    return 0;
}


## OUTPUT
		       	
<img width="453" height="127" alt="C26" src="https://github.com/user-attachments/assets/bbeffab0-9a8f-4624-baed-a97673960ce5" />


## RESULT
Thus the program to find area of rectangle using pointer has been executed successfully
 
 


# EX-27-DYNAMIC-MEMORY-ALLOCATION
## AIM
To write a C Program to print 'WELCOME' using malloc() and free().

## ALGORITHM
1.	Start the program.
2.	Read a string variable.
3.	Allocate memory using malloc().
4.	Display the string.
5.	Remove the allocated memory using free().
6.	Stop the program.

## PROGRAM

#include <stdio.h>
#include <stdlib.h>  // for malloc() and free()

int main() {
    char *str;

    // Allocate memory for 8 characters ("WELCOME" + '\0')
    str = (char *)malloc(8 * sizeof(char));

    if (str == NULL) {
        printf("Memory allocation failed!\n");
        return 1;
    }

    // Store the word "WELCOME" in the allocated memory
    str[0] = 'W';
    str[1] = 'E';
    str[2] = 'L';
    str[3] = 'C';
    str[4] = 'O';
    str[5] = 'M';
    str[6] = 'E';
    str[7] = '\0';  // Null terminator for string

    // Print the string
    printf("%s\n", str);

    // Free the allocated memory
    free(str);

    return 0;
}


## OUTPUT


<img width="693" height="51" alt="C27" src="https://github.com/user-attachments/assets/10b1820c-626e-478e-900e-1b2754edb6dc" />

## RESULT
Thus the program to print 'WELCOME' using malloc() and free() has been executed successfully
 
.



# EX-28-STUDENT-INFORMATION-USING-STRUCTURE

## AIM

To write a C Program to store the student information and display it using structure.

## ALGORITHM

1.	Start the program.
2.	Create a student structure with name, roll number and marks as members.
3.	Using structure variable read the structure members and print them.
4.	Stop the program.

## PROGRAM

#include <stdio.h>

struct Employee {
    int id;
    char name[50];
    float basic, hra, da, gross;
};

int main() {
    struct Employee emp[3];  // array of 3 employees
    int i;

    printf("Enter details of 3 employees:\n");

    for (i = 0; i < 3; i++) {
        printf("\n--- Employee %d ---\n", i + 1);
        printf("Enter Employee ID: ");
        scanf("%d", &emp[i].id);

        printf("Enter Name: ");
        scanf("%s", emp[i].name);

        printf("Enter Basic Salary: ");
        scanf("%f", &emp[i].basic);

        printf("Enter HRA: ");
        scanf("%f", &emp[i].hra);

        printf("Enter DA: ");
        scanf("%f", &emp[i].da);

        // Calculate Gross Salary
        emp[i].gross = emp[i].basic + emp[i].hra + emp[i].da;
    }

    printf("\n\n----- Employee Details with Gross Salary -----\n");
    printf("ID\tName\t\tGross Salary\n");
    printf("--------------------------------------------\n");

    for (i = 0; i < 3; i++) {
        printf("%d\t%-10s\t%.2f\n", emp[i].id, emp[i].name, emp[i].gross);
    }

    return 0;
}






## OUTPUT
<img width="696" height="802" alt="C28" src="https://github.com/user-attachments/assets/a705db5b-8dcd-4e24-841e-1e4de252ddf5" />


## RESULT

Thus the program to store the student information and display it using structure has been executed successfully
 
 


# EX-29-EMPLOYEE-STRUCTURE-SALARY-CALCULATION

## AIM

To write a C Program to read and store the data of 3 employees and calculate their Gross Salary using the concept of structure.

## ALGORITHM

1.	Start the program.
2.	Create an employee structure with name, id and salary details as members.
3.	Using structure variable read the structure members.
4.	Calculate the gross salary and print the details.
5.	Stop the program.

## PROGRAM

#include <stdio.h>

struct Employee {
    int id;
    char name[50];
    float basic, hra, da, gross;
};

int main() {
    struct Employee emp[3];  // array of 3 employees
    int i;

    printf("Enter details of 3 employees:\n");

    for (i = 0; i < 3; i++) {
        printf("\n--- Employee %d ---\n", i + 1);
        printf("Enter Employee ID: ");
        scanf("%d", &emp[i].id);

        printf("Enter Name: ");
        scanf("%s", emp[i].name);

        printf("Enter Basic Salary: ");
        scanf("%f", &emp[i].basic);

        printf("Enter HRA: ");
        scanf("%f", &emp[i].hra);

        printf("Enter DA: ");
        scanf("%f", &emp[i].da);

        // Calculate Gross Salary
        emp[i].gross = emp[i].basic + emp[i].hra + emp[i].da;
    }

    printf("\n\n----- Employee Details with Gross Salary -----\n");
    printf("ID\tName\t\tGross Salary\n");
    printf("--------------------------------------------\n");

    for (i = 0; i < 3; i++) {
        printf("%d\t%-10s\t%.2f\n", emp[i].id, emp[i].name, emp[i].gross);
    }

    return 0;
}



 ## OUTPUT


<img width="577" height="814" alt="C29" src="https://github.com/user-attachments/assets/40838eac-5d26-47b8-9217-0f87d0a053c9" />


 

## RESULT

Thus the C program to read and store the data of 3 employees and calculate their Gross Salary using the concept of structure
 




# EX – 30 -STUDENTS MARK -TOTAL &AVERAGE USING STRUCURE

## AIM
Create a C program to calculate the total and average of student using structure.

## ALGORITHM 

Step 1: Start the program.
Step 2: Define a struct student with:
•	name: a character array (size 10) for the student's name (not used in the logic).
•	rollno: an integer for the student's roll number (also unused).
•	subject[5]: an array to store marks of 5 subjects.
•	total: an integer to store total marks.
Step 3: Declare an array s[2] of type struct student for 2 students. Also declare variables n, i, and j for input 
             and iteration.
Step 4: Input Loop (i = 0 to 1):
•	Read an integer n (but it's not used later — possibly intended for roll number or placeholder).
•	Loop j = 0 to 4:
o	Read 5 subject marks into s[i].subject[j].
Step 5: Total Marks Calculation Loop (i = 0 to 1):
•	Initialize s[i].total to 0.
•	Loop j = 0 to 4:
o	Add each subject mark to s[i].total.
Step 6: Override Total (Hardcoded):
•	Set s[0].total = 374;
•	Set s[1].total = 383;
           This step overwrites the computed totals. It seems like testing or hardcoded totals — unnecessary if you’re 
                 already calculating them.
Step 7: Output Loop (i = 0 to 1):
•	Print s[i].total for each student.
Step 8: End the program.

## PROGRAM

#include <stdio.h>

struct Student {
    char name[50];
    int roll;
    float marks1, marks2, marks3;
    float total, average;
};

int main() {
    struct Student s;

    printf("Enter student name: ");
    scanf("%s", s.name);

    printf("Enter roll number: ");
    scanf("%d", &s.roll);

    printf("Enter marks of 3 subjects:\n");
    scanf("%f %f %f", &s.marks1, &s.marks2, &s.marks3);

    // Calculate total and average
    s.total = s.marks1 + s.marks2 + s.marks3;
    s.average = s.total / 3;

    printf("\n----- Student Details -----\n");
    printf("Name: %s\n", s.name);
    printf("Roll No: %d\n", s.roll);
    printf("Total Marks: %.2f\n", s.total);
    printf("Average Marks: %.2f\n", s.average);

    return 0;
}



## OUTPUT

 <img width="553" height="292" alt="C30" src="https://github.com/user-attachments/assets/6be21f5a-194a-48f9-add9-8953044ec19b" />


## RESULT

Thus the C program to calculate the total and average of student using structure has been executed successfully.
