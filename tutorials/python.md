---
layout: tutorial
title: "Light Table Python Tutorial"
---

###Opening Light Table

So let’s start by simply opening Light Table. The main screen is pretty basic, but an important link can be found - the documentation. The Light Table docs have basic directions if you ever get lost or need to figure out how to do something. You can always bring up the documentation from the help menu too.

In general, the best place to start finding things you can do in Light Table is use the command pane on the right. By hitting `Ctrl-Space` or going to `View` -> `Commands`, the command pane comes up, where you can type in whatever you want to do. You can type any part of what you want and Light Table will find the commands that match best. If you don't know what you're looking for or don't know how to complete a certain action, the command pane will help you find it.

<iframe width="560" height="315" src="//www.youtube.com/embed/q5zcE4rkGLM" frameborder="0" allowfullscreen></iframe>

###Starting a new Python file

Before starting a new file, you should close the welcome screen, with either `Cmd-W` or right clicking and choosing `Close tab`. With a blank window, you have to make a new tab to put your new Python file in. `Cmd-N` or `File` -> `New File` will let you create a new file in a new tab, which will be untitled for the time being. There are a couple ways to let Light Table know which language you're using. The first is by saving the file (`Cmd-S` or `File` -> `Save file`) with a .py extension, or you can also use the command pane to use the `Editor: Set current editor syntax` command. Either way, Light Table will now recognize your Python file and use the Python interpreter to evaluate your code.

<iframe width="560" height="315" src="//www.youtube.com/embed/don7hWe7VMI" frameborder="0" allowfullscreen></iframe>

###Workspace tree

If you're working with multiple files, you can view them in the workspace. By going to `View` -> `Workspace`, you can open the workspace tree on the left, where you'll see the options to open a folder, a file, or recent workspaces. If you right click on a blank area in the workspace, it gives you the option to add files or folders. If you right click on files and folders already in the workspace, it gives you options such as renaming them, removing them from the workspace, or adding more folders inside others. Just as a word of warning, there is a large difference between delete and remove from workspace; removing a file or folder from the workspace can only be done if it isn't nested inside another folder. Only parent folders and individual files you've added can be removed from the workspace. Selecting delete folder/file will delete it from your hard disk.

<iframe width="560" height="315" src="//www.youtube.com/embed/P7AXxbmLfe0" frameborder="0" allowfullscreen></iframe>

###Tabs and tabsets

As you do more work in Light Table, you'll find that you'll want to have multiple documents open simultaneously. If you already have a file open and hit `Cmd-N` again, a new tab will open up with an new untitled file. You can also open an existing file with `Cmd-Shift-O` or the workspace tree, and that file will pop up in a new tab as well. `Cmd-O` is an easy way to open files that have already been added to the workspace. A novel feature of Light Table though is the ability to open up tabs with other things, not just other files. If you open up the command pane and begin typing "browser", you'll see an option called `Browser: add browser tab`. By choosing this, you can add a tab that is an internet browser right into Light Table, where you can pull up any website you may have been using for help.

This consolidates your windows into tabs, but sometimes you need to see things side-by-side, and for this there are tabsets. To add a tabset, open up the command pane and type "tabset" to find the command `Tabset: Add a tabset`. By choosing this command, you'll see that Light Table will split your editor window, and you can drag any open tabs to the top of the new tabset to view them there. If you right click the console when it's open, you can choose to view the console as a tab, which makes it possible to view the console next to your program to keep an eye on its output. You can open as many tabsets as you'd like, dividing Light Table into halves, thirds, and so on. Bear in mind though that opening additional tabsets applies to the whole editor, not just a single tab.

<iframe width="560" height="315" src="//www.youtube.com/embed/vYGG648Hwsk" frameborder="0" allowfullscreen></iframe>

###Evaluation and the console

After you've made a new file and saved it with a .py extension, you’ll probably write some Python code. One of the things that makes Light Table powerful is the ability to try out that code right in the editor to see what it does. To do that, all you need to do is have Light Table evaluate your code. Hitting `Cmd-Enter` will evaluate the line of code your cursor is on, but nothing else. Hitting `Cmd-Shift-Enter` will evaluate the entire file. Most examples in Python tend to use the statement `print` to show you results, and if you used print in your code, your results aren’t immediately apparent. There is however a teal box in the bottom right with some numbers in it. This means there is new information in the console. If you click that teal box or go to `View` -> `Console`, the console will appear from the bottom. You will see that Python has provided as standard output, labeled stdout, whatever your Python program said to print, allowing you to see the results of your program.

<iframe width="560" height="315" src="//www.youtube.com/embed/i1omTGsilqI" frameborder="0" allowfullscreen></iframe>

###Viewing results inline

Viewing results in the console is sufficient for a lot of early work, particularly if there are only one or two print commands in your code, but it does have its limitations. The most obvious one is that it doesn't actually tell you which block of code produced which result. If you have one function that prints true or false and another that prints a number, it's pretty easy to deduce which result came from which function, but code isn't always that simple. Light Table shows you results inline, which helps enormously to understand what's going on. You may have noticed that when you hit the evaluate command, little blue boxes show up to the right of the code, one next to each block of code. You’ll notice that some only get a check mark - this is telling you that Light Table successfully evaluated a statement. Statements, like an `if` or `def` block, don’t return anything in Python, so the check is just a simple way to tell you that the statement is a valid one. The boxes next to expressions however, will show you the results of that expression, whether it's nothing (none/nil/null), true/false, a string, or a number, etc. If there's an error in your code, a red box will appear with a stack trace telling you what sort of error prevented that block of code from working.

<iframe width="560" height="315" src="//www.youtube.com/embed/sgTD_qPPCuo" frameborder="0" allowfullscreen></iframe>

###User keymap and behaviors

While the menu, the workspace tree, and the command pane provide a way to do nearly everything in Light Table, it is often inefficient to go hunting and clicking through them to get what you want. Light Table comes with some common key bindings already in place (`Cmd-O` to open, `Cmd-S` to save, `Cmd-N` for a new file, to name a few), but you may decide there are certain actions that you take frequently enough to want a key binding. You can set these key bindings yourself by opening the command pane and typing "keymap" to bring up the option entitled `Settings: User keymap`. The markup syntax the keymap file uses may not be familiar to you, but the format is relatively easy to discern, and Light Table has auto-complete to help you find what you want. Inside the brackets, you can see two sets of brackets named `:app` and `:editor`. Key bindings set under `:app` will function in all of Light Table, regardless of whether or not you have a file open. Some good examples would be creating a key bind to toggle the workspace tree or the console. Key bindings set under `:editor` will function only when you have an editor window focused. A good example of this would be unindenting by one tab length (a convenient feature when dealing with Python's use of whitespace to indicate run order).

<iframe width="560" height="315" src="//www.youtube.com/embed/F5cuKPr7I44" frameborder="0" allowfullscreen></iframe>

Behaviors are another aspect of Light Table that you may want to customize. Behaviors dictate settings like font size or color themes. Using the command pane to select `Settings: User behaviors`, you can see a similar layout to the keymap file, with the tags `:app` and `:editor` again. Changing behaviors lets you customize both the appearance and functionality of Light Table to your liking.

<iframe width="560" height="315" src="//www.youtube.com/embed/CBi_W7K1VYk" frameborder="0" allowfullscreen></iframe>

