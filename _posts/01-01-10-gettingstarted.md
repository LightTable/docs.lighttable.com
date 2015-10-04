---
layout: post
title: "Getting Started"
link: "start"
order: 1
tags: []
---

###Full tutorials

* [Getting started with Light Table](/tutorials/full/)

###Opening and creating new files

To create a new file, use the `New file` menu item in the `File` menu or press cmd/ctrl-n
To open a file, use the `Open file` menu item in the `File` menu or press cmd/ctrl-shift-o

###With Clojure

If you're new to Clojure, the quickest way to get going is to use the "Instarepl" - an environment for Clojure where everything you type is evaluated immediately. To do that:

1. In the view menu click the `commands` item (or press Ctrl+Space)
2. Type "insta" and press enter when the `Instarepl: Open a clojure instarepl` command is highlighted.
3. Type "(+ 3 4)" in the editor that was opened
4. Wait for the client to connect. If this is your first time it may take a couple minutes while it fetches all of the Clojure client's dependencies.
5. Once connected, type more code and see the results!

If you have some Clojure code in a file already, you can get going with inline eval by:

1. Create a new file and save it with a .clj extension or open a .clj file
2. Press Cmd/Ctrl+Enter to evaluate a form
3. Wait for the client to connect (this can take a bit the first time)
4. Once connected you'll see your result.

###With Javascript/HTML/CSS

In order to evaluate Javascript, HTML, or CSS, we need a browser to see the result in. To open a browser tab in Light Table:

1. In the view menu click the `commands` item
2. Type "brows" and press enter when the `Browser: add browser tab` command is highlighted
3. Use the url bar at the bottom to open your page (note: this can be a `file://` url to open an html file locally, or it can be something on the internet/localhost).

Now that we have a place to send our code, let's open a .js file and eval something:

4. Create a new file and save it with a .js extension or open a .js file
5. Press Cmd/Ctrl+Enter while the cursor is over a top-level block of code. To eval an inner block, select and then eval it.
5. Select the webpage name from the available clients popup
6. You'll now see results inline!
7. Evaling from a .css file will inject the css into the page.
8. Evaling from an .html file will refresh the browser tab.

###With Python

Getting started with Python is as simple as:

1. Create a new file with a .py extension or open a .py file
2. While over some code press Cmd/Ctrl+Enter
3. Allow Light Table a few seconds while it connects to a python process
4. You'll now see results inline!

If you want to use Light Table to do matplotlib/pylab graphs and such, you'll want to install the IPython kernel:

1. Follow these [instructions](http://ipython.org/ipython-doc/stable/install/install.html) to install IPython (note: it must IPython 1.0 or greater and you *must* install pyzmq as well in order for it to work with Light Table.)
2. Make sure IPython is on your path
3. Restart Light Table
4. Open a .py file by pressing Cmd/Ctrl+Shift+O
5. Over an expression that will return a graph, press Cmd/Ctrl+Enter
6. You'll see the graph embedded below your expression.


###With the workspace tree (or how to open files)

Opening each file individually through the native open dialogs isn't very efficient. The `workspace` tree allows you to instead add files and folders into a file explorer that you can then use to open/rename/delete/etc the files you're interested in. To open the workspace tree, click the `Workspace` item in the view menu. You can then add files or folders to the workspace using the buttons at the top.

![workspace tab](/images/start/wsadd.png)

Once you have items in your workspace, you can use the right-click context menu to do the standard file actions you would expect (rename, delete, new file, etc) as well as remove them from the workspace if you no longer want them there.

![workspace tab menu](/images/start/wsmenu.png)

When you open a new window of Light Table, you'll be given a new blank workspace - if you want to switch to a recently used one, click the recent button and select one of your old workspaces from the list.

![workspace tab recent](/images/start/wsrecent.png)

###With the Navigate pane

Once you have files and folders in your workspace, the `navigate` pane provides the quickest way to open a file by name. Opening it is bound to Cmd/Ctrl+O by default.

![navigate tab](/images/start/navi.png)

The navigate tab is a "filter list" where typing in the top input will filter the results down to those that match what you've typed. All filter lists inside of Light Table use a form of sequential partial substring matching, which is a fancy way of saying that you can type letters and as long as those letters appear in order in one of the list items it will be considered a match. This allows you to type "mcf" to match "my-cool-file" and so on, dramatically increasing efficiency of filter operations.

![navigate tab filtered](/images/start/navi2.png)

###With the Connections pane

The `connect` pane shows you a list of currently connected "clients" that can be used for doing language operations like eval. To open it, use the `Connections` item in the `View` menu or the `Connect: Show connect bar` command.

![connect tab](/images/start/con.png)

This list allows you to disconnect a client, which often kills the process it is associated to, or unset a client associated to an editor. You might do the latter when you want to change the context in which you eval something, for example. Clients associated with the currently active editor will appear highlighted.

![connect tab](/images/start/consel.png)

The `connect` tab also allows you to explicitly add a connection to a client, by presenting a list of all the available client type for you to select one from.

![connect tab](/images/start/conadd.png)

###With the Command pane

The `command` pane is your one stop shop to figure out if Light Table can do something. It's a filter list like navigate that presents a list of all the visible commands in Light Table. Want to open a file or change some setting? Type "open file" or "setting" to filter down to what you want to do and then press enter to do it. Opening the `command` pane is bound to Ctrl+Space by default, but you can use the `Commands` item in the `View` menu as well.

![command tab](/images/start/cmd.png)

The command pane will also show keybindings for the given command underneath the command's name.

![command tab](/images/start/cmdopts.png)
