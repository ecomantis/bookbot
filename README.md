# BookBot

BookBot is my first [Boot.dev](https://www.boot.dev) project.

A command-line Python program that reads a book as a text file and prints a report of its word count and character frequencies.

## Features

- Counts the total number of words in a book
- Counts every character (case-insensitive)
- Prints alphabetic characters sorted from most to least common
- Takes the book path as a command-line argument

## Usage

Requires Python 3.

```sh
mkdir -p books
curl -L "https://storage.googleapis.com/qvault-webapp-dynamic-assets/course_assets/frankenstein.txt" -o books/frankenstein.txt
python3 main.py books/frankenstein.txt
```

If you run it without a path, it prints:

```
Usage: python3 main.py <path_to_book>
```

### Extra sample books

```sh
curl -L "https://storage.googleapis.com/qvault-webapp-dynamic-assets/course_assets/mobydick.txt" -o books/mobydick.txt
curl -L "https://storage.googleapis.com/qvault-webapp-dynamic-assets/course_assets/prideandprejudice.txt" -o books/prideandprejudice.txt

python3 main.py books/mobydick.txt
python3 main.py books/prideandprejudice.txt
```

## Example output

```
============ BOOKBOT ============
Analyzing book found at books/frankenstein.txt...
----------- Word Count ----------
Found 75767 total words
--------- Character Count -------
e: 44538
t: 29493
a: 25894
...
============= END ===============
```

## Project structure

```
bookbot/
├── main.py      # CLI entry point, file reading, and report printing
├── stats.py     # Word count, character count, and sorting
└── books/       # Sample books (download with the commands above)
```
