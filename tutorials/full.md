---
layout: tutorial
title: "Getting started with Light Table"
---

_Note: Videos are based on an older version that has an outdated configuration format. For up-to-date configuration, see this [section for keymaps](/#configure-keybindings) and this [section for behaviors](/#configure-behaviors)_

###Starting Light Table

So let’s start by simply opening Light Table. The main screen is pretty basic, but it contains an important link - Light Table’s documentation. These docs have basic directions if you ever get lost or need to figure something out. You can open the documentation at any time from the help menu, or on the web at docs.lighttable.com.

In general, the best place to start finding things you can do in Light Table is use the command pane on the right. By hitting `Ctrl-Space` or going to `View -> Commands`, the command pane comes up, where you can type in whatever you want to do.

The command pane is a filter list, which is a useful feature that will narrow down the results based on what you type. In essence, it means you can type letters and as long as those letters appear in order in any list item, the command pane will show that item to you. For example, I could type “ltd” to match “Light Table’s documentation”. You can find nearly any command in the command pane, from creating new files to customizing your Light Table experience. One other small detail to notice here is that any command that has a keybinding associated with it will show that keybinding in underneath the command in the list.

<iframe width="560" height="315" src="//www.youtube.com/embed/CPGlgWSQb3U" frameborder="0" allowfullscreen></iframe>

###The Workspace Tree
To begin working in Light Table, all you need to do is create a new file or open an existing one. `Cmd-N` or `File -> New file` will let you create a new file in a new tab, which will be untitled for the time being. You can also open a file already on your computer with `Cmd-Shift-O` or `File -> Open file`.

If you're working with multiple files, it’s inefficient to open them individually with the native open dialog, so instead we’ll use the workspace. By going to `View -> Workspace` you can open the workspace tree on the left, where you'll see the options to open a folder, a file, or recent workspaces. If you right click on a blank area in the workspace, it gives you the option to add files or folders. If you right click on files and folders already in the workspace, it gives you options such as renaming them, removing them from the workspace, or adding more folders inside others.

If you clear the workspace or open a new window of Light Table, the workspace will be blank, but you can switch back to an old workspace by clicking on the recent button and selecting any of your old workspaces. It’s also useful to note that once a file has been added to your workspace, you can easily access it later with the navigate pane, which you can bring up with `Cmd-O`. The navigate pane is a filter list just like the command pane to make it easy for you to find your files.

<iframe width="560" height="315" src="//www.youtube.com/embed/8C3yTweZOIU" frameborder="0" allowfullscreen></iframe>

###Tabs and Tabsets
Light Table opens each of your files as a tab so as you open multiple files you can easily navigate between them. Tabs don’t have to be just your files though - Light Table can also open a browser window in a tab. If you open the command pane and begin typing “browser”, you’ll see an option called `Browser: add browser tab`. This will open a browser window with the URL bar at the bottom. From there you can navigate to a website, or preview locals files on your machine.

While your files are consolidated into tabs, sometimes you need to see things side-by-side, and for this there are tabsets. To add a tabset, open up the command pane and type "tabset" to find the command `Tabset: Add a tabset`. By choosing this command, you'll see that Light Table will split your editor window, and you can drag any open tabs to the top of the new tabset to view them there. You can open as many tabsets as you'd like, dividing Light Table into halves, thirds, and so on. Bear in mind though that opening additional tabsets applies to the whole editor, not just a single tab.

<iframe width="560" height="315" src="//www.youtube.com/embed/6qBVSQO8g-E" frameborder="0" allowfullscreen></iframe>

###Evaluation and the Console
One of the things that makes Light Table powerful is the ability to try out code right in the editor to see what it does. To do this, all you need to do is write some code in the editor and have Light Table evaluate it. Hitting `Cmd-Enter` will evaluate the line of code your cursor is on, but nothing else. Hitting `Cmd-Shift-Enter` will evaluate the entire file. Most basic examples such as the canonical “Hello, world!” print to the console, but if you try this, your results aren’t immediately apparent. There is however a teal box in the bottom right with some numbers in it. This means there is new information in the console. If you click that teal box or go to `View -> Console`, the console will appear from the bottom. You will see that Light Table has provided as standard output, labeled stdout, whatever your program said to print, allowing you to see the results of your program. The console can be treated just like another tab if you so desire by right clicking the console and selecting Open console tab.

<iframe width="560" height="315" src="//www.youtube.com/embed/KyjSBiU1oU8" frameborder="0" allowfullscreen></iframe>

###Inline Evaluation
Viewing results in the console is sufficient for a lot of early work, particularly if there are only one or two print commands in your code, but it does have its limitations. The most obvious one is that it doesn't actually tell you which block of code produced which result. If you have one function that prints true or false and another that prints a number, it's pretty easy to deduce which result came from which function, but code isn't always that simple. Light Table shows you results inline, which helps enormously to understand what's going on. You may have noticed that when you hit the evaluate command, little blue boxes show up to the right of the code, one next to each block of code. You’ll notice that some only get a check mark - this is telling you that Light Table successfully evaluated a statement. Statements don’t return anything, so the check is just a simple way to tell you that the statement is a valid one. The boxes next to expressions however, will show you the results of that expression, whether it's nothing (none/nil/null), true/false, a string, or a number, etc. If there's an error in your code, a red box will appear with a stack trace telling you what sort of error prevented that block of code from working.

<iframe width="560" height="315" src="//www.youtube.com/embed/7YIaHyTdjTY" frameborder="0" allowfullscreen></iframe>

###Evaluating with Python
To let Light Table know your code is in Python, save the file with a .py extension or use the command pane to find `Editor: Set current editor syntax` and choose Python from the list. Once a file’s syntax is set to Python, Light Table will use the Python interpreter to evaluate your code.

Seeing inline results with Python is very simple - after evaluating a line or an entire file, Light Table will connect to a Python process and display your results inline.

<iframe width="560" height="315" src="//www.youtube.com/embed/tdrNme7A1fc" frameborder="0" allowfullscreen></iframe>

###Evaluating with Javascript
To let Light Table know which languages you’re using, save the files with .html, .css, or .js extensions or use the command pane to find `Editor: Set current editor syntax` and choose HTML, CSS, or Javascript from the list. Once each file’s syntax is set to its respective language, Light Table will know how to evaluate your code.

When you evaluate a Javascript file, Light Table will usually ask you to connect to a client. You can choose to connect to a browser if you want to inject your Javascript into a webpage, or you can connect to the Light Table UI if your Javascript is a stand-alone program and only needs to be evaluated in a local context.

Evaluating HTML will open a browser tab if there isn’t one available already, or refresh the browser tab it’s connected to. Evaluating CSS, similar to Javascript, will prompt you to choose a client and inject that CSS into a browser page.

<iframe width="560" height="315" src="//www.youtube.com/embed/oEBEa1mJD5Q" frameborder="0" allowfullscreen></iframe>

###Evaluating with Clojure
To let Light Table know your code is in Clojure, save the file with a .clj extension or use the command pane to find `Editor: Set current editor syntax` and choose Clojure from the list. Once a file’s syntax is set to Clojure, Light Table will use the Clojure client to evaluate your code.

Seeing inline results with Clojure is very simple - after evaluating a line or an entire file, Light Table will connect to a Clojure process and display your results inline.

<iframe width="560" height="315" src="//www.youtube.com/embed/FMZphPbO8gk" frameborder="0" allowfullscreen></iframe>

###Clojure in the Instarepl
Another way to evaluate Clojure code is with the instarepl, an environment that not only evaluates your code in real time, but also shows how your values flow through your code. To open an instarepl, use the command pane to choose `Instarepl: Open a clojure instarepl`. You can also turn a regular Clojure file into an instarepl with `Instarepl: Make current editor an instarepl`. In an instarepl, your Clojure code with be automatically evaluated with results being displayed inline.

<iframe width="560" height="315" src="//www.youtube.com/embed/YY6B9EHbH24" frameborder="0" allowfullscreen></iframe>

###User Keymaps and Behaviors
While the menu, the workspace tree, and the command pane provide a way to do nearly everything in Light Table, it is often inefficient to go hunting and clicking through them to get what you want. Light Table comes with some common key bindings already in place (`Cmd-O` to open, `Cmd-S` to save, `Cmd-N` for a new file, to name a few), but you may decide there are certain actions that you take frequently enough to want a key binding. You can set these key bindings yourself by opening the command pane and typing "keymap" to bring up the option entitled `Settings: User keymap`. The markup syntax the keymap file uses may not be familiar to you, but the format is relatively easy to discern, and Light Table has auto-complete to help you find what you want. Inside the brackets, you can see two sets of brackets named `:app` and `:editor`. Key bindings set under `:app` will function in all of Light Table, regardless of whether or not you have a file open. Some good examples would be creating a key bind to toggle the workspace tree or the console. Key bindings set under `:editor` will function only when you have an editor window focused. A good example of this would be unindenting by one tab length (a convenient feature when dealing with Python's use of whitespace to indicate run order).

<iframe width="420" height="315" src="//www.youtube.com/embed/F5cuKPr7I44" frameborder="0" allowfullscreen></iframe>

Behaviors are another aspect of Light Table that you may want to customize. Behaviors dictate settings like font size or color themes. Using the command pane to select `Settings: User behaviors`, you can see a similar layout to the keymap file, with the tags `:app` and `:editor` again. Changing behaviors lets you customize both the appearance and functionality of Light Table to your liking.

<iframe width="420" height="315" src="//www.youtube.com/embed/CBi_W7K1VYk" frameborder="0" allowfullscreen></iframe>
