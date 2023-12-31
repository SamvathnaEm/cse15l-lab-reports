# Basic filesystem

## cd - "Change Directory"

* Example with no argument

```
[user@sahara ~]$ cd
[user@sahara ~]$ 
```
The ```cd``` command with no argument always places the user in the home directory. This command produced no output since it worked successfully, and the working directory was in the _/home_ directory when this command was run. 


* Example with a path to a directory as an argument

```
[user@sahara ~]$ cd lecture1/messages
[user@sahara ~/lecture1/messages]$ 
```
The ```cd``` command with a path to a directory as an argument will change the current working directory to the given path. As the example above, the current working directory was changed from the _/home_ directory to _/home/lecture1/messages_ directory. This command produced no output since the current working directory had been switched successfully.

* Example with a path to a file as an argument

```
[user@sahara ~/lecture1/messages]$ cd en-us.txt
bash: cd: en-us.txt: Not a directory
[user@sahara ~/lecture1/messages]$ 
```
The ```cd``` command with a path to a file as an argument will give an error message for the output, and the working directory will remain the same, which is _/home/lecture1/messages_. The cd command can only switch a directory path and cannot change a directory into a file. Therefore, the output will indicate that en-us.txt is not a directory, and we cannot change the working directory into that file.

## ls - "List"

* Example with no argument

```
[user@sahara ~]$ ls
lecture1
[user@sahara ~]$ 
```
The ```ls``` command with no argument will list all the files and folders in the current working directory. Based on the example above, the current working directory was _/home_ when this command was run. Therefore, the output would list the names of the files stored inside _/home_ directory, which is lecture1.


* Example with a path to a directory as an argument

```
[user@sahara ~]$ ls lecture1/messages
ar-kw.txt  en-us.txt  es-mx.txt  vi.txt  zh-cn.txt
[user@sahara ~]$ 
```
The ```ls``` command with a path to a directory as an argument will list all the files stored inside the working directory. As the example above, the working directory was _/home_ when the command was run. Therefore, the output would be the list of filenames stored inside the messages folder. 

* Example with a path to a file as an argument

```
[user@sahara ~]$ ls /home/lecture1/messages/en-us.txt
/home/lecture1/messages/en-us.txt
[user@sahara ~]$ 
```
The ```ls``` command with a path to a file as an argument will print the file path as the output. Based on the example above, the working directory was _/home_ when this command was run. This command typically lists the contents of the input paths. However, in our example, it listed the input file path because it is the only thing present at the given path.


## cat - "Concatenate"

* Example with no argument

```
[user@sahara ~]$ cat

```
The ```cat``` command with no argument won't produce anything as the output. This command is used to print the contents of one or more files given by the paths as the arguments. 
The working directory was in the _/home_ directory when this command was run. Since there are no file paths in the argument, this command won't print anything and will wait for the user input from the keyboard. If there is user input from the keyboard, the ```cat``` command will read it and print it as the output in the following line. It will continue this process until it receives the signal produced by the Ctrl+D key to stop the run of this command.

* Example with a path to a directory as an argument

```
[user@sahara ~]$ cat lecture1/messages
cat: lecture1/messages: Is a directory
[user@sahara ~]$ 
```
The ```cat``` command with a path to a directory as an argument will produce an error message for the output. The working directory was _/home_ when this command was run. Since this command only accepts one or more file paths to print the contents of those files given by the paths, a path to a directory as an argument doesn't work in the example above. Therefore, the output had been produced as an error message saying that lecture1/messages is a directory. 

* Example with a path to a file as an argument

```
[user@sahara ~]$ cat lecture1/Hello.java
import java.io.IOException;
import java.nio.charset.StandardCharsets;
import java.nio.file.Files;
import java.nio.file.Path;

public class Hello {
  public static void main(String[] args) throws IOException {
    String content = Files.readString(Path.of(args[0]), StandardCharsets.UTF_8);    
    System.out.println(content);
  }
}[user@sahara ~]$ 
```
The ```cat``` command with a path to a file as an argument will print the content inside that file given by a path.
The working directory was _/home_ when this command was run. Therefore, the output would simply be the content inside the Hello.java file.





