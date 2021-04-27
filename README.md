# What I Learned In Week 13 At Code Immersives

&nbsp;

## .gitignore

When you make commits in a git repository, you choose which files to stage and commit by using git add FILENAME and then git commit. But what if there are some files that you never want to commit? It's too easy to accidentally commit them (especially if you use git add . to stage all files in the current directory). That's where a .gitignore file comes in handy. It lets Git know that it should ignore certain files and not track them.

&nbsp;

What Kind of Files Should You Ignore?

- Log files
- Files with API keys/secrets, credentials, or - sensitive information
  Useless system files like .DS_Store on macOS
- Generated files like dist folders
- Dependencies which can be downloaded from a package manager

You can get an idea for what sort of files to ignore on gitignore.io, by selecting your operating system, text editor or IDE, languages, and frameworks.

&nbsp;

How .gitignore Works

Here's how it works. A .gitignore file is a plain text file where each line contains a pattern for files/directories to ignore. Generally, this is placed in the root folder of the repository, and that's what I recommend. However, you can put it in any folder in the repository and you can also have multiple .gitignore files. The patterns in the files are relative to the location of that .gitignore file.

Literal File Names

The easiest pattern is a literal file name, for example:

    .DS_Store

This will ignore any files named .DS_Store, which is a common file on macOS.

Directories

You can ignore entire directories, just by including their paths and putting a / on the end:

    node_modules/
    logs/

If you leave the slash off of the end, it will match both files and directories with that name.

&nbsp;

## jQuery

jQuery is a fast, small, and feature-rich JavaScript library. It makes things like HTML document traversal and manipulation, event handling, animation, and Ajax much simpler with an easy-to-use API that works across a multitude of browsers. With a combination of versatility and extensibility, jQuery has changed the way that millions of people write JavaScript.

https://jquery.com/

&nbsp;

## window.localStorage

The localStorage read-only property of the window interface allows you to access a Storage object for the Document's origin; the stored data is saved across browser sessions.

localStorage is similar to sessionStorage, except that while localStorage data has no expiration time, sessionStorage data gets cleared when the page session ends — that is, when the page is closed. (localStorage data for a document loaded in a "private browsing" or "incognito" session is cleared when the last "private" tab is closed.)

    myStorage = window.localStorage;

&nbsp;

The localStorage mechanism is available via the Window.localStorage property. Window.localStorage is part of the Window interface in JavaScript, which represents a window containing a DOM document.

The Window interface features a wide range of functions, constructors, objects, and namespaces. Window.localStorage is a read-only property that returns a reference to the local storage object used to store data that is only accessible to the origin that created it.

How does localStorage work?
To use localStorage in your web applications, there are five methods to choose from:

- setItem(): Add key and value to localStorage
- getItem(): This is how you get items from localStorage
- removeItem(): Remove an item by key from localStorage
- clear(): Clear all localStorage
- key(): Passed a number to retrieve the key of a localStorage
- setItem(): How to store values in localStorage
  Just as the name implies, this method allows you to store values in the localStorage object.

It takes two parameters: a key and a value. The key can be referenced later to fetch the value attached to it.

    window.localStorage.setItem('name', 'Obaseki Nosa');

Where name is the key and Obaseki Nosa is the value. Also note that localStorage can only store strings.

To store arrays or objects, you would have to convert them to strings.

To do this, we use the JSON.stringify() method before passing to setItem().

&nbsp;

## Modular Code / Modular programming

Modular programming is a software design technique that emphasizes separating the functionality of a program into independent, interchangeable modules, such that each contains everything necessary to execute only one aspect of the desired functionality.

Writing a Modular Code is an important step in software development as it allows the use of the same code in the module by referencing it to perform a specific action in different locations in the program. This method facilitates the debugging of large programs, increase code reusability & readability, improves reliability, and also helps in programming with multiples devs or teams.

    “The ratio of time spent reading versus writing is well over 10 to 1. We are constantly reading old code as part of the effort to write new code. Therefore, making it easy to read makes it easier to write.”

    Robert C. Martin, Clean Code: A Handbook of Agile Software Craftsmanship

&nbsp;

    “Always code as if the guy who ends up maintaining your code will be a violent psychopath who knows where you live.”

    John F. Woods
