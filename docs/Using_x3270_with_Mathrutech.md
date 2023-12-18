# Using x3270 with Mathrutech

## Install x3270

### OS X (Mac)

The standard way to install x3270 is with Homebrew.

```shell
brew install x3270
``` 

### Location of the executable 

After installation, the executable will be located in the following directory.

```shell 
/opt/homebrew/Cellar/x3270/4.3ga4/bin 
``` 

### Name of the executable 

The command-line wrapper for the x3270 library is:

```shell 
c3270 
```


## Help and documentation 

The help explains all the c3270 commands.

```shell 
help
```

The online manual page is located here: 

```shell 
http://x3270.bgp.nu/Unix/c3270-man.html 
```

### Adjusting display size

c3270 is a plain-text, command-line application. 3270 displays are not resizeable anyway. If the text is too small to read comfortably, use your operating system's facility to zoom in, such as Cmd+ on a Mac. 

### Connect

```shell
Connect [ip addr]:[port]
```

Example:

```shell
Connect 23.229.8.213:8723
```

You can also specify the IP address and port on the ```c3270``` command:

```shell 
c3270 23.229.8.213:8723
```

### Disconnect 

After exiting whatever z/OS applications you were using (such as TSO or CICS), enter ```logoff``` at the command prompt.

c3270 is a command-line application and you are working in a terminal window. The display may scroll. If the cursor appears to be in the right position for you to enter a command but the display indicates "X Protected", press the Tab key to jump to an enterable field. It will not be visually apparent where the enterable field is located on your monitor.









