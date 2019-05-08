# English

# Updater
This program is java program updater.

# How To Use
This program is executed from command.
```
java -jar Updater.jar <Download URL> <Type> <Title> <Exec Command>
```
Execute the command using java.lang.Runtime#getRuntime()#exec().  
Also, the computer that uses this program needs to be through the Java path.

You can use it by adding it to your source code.
It can be used like the command line by calling io.github.kusaanko.Updater#main(String[] args).

## Download URL
Download URL is URL of the new file download source.

For example: https://github.com/kusaanko/Updater/release/download/1.0/Updater.jar

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
java.lang.Runtime.getRuntime().exec("java -jar Updater.jar https://github.com/example/example/release/download/1.0/example.jar replace:example.jar example.jar \"java -jar example.jar\"", null, new File("./"));
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

# 日本語

# Updater
このプログラムはJavaのプログラムを更新するプログラムです。

# 使い方
このプログラムはコマンドから実行します。
```
java -jar Updater.jar <Download URL> <Type> <Title> <Exec Command>
```
コマンドを実行するにはjava.lang.Runtime#getRuntime()#exec()を使用してください。  
また、使用するにはコンピューターにJavaのパスを通しておく必要があります。

あなたのソースコードに追加しても使えます。
io.github.kusaanko.Updater#main(String[] args)を呼び出すことでコマンドラインと同様に使えます。

## Download URL
Download URLは新しいファイルのダウンロード元URLです。

例: https://github.com/kusaanko/Updater/release/download/1.0/Updater.jar

## Type
Typeは置き換える方法です。

**replace:** から始まるコマンドはjar、exe等解凍する必要がない場合に使用します。  
このコマンドの後ろには置き換えるファイル名を指定します。

例: replace:Executable.jar

**zip:** から始まるコマンドはzipファイルをダウンロードするのに使用します。  
このコマンドの後ろには何も書く必要はありません。

例: zip:

## Title
Titleはタイトルバーに表示されます。  
以下のように表示されます。

Updater - **Title**

## Exec Command
Exec Commandは更新が完了したあとに実行されるコマンドです。

例: "java -jar Executable.jar"

## Updaterを起動する例
```Java
java.lang.Runtime.getRuntime().exec("java -jar Updater.jar https://github.com/example/example/release/download/1.0/example.jar replace:example.jar example.jar \"java -jar example.jar\"", null, new File("./"));
```

# ファイル配置
root  
├ libs/  
├ Updater.jar  
├ Executable.jar  
└ etc...

# 注意
このプログラムは自分自身を更新する機能はついていません。  
UpdaterのSHA-256値を見てJavaプログラムで更新してください。  
SHA-256値はsum.txtを見てください。