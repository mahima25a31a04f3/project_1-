#include <stdio.h>
#include <string.h>

struct Student {
    char name[50];
    char aadhar[20];
    char apaar[20];
    char email[50];
    char phone[15];
};

int main() {
    struct Student s[100];
    int choice, count = 0;
    char searchAadhar[20];

    while (1) {
        printf("\n====== Student Management System ======\n");
        printf("1. Add Student Details\n");
        printf("2. Display All Students\n");
        printf("3. Search Student by Aadhar\n");
        printf("4. Exit\n");
        printf("Enter your choice: ");
        scanf("%d", &choice);
        getchar(); // Clear buffer

        switch (choice) {
        case 1:
            printf("\nEnter Student Name: ");
            fgets(s[count].name, sizeof(s[count].name), stdin);

            printf("Enter Aadhar Number: ");
            fgets(s[count].aadhar, sizeof(s[count].aadhar), stdin);

            printf("Enter APAAR ID: ");
            fgets(s[count].apaar, sizeof(s[count].apaar), stdin);

            printf("Enter Email: ");
            fgets(s[count].email, sizeof(s[count].email), stdin);

            printf("Enter Phone Number: ");
            fgets(s[count].phone, sizeof(s[count].phone), stdin);

            count++;
            printf("Student Added Successfully!\n");
            break;

        case 2:
            if (count == 0) {
                printf("No student records available.\n");
            } else {
                printf("\n----- Student Records -----\n");
                for (int i = 0; i < count; i++) {
                    printf("\nStudent %d:\n", i + 1);
                    printf("Name        : %s", s[i].name);
                    printf("Aadhar      : %s", s[i].aadhar);
                    printf("APAAR ID    : %s", s[i].apaar);
                    printf("Email       : %s", s[i].email);
                    printf("Phone       : %s", s[i].phone);
                }
            }
            break;

        case 3:
            printf("Enter Aadhar Number to search: ");
            fgets(searchAadhar, sizeof(searchAadhar), stdin);

            int found = 0;
            for (int i = 0; i < count; i++) {
                if (strcmp(s[i].aadhar, searchAadhar) == 0) {
                    printf("\nStudent Found!\n");
                    printf("Name        : %s", s[i].name);
                    printf("Aadhar      : %s", s[i].aadhar);
                    printf("APAAR ID    : %s", s[i].apaar);
                    printf("Email       : %s", s[i].email);
                    printf("Phone       : %s", s[i].phone);
                    found = 1;
                    break;
                }
            }
            if (!found) {
                printf("No student found with given Aadhar.\n");
            }
            break;

        case 4:
            printf("Exiting...\n");
            return 0;

        default:
            printf("Invalid choice! Try again.\n");
        }
    }
}
