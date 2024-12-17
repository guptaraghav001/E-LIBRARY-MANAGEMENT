# E-LIBRARY-MANAGEMENT
THIS PROJECT IS ABOUT E -LIBRARY MANAGEMENT
                                          // E-library Management System
 #include <stdio.h>
#include <string.h>


// Structure of Library

struct library {
	char book_name[20];
  char book_secondname[10];
	char author_firstname[20];
  char author_name[10];
	int pages ;
	float price ;
};


int main()  
{

	// variable and array 

	struct library lib[100];

	char authorfirstname[30];
  	char authorname[30];


	
	int i =0;
  int count =0;
  int input =0;
  

	// execution loop

	while (input != 5) {

		printf("\n\n            ********!!!!!!!!!!  WELCOME TO E-LIBRARY !!!!!!!!!!********\n\n");
		printf("1. Add book information\n"); 
    printf("2. Display book information\n");
		printf("3. List all the detail of the books of given author\n");
		printf("4. List the number of books in the library\n");
		printf("5. Exit");

		// Enter the book detail

		printf("\n\nEnter one of the above: ");
		scanf("%d", &input);

		

		switch (input) {

	
	// Add book
        case 1:
            printf("Enter book name = ");
			scanf("%s %s", lib[i].book_name , lib[i].book_secondname);


             printf("Enter author name = ");
			scanf("%s %s", lib[i].author_firstname , lib[i].author_name);

			printf("Enter pages = ");
			scanf("%d", &lib[i].pages);

			printf("Enter price = ");
			scanf("%f", &lib[i].price);
			count++;

			break;

		// print about the book information
		case 2:
			printf("\n you have entered the following information :\n\n");
			for (i = 0; i < count; i++) {

				printf("1.) book name = %s %s ",	lib[i].book_name , lib[i].book_secondname);

				printf("2.) author name = %s %s ", lib[i].author_firstname , lib[i].author_name);

				printf("3.)pages = %d ",  lib[i].pages);

				printf("4.)price = %f\n",	lib[i].price);
			}
			break;

		
    
    //  print books detail of given author 
		case 3:
			printf("Enter author name :\n ");
			scanf("%s %s", authorfirstname ,authorname);
			for (i = 0; i < count; i++) {

				if (strcmp((authorfirstname ,authorname),  (lib[i].author_firstname ,lib[i].author_name))== 0)
					printf(" book name:%s author name:%s page:%s price:%s %d %f\n",  lib[i].book_name , lib[i].book_secondname , lib[i].author_firstname , lib[i].author_name ,lib[i].pages , lib[i].price);
			}
			break;

// Print total count		
    case 4:
			printf("\n No of books in library : %d", count);
			break;

     // exit the library

		case 5:
			break;
		}
	}

	return 0;
}

