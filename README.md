# Tour-guide-directory-
Telephone directory to find tour guide mobile number:

PROGRAM CODE:
#include <stdio.h>
#include <string.h>

struct Location {
    char place[20];
    int pincode;
    char guide_name[20];
    long long guide_number;
};

int main() {
    struct Location L[11] = 
    {
        {"Pune", 411001, "Rahul", 9876543210},
        {"Mumbai", 400001, "Amit", 9988776655},
        {"Delhi", 110001, "Rohan", 9090909090},
        {"Goa", 403001, "Suresh", 8800223344},
        {"Nashik", 422001, "Prakash", 9123456780},
        {"Satara", 415001, "Ramesh", 9922334252},
        {"Nagpur", 440007, "Mahesh", 9157257268},
        {"Kolhapur", 416001, "Gauri", 997527266},
        {"Jalgaon",425001,"Saloni",953625274},
        {"Ahmednagar",414001,"Ahmed",764835833},
        {"Amravati",414001,"Aditi",9463724836},
        
        
        
    };

    char user_place[20];
    int found = 0;

    printf("Enter location name: ");
    scanf("%s", user_place);

    for (int i = 0; i < 11; i++) {
        if (strcmp(user_place, L[i].place) == 0) {
            printf("\n--- Travel Guide Details ---\n");
            printf("Place: %s\n", L[i].place);
            printf("Pincode: %d\n", L[i].pincode);
            printf("Guide Name: %s\n", L[i].guide_name);
            printf("Guide Number: %lld\n", L[i].guide_number);
            found = 1;
    
        }
    }

    if (!found) {
        printf("\nLocation not found in database.\n");
    }

    return 0;
}
