# Basic filesystem

## cd - "Change Directory"

Example with no argument

```
[user@sahara ~]$ cd
[user@sahara ~]$ 
```

Example with a path to a directory as an argument

```
[user@sahara ~]$ cd lecture1/messages
[user@sahara ~/lecture1/messages]$ 
```

Example with a path to a file as an argument

```
[user@sahara ~/lecture1/messages]$ cd en-us.txt
bash: cd: en-us.txt: Not a directory
[user@sahara ~/lecture1/messages]$ 
```

## ls - "List"

Example with no argument
```
[user@sahara ~]$ ls
lecture1
[user@sahara ~]$ 
```

Example with a path to a directory as an argument
```
[user@sahara ~]$ ls lecture1/messages
ar-kw.txt  en-us.txt  es-mx.txt  vi.txt  zh-cn.txt
[user@sahara ~]$ 
```
Example with a path to a file as an argument

```
[user@sahara ~]$ ls lecture1/messages/en-us.txt
lecture1/messages/en-us.txt
[user@sahara ~]$ 
```
## cat - "Concatenate"

Example with no argument
```
[user@sahara ~]$ cat

```

Example with a path to a directory as an argument
```
[user@sahara ~]$ cat lecture1/messages
cat: lecture1/messages: Is a directory
[user@sahara ~]$ 
```
Example with a path to a file as an argument

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




