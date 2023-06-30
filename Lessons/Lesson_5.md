# SED workflow:

>* _Mac users_:  ```brew install gnu-sed``` 
>* _Then run_: ```gsed '1~2d' sample.txt```


## 1. 'Delete' command
To run the ```delete``` command, use d along with a file in quotes. The command will remove the first line in the text.txt file:

```sed ‘1d’ text.txt```

## 2. 'Write' command
To execute the write command, type w, the line number, and the file, in quotes. The following command reads the second line and writes it to the text2.txt file:

```sed '2~2 w text2.txt' text.txt ```

_Mac users_ : ```sed '2~2 w text2.txt' text.txt ```

```cat text2.txt```

## 3. 'Add' command
Use the keyword and a line number in quotes. After closing the quotes, provide the attached source. The following command displays the second line of the text.txt file.

```sed '2 a The Append example' text.txt``` 

```cat text.txt```

## 4. 'Read' command
Use r and put the file location in quotes. The following command will read the input from a text file and add it after the third line in the text2.txt file.

```sed '3 r text.txt' text2.txt```

```cat text2.txt```