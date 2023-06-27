# Word Count:


## 1. To count words, letters, bytes or lines
> ```wc```

|Functionallity|Code|
|:---:|:---:|
|Number of lines| ```wc -l <file>```|
|Number of bytes|```wc -c <file>```|
|Number of chartacters|```wc -m <file>```|
|Number of words|```wc -w <file>```|


## 2. To count words, letters, bytes or lines
> ```grep:``` 

```[options]```: command modifiers

```pattern```: the pattern we want to find with the search

```[FILE]```: The file you are searching in


|Param|Explanation|
|:---:|:---:|
|```-i```| The search will not be case sensitive. That is, if you want to search for the word "auto" it will be the same as "AUTO"
|```-c```| will only show the number of lines that match the searched pattern
|```-r```| enable recursive search in current directory|
|```-n```| Searches for lines and precedes each matching line with a line number.
|```-v```|with this option, we are shown the lines that do not match the pattern we have searched for|


## 3. Find a word in a text file
To search for a word in a text file, simply type the command:

```grep file search```

> ```search```: the word you are looking for 
```file```: the file in which you are looking for the word

For example, if we are looking for the word command in a file called test.txt:

```grep command test.txt```

## 4. Find a word regardless of case
To do this, it is necessary to add the ```-i``` option.

```grep -i search file```

## 5. Count of words that match the search
Using the grep command you can find out how many times a word is used in the text file. Just add the ```-c``` option.

```grep -c search file```

## 6. Search multiple keywords
So far we have seen examples where we search for a single word. Grep supports multiple queries in a single command. The command would look like this:

```grep search1 file | grep search2 file```

The command works very simply. First, we search for Search1 and then pass after the slash to a second grep command for the second word: Search2.

## 7. Find a word in a set of files
It is also possible to search multiple files with a single command:

```grep -l search_word ./*```

In the terminal, the files containing the word you searched for will be displayed.