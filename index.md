## Lab Report 3

Hi again! This is my third lab report, and for this report I learned about some options a command-line command could be used with. The command I
chose to use for this assignment is the `less` command. `less` is a command that displays a txt file on the terminal, allowing a user
to read a file's contents without crowding out their terminal. In this blog I'll be showing you four different command=line options for the command.

First, to get an idea of the output of `less`, I'll show you what is displayed on my terminal when I use the command to read the file `HistoryItaly.txt`. Here
is the input followed by the output:

`less HistoryItaly.txt`

**INSERT IMAGE**

As you can see, the contents of the file were displayed in the terminal. I can exit this screen and return to the terminal by pressing q.

# Option 1: -N

-N is a command used to display line numbers to the left of the displayed output of a text file. I found this command through an online manual on the less command
, at https://www.man7.org/linux/man-pages/man1/less.1.htm. 

Here is an example of a command to use `less -N` to open the `HistoryItaly.txt` file:

`less -N HistoryItaly.txt`

Output:

![image](https://user-images.githubusercontent.com/122569112/217960170-f646b2a6-794f-4d56-909a-ee94ca8e82db.png)

Here is an example of using `less -N` to open `IntroDublin.txt`:

`less -N IntroDublin.txt`

![image](https://user-images.githubusercontent.com/122569112/217960995-95e47094-c901-4735-b50f-43f5b887fdb9.png)

# Option 2: Finding Text

In order to search for text within a file, all a user must do is type `/[text to search]`. After pressing enter, it highlights all of the instances of 
the searched phrase, and to navigate to the next line in which an instance of the word can be found the user must press `n`. 

Here is an example of using `/they` to search `HistoryItaly.txt` for all instances of the word "they". 

`less HistoryItaly.txt`

Then I type: `/they`. Here is what is displayed:

![image](https://user-images.githubusercontent.com/122569112/217962688-078ac52f-0769-41b2-aa1a-3e3d4056c7ff.png)

By using `n`, I can navigate to different instances of "they", and by using `Shift + n` I can navigate backwards. 

