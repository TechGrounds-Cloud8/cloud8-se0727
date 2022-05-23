# Working with text (CLI)

One of the essential tasks we do while working with bash scripting is reading and writing files. In this guide, we will focus on how to read files in bash and how to edit them.
There are multiple ways to read and write a file in bash. The simplest way is using operators “>” and “>>”.

“>” operator will overwrite the existing data
“>>” operator will append data

How to write a file using redirection operators
The simple and straightforward approach of writing to a file is using redirection operators. For instance, if you want to change the text of an already existing file, then firstly create a text file by the name of “testfile.txt” and write anything in it:

Type the below-mentioned command in the terminal:
$ echo “Overwriting the existing text in the file” >> testfile.txt

## Key terminology

echo: ‘echo’ is one of the most used commands to print text or string data into the terminal or another command as input or a file.

">>"  STDERR append mode 

grep: Grep is an essential Linux and Unix command. It is used to search text and strings in a given file. In other words, grep command searches the given file for lines containing a match to the given strings or words. It is one of the most useful commands on Linux and Unix-like system for developers and sysadmins. 

">"  STDOUT overwrite mode

## Exercise
Use the echo command and output redirection to write a new sentence into your text
file using the command line. The new sentence should contain the word
‘techgrounds’.

● Use a command to write the contents of your text file to the terminal. Make use of a
command to filter the output so that only the sentence containing ‘techgrounds’
appears.

● Read your text file with the command used in the second step, once again filtering for
the word ‘techgrounds’. This time, redirect the output to a new file called
‘techgrounds.txt’.


### Sources
https://linuxhint.com/write-to-file-bash/
[List your sources you used for solving the exercise]
https://linuxhint.com/bash_echo/
https://www.cyberciti.biz/faq/howto-use-grep-command-in-linux-unix/#Use_grep_to_search_a_file
https://www.cyberciti.biz/faq/howto-use-grep-command-in-linux-unix/#Saving_grep_output_to_a_file
https://stackoverflow.com/questions/16631423/output-grep-results-to-text-file-need-cleaner-output


### Overcome challenges
Had found grep command but did not understand I had to look further into it. So I continued searching for a command which was in fact grep.

### Results

![alt text](https://github.com/TechGrounds-Cloud8/cloud8-se0727/blob/main/00_includes/Linux/linux%20opdr3%20output%20redirection%20and%20echo.PNG)
![alt text](https://github.com/TechGrounds-Cloud8/cloud8-se0727/blob/main/00_includes/Linux/linux%20opdr3%20write%20content%20to%20terminal.PNG)
![alt tesxt](https://github.com/TechGrounds-Cloud8/cloud8-se0727/blob/main/00_includes/Linux/linux%20opdr3%20redirect%20ouput%20of%20grep%20in%20a%20file.PNG)

