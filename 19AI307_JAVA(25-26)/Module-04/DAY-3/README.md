# Ex.No:4(C)  COMPOSITION IN JAVA

## QUESTION:
Implement a system where a Library contains multiple Book objects. Each Book is created inside the Library. Books can't exist independently (Composition).


<img width="521" height="307" alt="image" src="https://github.com/user-attachments/assets/ae0c9bf9-e55a-4c6d-a48a-0977ee0a6bb4" />



## AIM:

To demonstrate composition in Java by creating Book objects that exist only within a Library.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a Scanner object to read user input.
4.	Instantiate a Library object.
5.	Read an integer n representing the number of books to add.
6.	For each book (repeat n times):
     a. Read the book’s title from input.
     b. Read the book’s author from input.
     c. Call addBook(title, author) on the Library object, which internally creates Book object and adds it to the library’s collection.
7.Call showBooks() on the Library object to display all books and their details.
8.Close the scanner.
9.End the program.





## PROGRAM:
 ```
/*
Program to implement a Composition Concepts in Java
Developed by: Reshma C
RegisterNumber:  212223040168
*/
```

## SOURCE CODE:

```
import java.util.*;

public class CompositionExample {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Library library = new Library();

        int n = sc.nextInt();
        sc.nextLine();

        for (int i = 0; i < n; i++) {
            String title = sc.nextLine();
            String author = sc.nextLine();
            library.addBook(title, author);
        }

        library.showBooks();
        sc.close();
    }
}

class Book {
    private String title;
    private String author;

    public Book(String title, String author) {
        this.title = title;
        this.author = author;
    }

    public String getDetails() {
        return title + " by " + author;
    }
}

class Library {
    private List<Book> books = new ArrayList<>();

    public void addBook(String title, String author) {
        books.add(new Book(title, author));
    }

    public void showBooks() {
        if (books.isEmpty()) {
            System.out.println("No books in the library.");
        } else {
            System.out.println("Books in Library:");
            for (Book b : books) {
                System.out.println("- " + b.getDetails());
            }
        }
    }
}
```






## OUTPUT:

<img width="1013" height="527" alt="image" src="https://github.com/user-attachments/assets/9f66898c-ce18-45d8-a09b-f1b19688ef0a" />


## RESULT:

Each Book is instantiated and managed inside the Library, showing a strong lifecycle dependency.
