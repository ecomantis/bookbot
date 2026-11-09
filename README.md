# BookBot

first boot.dev project. reads a text file and prints the word count, then how often each letter shows up.

needs python 3.

```sh
mkdir -p books
curl -L "https://storage.googleapis.com/qvault-webapp-dynamic-assets/course_assets/frankenstein.txt" -o books/frankenstein.txt
python3 main.py books/frankenstein.txt
```

if you forget the path:

```
Usage: python3 main.py <path_to_book>
```

same download for the other two samples:

```sh
curl -L "https://storage.googleapis.com/qvault-webapp-dynamic-assets/course_assets/mobydick.txt" -o books/mobydick.txt
curl -L "https://storage.googleapis.com/qvault-webapp-dynamic-assets/course_assets/prideandprejudice.txt" -o books/prideandprejudice.txt
```

frankenstein comes out like this:

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

main.py reads the file and prints the report. stats.py counts the words and letters.
