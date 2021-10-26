# Introduction to Windows Subsystem for Linux (WSL2) Environment Setup

In this module, we will walk through the process of setting up your Windows 10
local development environment.

> **Note:** If you are not using a Windows computer for this course, skip the
> lessons in this module.

## Brief History

### Understanding Environments

A **software environment** describes the set of tools that work together to
enable you to develop and execute the code that you write. Environments
typically include the operating system, databases, programming languages, and
related tools like text editors or browsers.

### Comparing Environments with Machines

You may hear us use the term "software environment" and "machine" to mean
similar things. A **machine** describes the physical hardware that your software
environment runs on. You'll hear the term machine and computer used
interchangeably. Different machines (like PCs and Macs) use different hardware
to run the programs that they use. Differences in those machines mean that
setting up your development environment on one type of machine could look much
different than setting it up on another.

### Windows Subsystem for Linux (WSL)

To work around some of the differences between machines, and specifically
between operating systems, we recommend that all students whose computers come
pre-installed with the Windows operating system use a tool called **Windows
Subsystem for Linux (WSL)**. Windows Subsystem for Linux provides a Linux-based
environment for interfacing with and developing on a Windows operating system.

**Linux** is a family of operating systems that share the same core operating
system programs. Operating systems based on Linux are very commonly used in
professional software engineering settings. Learning how to use a Linux-based
operating system will be a valuable skill for your future software engineering
career.

The version, or distribution, of Linux that you will use is called **Ubuntu**.
It is one of the leading Linux distributions and has great support with Windows
Subsystem for Linux. There are others like Debian and Fedora, and those should
work similarly.

The advantage of using Windows Subsystem for Linux is that it's highly
integrated into Windows 10, works on most machines that support Windows 10, and
only needs to be enabled and configured.

The first version of Windows Subsystem for Linux (WSL 1) was groundbreaking! It
translates commands that you run with Linux into commands that Windows can
understand. For this course, we'll use the second version of Windows Subsystem
for Linux (WSL 2). The first version had some compatibility issues and was
slower compared to native Windows.

### Terminals and Shells

You may be familiar with opening files and applications on your computer by
clicking icons, or viewing a website by typing an address into the address bar
and seeing what pops up. These **graphical user interfaces (GUIs)** created a
revolution in computing and are still extremely helpful in getting work done for
many non-technical computer users.

Before graphical user interfaces (GUIs), the way to tell the computer to do
something was through a **terminal**. The terminal included a screen, which
would display only text, and a keyboard. The screen and keyboard were connected
to a computer, and you would type into the keyboard what you wanted the computer
to do. Then, you would press `<Enter>` and wait for the computer to finish.

Terminals are still used frequently today, especially in software development.
We can connect to another computer on the internet, give it instructions by
typing in commands, and view the result on our screen. The way that modern
computers emulate the terminals of yesterday is through a program called a
**command-line interface**, or a **shell**.

Similar to operating systems, there are many different types of shells. The
shell that Flatiron School supports on the Ubuntu operating system is called
**bash**, short for Bourne Again Shell.

### Windows Command Prompt

Before we get to **bash**, however, we need to do some work in the "Command
Prompt", which is the built-in shell on Windows computers.

The "Command Prompt" application is a text-based way to browse and work with
your computer files. We will only be using the "Command Prompt" application
at the beginning of the environment setup. For now, let's start to see what
"Command Prompt" and, more generally, **shell**s can do.

## Action Items: View Your Desktop in "File Explorer" and "Command Prompt" Applications

To complete the environment setup, you will need to be able to open
applications. You can open new applications by using the search bar at the
bottom of your screen. The search bar says, "Type here to search".

### View Your Desktop in the "File Explorer"

The "File Explorer" application is a visual way to browse the files on your
computer. You may already be familiar with the "File Explorer" application. This
application allows you to quickly see the files on your desktop, downloads,
documents, pictures, music, videos, and much more.

1. Click on the "Start" menu search bar
2. Type "File Explorer" and open the application
3. Find and open the "Desktop" folder located on the left-hand side in your
   "File Explorer"

### View Your Desktop in the "Command Prompt" Shell

The "Command Prompt" application is the terminal that will allow us to interface
with our computer through a shell. This action item is primarily to get you
comfortable running commands in _any_ shell so that you can work through the
environment setup on your own.

1. Click on the "Start" menu search bar
2. Type "Command Prompt" and open the application
3. Type `cd /Users` into the terminal and press `<Enter>`
4. Type `dir` into the terminal and press `<Enter>`
5. Look for your username in the list
6. Type `cd` into the terminal, add a space, and type your name as it appears in
   the list and press `<Enter>`
7. Type `dir` into the terminal and press `<Enter>`
8. Look for the "Desktop" folder in the list
9. Type `cd Desktop` into the terminal and press `<Enter>`
10. Type `dir` into the terminal and press `<Enter>`

### Check Your Work

<iframe width="560" height="315" src="https://www.youtube.com/embed/gLtUXeP2T50" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

If you were able to open your Desktop folder in the "File Explorer" application
and you were able to open the "Command Prompt" application and `cd` to the same
folder, you should see the same list of files and folders in both the
**graphical user interface (GUI)** and in the **command-line interface (CLI)**
or shell.

This may be your first time using the "Command Prompt" or any terminal or shell.
Now you know how to see the items in a particular folder through the "File Explorer"
_and_ through the "Command Prompt". This step is to get you familiar with using
a terminal to be able to complete the environment setup.

## Preparing for Your Environment Setup

- During the environment setup, you will be spending a lot of time in the
  "Ubuntu" application.
- As much as possible, copy and paste commands that we ask you to run there
  instead of typing by hand to help prevent environment setup issues.
- Specific keys that you need to press will be surrounded by `<` `>` (for
  example, `<Shift>`, `<Space>`, `<Enter>`).
- You will need to be comfortable switching between windows; we will primarily
  be using the browser and the "Ubuntu" application.
- You should be able to start and stop the environment setup.
- If you get stuck, reach out to your classmates or an instructor.
