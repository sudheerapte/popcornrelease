# popcornrelease
releases of popcorn

Latest release = `popcorn-0.1.0.tar.gz`

# Installing popcorn on Linux

(What is Popcorn? See the Popcorn manual:
https://github.com/sudheerapte/popcornserver/tree/dev/doc)

Installing Popcorn just creates a directory you can place anywhere on
your machine. The directory contains all the code it needs except for
NodeJS, and makes no references to any other files.  You can move the
whole directory anywhere you want and launch Popcorn.

1. Make sure you have NodeJS v.10 LTS or newer on your PATH, i.e., you
can run `node -v` directly from the command line and it prints a
version number like `v10.15.1`.

2. Untar the file `popcorn-`x.y.z`.tar.gz` in some directory and
`cd` into it.

3. Run the `bin/initialize` command, which creates a `.popcorn`
directory in your home directory with a default configuration and a
little demo program.

4. To start Popcorn, run `node ./bin/launch`.

This should start the Popcorn NodeJS process in the foreground. You
can stop the process by killing it with `^C`.

The process contains a web server listening on TCP port 8000, and a
Popcorn app server listening on TCP port 8001.  It also contains a
built-in demo app.

You can connect to a demo "machine" by typing in your browser:

```
http://localhost:8000/demo
```

It should show a simple app updating its page every ten seconds. The
page shows a button with which you can immediately change the state, too.

If you can see this app, then you have installed Popcorn correctly.

5. To start your own Popcorn app, tell popcorn where to find your
machine directory. In `~/.popcorn/options.json`, create an entry for
your machine name and its directory path.  Make up a name for your
machine (all lowercase letters) and make sure that the machine
directory exists and has at least a file called `frags.html`.

When popcorn is launched, it will read this options file and will be
able to locate your machine assets and show the initial state of your
machine on a web page.

To access your app page from the browser, provide the name of your
machine as the "path" portion of your URL, like the word "demo" above.

To dynamically modify your app state, you will have to write a program
following the instructions in the Popcorn manual.

## Documentation

* Popcorn manual: https://github.com/sudheerapte/popcornserver/tree/dev/doc

* Popcorn roadmap: https://github.com/sudheerapte/popcornserver/tree/dev/doc (see section Roadmap)


