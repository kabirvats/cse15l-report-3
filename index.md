## Lab Report 3

Hi again! This is my third lab report, and for this report I learned about some options a command-line command could be used with. The command I
chose to use for this assignment is the `less` command. `less` is a command that displays a txt file on the terminal, allowing a user
to read a file's contents without crowding out their terminal. In this blog I'll be showing you four different command=line options for the command.

First, to get an idea of the output of `less`, I'll show you what is displayed on my terminal when I use the command to read the file `HistoryItaly.txt`. Here
is the input followed by the output:

`less HistoryItaly.txt`

**INSERT IMAGE**

As you can see, the contents of the file were displayed in the terminal. I can exit this screen and return to the terminal by pressing q.

# Option 1: Displaying Line Numbers Using -N

-N is a command used to display line numbers to the left of the displayed output of a text file. I found this command through an online manual on the less command
, at https://www.man7.org/linux/man-pages/man1/less.1.html. 

Here is an example of a command to use `less -N` to open the `HistoryItaly.txt` file:

`less -N HistoryItaly.txt`

Output:

![image](https://user-images.githubusercontent.com/122569112/217960170-f646b2a6-794f-4d56-909a-ee94ca8e82db.png)

Here is an example of using `less -N` to open `IntroDublin.txt`:

`less -N IntroDublin.txt`

![image](https://user-images.githubusercontent.com/122569112/217960995-95e47094-c901-4735-b50f-43f5b887fdb9.png)

# Option 2: Finding Text

In order to search for text within a file, all a user must do is type `/[text to search]`. After pressing enter, it highlights all of the instances of 
the searched phrase, and to navigate to the next line in which an instance of the word can be found the user must press `n`. I found out about this through this
website: https://linuxhandbook.com/less-command/.

Here is an example of using `/they` to search `HistoryItaly.txt` for all instances of the word "they". 

`less HistoryItaly.txt`

Then I type: `/they`. Here is what is displayed:

![image](https://user-images.githubusercontent.com/122569112/217962688-078ac52f-0769-41b2-aa1a-3e3d4056c7ff.png)

By using `n`, I can navigate to different instances of "they", and by using `Shift + n` I can navigate backwards. 

It is also possible to do this while the line numbers are displayed! Here is an example: 

`less -N HistoryIndia.txt`

`/Aryan`

![image](https://user-images.githubusercontent.com/122569112/217964542-719eab55-1e39-4fd8-994e-24719472e750.png)

Unfortunately, we can't use / to search the line numbers directly, but this is useful for finding which lines a specific word occurs on.

# Option 3: Changing Colors Using -D

This command is a little more nuanced than the previous two, and there are some fun options to play around with once you get the hang of it! 
I believe this command is only available on MS-DOS terminals, I'm not sure though. In my use of the command, when I'm using this modifier I have
to include `--use-color`.

This command has options for use, and the formatting of the modifier is as follows: `-D[part of text to change color of][color]`.

To signify which part of the text to change the color of, there are a variety of options. `B` changes binary characters, `C` changes control characters, 
`E` changes errors, `H` changes headers set with the `--header` option, `M` changes the color of mark letters in the status column, `N` changes the 
color of line numbers, `P` changes prompts' color scheme, `R` changes the color of the Rscroll character, `S` changes the color of search results, 
`W` changes highlights enabled with -w, `d` changes the color of bold text, `k` for blinking text, `s` for standout text and `u` for underlined text. 

Next, to signify the color there are two components. The first letter is the color of the textin the foreground, and the other letter signifies the background color. The color options are as follows: 'b' for blue, 'c' for cyan, 'g' for green, 'k' for black, 'm' for magenta, 'r' for red, 'w' for white, and 'y' for yellow. Using a capital letter denotes a brighter shade of the color.

That's a lot, so here's an example modifier: `-DuBc` displays all underlined characters with bright blue text on a cyan background.

Now to put it into practice. For the first example, I'll display all searched terms in `HawaiiHistory.txt` as bright magenta on a cyan background.

`less --use-color -DSMc HistoryHawaii.txt` 

Now I'll search using `/Hawaii`

Here is the result:

![image](https://user-images.githubusercontent.com/122569112/217972153-feedfe06-d644-4191-a04a-7dec781ead78.png)

