---
title:  "Build Exe File Out Of Python Script"
date:   2021-04-15 22:10:00 +0545
categories: [Python]
tags: [PyInstaller]
---

## Introduction

PyInstaller is a popular and powerful tool for converting Python scripts into standalone executable files. This tool is useful for a variety of reasons, such as distribution, protection of source code, or simply making it easier for non-technical users to run Python scripts.

In this article, we will explore how to use PyInstaller to build an executable file from a Python script.

## What is PyInstaller?

PyInstaller is a Python package that can be used to convert Python scripts into standalone executable files. It supports a variety of platforms, including Windows, Mac, and Linux.

PyInstaller works by analyzing the script and building an executable bundle that includes the Python interpreter, any required modules, and the script itself. This bundle is then compressed and packaged into a single file, which can be distributed and run on any machine with the appropriate platform.

## Installing PyInstaller

Before we can use PyInstaller, we need to install it. The easiest way to do this is to use pip, the Python package manager. To install PyInstaller using pip, run the following command in a terminal:

```python
pip install pyinstaller
```

## Building an executable with PyInstaller

Once PyInstaller is installed, building an executable is a straightforward process. We will use a simple Python script as an example:

```python
# addition_program.py

def add ():
    a = int(input("Enter a first number: "))
    b = int(input("Enter a second number: "))
    print(a+b)


while True:
    
    add()
    
    while True:
        ask = input("Do you want to continue? Y/N ")
        if ask.upper() == 'Y':
            add()
        else:
            quit()
```

To build an executable for this script, we simply need to run the following command in a terminal:

```terminal
pyinstaller addition_program.py
```

This will generate a folder called `dist` in the current directory, which contains the executable file. The name of the executable will be the same as the name of the script, but with an added platform-specific extension (e.g. `.exe` on Windows).

> Make sure your python path is added to system variables![^footnote]
{: .prompt-warning }

## Customizing the build process

PyInstaller supports a variety of options that can be used to customize the build process. For example, we can specify additional files or directories to include in the bundle, exclude certain modules, or set the icon for the executable.

These options can be specified using a `.spec` file, which is a Python script that defines the build configuration.

### Generating a `.spec` file

To generate a `.spec` file for our example script, we can use the following command:

```terminal
pyinstaller --name addition_program --onefile addition_program.py
```

This command generates a `addition_program.spec` file in the current directory. The `--name` option allows us to specify the name of the final executable, and the `--onefile` option tells PyInstaller to bundle everything into a single executable file.

### Adding additional files

Sometimes we need to include additional files or directories in the final executable. This can be done by modifying the `.spec` file.

For example, let's say we have a text file called `example.txt` that our script reads from. To include this file in the final executable, we need to add the following line to the `Analysis` section of the `.spec` file:

```python

datas=[('example.txt', '.')]
```

This tells PyInstaller to include `example.txt` in the bundle and to place it in the same directory as the executable.

### Excluding modules

PyInstaller may include modules that are not needed by our script, which can bloat the final executable. We can exclude these modules by modifying the .spec file.

For example, let's say our script uses the `numpy` module, but we know that it will not be needed in the final executable. To exclude `numpy`, we need to add the following line to the `Analysis` section of the `.spec` file:

```python
excludes=['numpy']
```

This tells PyInstaller to exclude the numpy module from the bundle.

### Specifying the icon

We can specify a custom icon for the final executable by adding the following line to the `Analysis` section of the `.spec` file:

```python
icon='path/to/icon.ico'
```

This tells PyInstaller to use the specified icon for the final executable. Note that the icon file must be in the ICO format.

## Building the executable

To build the final executable using the modified `.spec` file, we simply need to run the following command in the terminal:

```terminal
pyinstaller addition_program.spec
```

This will generate a `dist` folder containing the final executable, along with any additional files or directories that were included in the build.

## Conclusion

In this article, we explored how to use PyInstaller to build an executable file from a Python script, as well as how to customize the build process using a .spec file. PyInstaller is a powerful tool that makes it easy to distribute and run Python scripts without requiring the user to install Python or any additional modules. By customizing the build process, we can create optimized and professional-looking executables that meet our specific needs.

## Resources

[^footnote]: https://github.com/pyinstaller/pyinstaller/issues/5248
