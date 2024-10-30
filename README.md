# Semester Project: Milestone 1

## Group Members: Kevin Torrealba, Nicholas Murphy, Kevin Carcamo

### Main Class

The `Main` class serves as the starting point of the program, handling user input and initiating the process of reading and processing articles.

### Key Functions:
- **User Interaction**: The class prompts the user to input the directory path where article files are stored.
- **Process Initialization**: It passes the user-provided directory path to the `ArticleProcessor` class to start reading and processing the files.

The `Main` class is the entry point for the program, ensuring that user input is gathered before starting the core text processing tasks performed by other classes.

### ArticleProcessor Class

The `ArticleProcessor` class is responsible for reading and processing the article files in the directory provided by the user. It performs key tasks such as file reading, stop word removal, and generating word frequency statistics.

### Fields:
- **`stopWords`**: A static list that stores the stop words used for filtering out common words from the text.
- **`fileList`**: A static array of `File` objects that stores the list of files found in the specified directory.

### Methods:
- **`readFiles(String directoryPath)`**: This static method reads all the files in the provided directory, processes each file's content, and calls other methods to analyze the text. It prints the original text and processes it to remove stop words, count words, and rank words by frequency.
  
- **`removeStopWords(String outString)`**: This static method removes stop words from the provided text (`outString`) by comparing each word with a predefined list of stop words. It returns the cleaned string, which no longer contains stop words, and prints the cleaned version of the text.

The `ArticleProcessor` class manages the entire text processing workflow, from reading files and removing stop words to generating word frequency statistics. It acts as the central component for processing and analyzing the content of the article files.

### Statistics Class

The `Statistics` class is responsible for calculating basic textual statistics such as word count and statement count.

### Fields:
- `orgWordCount`: Stores the original word count of the text.
- `newWordCount`: Stores the word count after removing stop words.
- `statementCount`: Stores the number of statements in the text.

### Methods:
- **`getWordCount(String outString, String stopWordsString)`**: This static method calculates the total number of words in the original text (`outString`) and the number of words remaining after stop words are removed (`stopWordsString`). It prints both values.
- **`getStatementCount(String outString)`**: This static method calculates the number of statements in the text by splitting the text based on punctuation (`.`, `!`, `?`) and prints the count.

### FrequencyRanker Class

The `FrequencyRanker` class ranks words based on their frequency in a given text and stores the results in a list.

### Fields:
- `words`: A static list that holds all words from the text (not used directly in the methods provided).
- `wordCountList`: A static list of `WordCount` objects that stores each unique word and its frequency in the text.

### Methods:
- **`rankWords(String cleanString)`**: This static method splits the provided `cleanString` into words, counts the frequency of each word, and sorts the words in descending order of frequency. It prints the ranked words and their frequencies.

### Nested Class:
- **`WordCount`**: This class represents a word and its associated frequency.
  - **Fields:**
    - `word`: The word being counted.
    - `count`: The frequency of the word.
  - **Constructor:**
    - `WordCount(String word, int count)`: Initializes a new `WordCount` object with the given word and frequency.

## UML Diagram
![](/Users/kevintorrealba/ProjectLibrary/UML_Diagram.png)
