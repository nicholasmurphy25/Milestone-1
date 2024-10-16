# Semester Project: Milestone 1

## Group Members: Kevin Torrealba, Nicholas Murphy, Kevin Carcamo

### Main Class
The `Main.java` file serves as the entry point of the program. It is responsible for interacting with the user and passing the necessary data to other parts of the application.

#### Key Functions:
- **User Interaction**: The program prompts the user to input a directory path where the article files are stored.
- **Data Handling**: Once the user provides the directory path, it is passed to the `ArticleProcessor` class for file reading and further processing.

The purpose of this class is to gather input from the user and initiate the file processing by calling the appropriate method in the `ArticleProcessor` class. This ensures that the user can specify the location of the files, and the program will handle the rest of the processing from there.

### ArticleProcessor Class

The `ArticleProcessor` class is responsible for reading and processing the files from the directory provided by the user. It handles the core functionality of the project, including reading article files, counting words, and processing the text.

#### Key Functions:
- **File Reading**: The class takes a directory path as input and reads all the article files within that directory.
- **Text Processing**: It processes the text in each article by counting the total number of words, removing stop words, and counting the number of statements (sentences) in the articles.
- **Statistics Generation**: After processing, the class gathers the relevant statistics such as original word count, new word count (after stop words are removed), and statement count.

The `ArticleProcessor` is the core component that performs the main processing tasks for the articles, preparing the data for analysis and generating statistics based on the text.

### Statistics Class
This class contains 3 attributes:
- *orgWordCount* 
- *newWordCount*
- *statementCount* 

*orgWordCount* - This attribute is a public integer that stores the number of words in the article **before** removing stop words.<br>
*newWordCount* - This attribute is a public integer that stores the number of words in the article **after** removing stop words.<br> 
*statementCount* - This attribute is a public integer that stores the number of statements (sentences) that are in the article.<br>

This class contains 2 methods: 
- *getWordCount*
- *getStatementCount*

  *getWordCount* - This method requires 2
