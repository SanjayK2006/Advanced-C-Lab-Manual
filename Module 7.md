##NAME: SANJAY K
##REG NO: 212223220094
EXP NO:1 C PROGRAM FOR ARRAY OF STRUCTURE TO CHECK ELIGIBILITY FOR THE VACCINE.

Aim:
To write a C program for array of structure to check eligibility for the vaccine person age above 6 years of age.

Algorithm:
1.	Declare structure eligible with age (integer) and n (character array)
2.	Declare variable e of type eligible
3.	Input age and name using scanf, store in e
4.	If e.age <= 6
-	Print "Vaccine Eligibility: No"
Else
-	Print "Vaccine Eligibility: Yes"
5.	Print details (e.age, e.n)
6.	Return 0
 
Program:
```
#include <stdio.h>

struct Person {
    char name[50];
    int age;
};

int main() {
    struct Person p[100];
    int n, i;

    printf("Enter number of persons: ");
    scanf("%d", &n);

    for(i = 0; i < n; i++) {
        printf("Enter name: ");
        scanf("%s", p[i].name);
        printf("Enter age: ");
        scanf("%d", &p[i].age);
    }

    printf("\nEligibility Check:\n");
    for(i = 0; i < n; i++) {
        if(p[i].age > 6)
            printf("%s is eligible\n", p[i].name);
        else
            printf("%s is not eligible\n", p[i].name);
    }

    return 0;
}
```


Output:

![Screenshot 2025-04-25 211133](https://github.com/user-attachments/assets/afdc077d-257a-420d-95f6-0c899348c2b7)


Result:
Thus, the program is verified successfully. 



EXP NO:2 C PROGRAM FOR PASSING STRUCTURES AS FUNCTION ARGUMENTS AND RETURNING A STRUCTURE FROM A FUNCTION
Aim:
To write a C program for passing structure as function and returning a structure from a function

Algorithm:
1.	Define structure numbers with members a and b.
2.	Declare variable n of type numbers.
3.	Prompt the user to enter values for a and b.
4.	Input values for a and b into n using scanf.
5.	Call the add function with n as an argument.
6.	Print the result returned by the add function.
7.	Return 0
 
Program:
```
#include <stdio.h>

// Define a structure
struct Student {
    char name[50];
    int marks;
};

// Function that takes a structure and returns a structure
struct Student updateMarks(struct Student s) {
    s.marks += 10;  // Add 10 bonus marks
    return s;
}

// Function to display the structure
void display(struct Student s) {
    printf("Name: %s\n", s.name);
    printf("Marks: %d\n", s.marks);
}

int main() {
    struct Student s1;

    // Input student details
    printf("Enter student name: ");
    scanf("%s", s1.name);
    printf("Enter student marks: ");
    scanf("%d", &s1.marks);

    // Pass to function and get updated structure
    s1 = updateMarks(s1);

    // Display updated student details
    printf("\nAfter updating marks:\n");
    display(s1);

    return 0;
}

```



Output:


![Screenshot 2025-04-25 211424](https://github.com/user-attachments/assets/aa0a7fa7-5f68-4ad8-ba67-fc7dd37fd246)




Result:
Thus, the program is verified successfully


 
EXP.NO:3 C PROGRAM TO READ A FILE NAME FROM USER AND WRITE THAT FILE USING FOPEN()

Aim:
To write a C program to read a file name from user

Algorithm:
1.	Include the necessary header file stdio.h.
2.	Begin the main function.
3.	Declare a file pointer p.
Declare a character array name to store the file name.
4.	Prompt the user to enter a file name.
Use scanf to input the file name into the name array.
5.	Print a message indicating that the file with the specified name has been created successfully.
6.	Use fopen to open a file with the name provided by the user in write mode ("w").
-	If successful, continue to the next step.
-	If unsuccessful, print an error message and exit the program with a non-zero status.
1.	Print a message indicating that the file has been opened successfully.
2.	Use fclose to close the file.
3.	Print a message indicating that the file has been closed.
4.	End the main function.
5.	Return 0 to indicate successful program execution.
 
Program:
```
#include <stdio.h>

int main() {
    char filename[100];
    FILE *file;

    printf("Enter file name: ");
    scanf("%s", filename);

    file = fopen(filename, "r");

    if (file == NULL) {
        printf("Unable to open file.\n");
    } else {
        printf("File opened successfully.\n");
        fclose(file);
    }

    return 0;
}
```



Output:
![Screenshot 2025-04-25 211701](https://github.com/user-attachments/assets/855f94f1-5a64-4979-99b2-c605f4a7ec64)

Result:
Thus, the program is verified successfully
 


EXP NO:4   PROGRAM TO READ A FILE NAME FROM USER, WRITE THAT FILE AND INSERT TEXT IN TO THAT FILE
Aim:
To write a C program to read, a file and insert text in that file
Algorithm:
1.	Include the necessary header file stdio.h.
2.	Begin the main function.
3.	Declare a file pointer p.
Declare character arrays name and text. Declare an integer variable num.
4.	Prompt the user to enter a file name and the number of strings.
Use scanf to input the file name into the name array and the number of strings into the num variable.
5.	Use fopen to open a file with the name provided by the user in write mode ("w").
-	If successful, continue to the next step.
-	If unsuccessful, print an error message and exit the program with a non-zero status.
6.	Print a message indicating that the file has been opened successfully.
1.	Use a loop to input strings from the user and write them to the file using fputs.
2.	Use fclose to close the file.
3.	Print a message indicating that data has been added successfully.
4.	End the main function.
5.	Return 0 to indicate successful program execution.
 
Program:
```
#include <stdio.h>
int main()
{
    char a[10],b[10],c[10];
    FILE *in;
    char fname[20];
    scanf("%s",fname);
    in=fopen(fname,"w");
    printf("%s Opened\n",fname);
    scanf("%c%c%c",a,b,c);
    fputs(a,in);
    fputs(b,in);
    fputs(c,in);
    printf("Data added Successfully");
}
```



Output:

![Screenshot 2025-04-25 212027](https://github.com/user-attachments/assets/f4d9a56e-705c-4d6b-af80-8f2daafa847a)






Result:
Thus, the program is verified successfully



Ex No 5 : C PROGRAM TO DISPLAY STUDENT DETAILS USING STRUCTURE

Aim:
The aim of this program is to dynamically allocate memory to store information about multiple subjects (name and marks), input the details for each subject, and then display the stored information. Finally, it frees the allocated memory to prevent memory leaks.

Algorithm:
1.Input the number of subjects.

2.Read the integer value n from the user, which represents the number of subjects.

3.Dynamically allocate memory:

4.Use malloc to allocate memory for n subjects. Each subject has a name (array of characters) and marks (integer).

5.If memory allocation fails (i.e., the pointer s is NULL), display an error message and exit the program.

6.Input the details of each subject

7.Use a for loop to read the name and marks of each subject using scanf. For each subject, store the name as a string and marks as an integer in the dynamically allocated memory.

8.Display the details of each subject

9.Use another for loop to print the name and marks of each subject.

10.Free the allocated memory

11.After all operations are done, call free(s) to release the dynamically allocated memory.

12.Return from the main function

13.End the program by returning 0.

Program:
```
#include <stdio.h>
#include <stdlib.h>
#include <string.h>

typedef struct {
    char name[50];
    int marks;
} Subject;

int main() {
    int n, i;

    printf("Enter number of subjects: ");
    scanf("%d", &n);

    Subject *subjects = (Subject *)malloc(n * sizeof(Subject));

    if (subjects == NULL) {
        printf("Memory allocation failed!\n");
        return 1;
    }

    for (i = 0; i < n; i++) {
        printf("Enter name of subject %d: ", i + 1);
        getchar();
        fgets(subjects[i].name, sizeof(subjects[i].name), stdin);
        subjects[i].name[strcspn(subjects[i].name, "\n")] = 0;

        printf("Enter marks for subject %d: ", i + 1);
        scanf("%d", &subjects[i].marks);
    }

    printf("\nSubject Information:\n");
    for (i = 0; i < n; i++) {
        printf("Subject %d: Name = %s, Marks = %d\n", i + 1, subjects[i].name, subjects[i].marks);
    }

    free(subjects);

    return 0;
}
```



Output:

![Screenshot 2025-04-25 212623](https://github.com/user-attachments/assets/5d075e35-23f9-4cba-90a7-3f38bdbd7c85)






Result:
Thus, the program is verified successfully
