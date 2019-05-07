# Updater
This program is java program updater.

# How To Use
This program is executed from command.
```
java -jar Updater.jar <Download URL> <Type> <Title> <Exec Command>
```
Execute the command using java.lang.Runtime#getRuntime()#exec().  
Also, the computer that uses this program needs to be through the Java path.

## Download URL
Download URL is URL of the new file download source.

For example: https://github.com/kusaanko/Updater/release/download/1.0.0/Updater.jar

## Type
Type is type of replace way.

Command beginning with **replace:** is used to update files that you download, such as jar and exe that do not need to be extracting.  
After this command, specify the replacement file name.

For example: replace:Executable.jar

Command beginning with **zip:** is used when the file to be downloaded is zip.  
There is no need to write anything after this command.

For example: zip:

## Title
Title is viewed title bar.  
It will be displayed as below.

Updater - **Title**

## Exec Command
Exec Command is a command to be executed after the update is completed.

For example: "java -jar Executable.jar"

## Example of program to start Updater
```Java
java.lang.Runtime.getRuntime().exec("java -jar Updater.jar https://github.com/example/example/release/download/1.0.0/example.jar replace:example.jar example.jar \"java -jar example.jar\"", null, new File("./"));
```

# File Placement
root  
├ libs/  
├ Updater.jar  
├ Executable.jar  
└ etc...

# Notes
This program does not have its own update feature.  
Check the SHA-256 value from the source Java program and update it.  
The SHA-256 value is described in sum.txt.