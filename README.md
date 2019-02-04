# popcornrelease
releases of popcorn

Latest release = `popcorn-0.0.5.tar.gz`

# Installing popcorn

1. Make sure you have NodeJS 8.10 LTS or newer on your PATH, i.e., you
can run "node -v" directly from the command line and it prints a
version number like "v8.10.0".

2. Untar the file `popcorn-`x.y.z`.tar.gz` in some directory and
'cd' into it.

3. Execute this command:

node ./bin/launch

This should start a web server listening on port 8000. You can connect
to a demo "machine" by typing in your browser:

http://localhost:8000/t2

It should show the word "t2" in the title bar, and a blank page.

4. Tell popcorn where to find your machine:

Your machine directory should contain at least a file named
`frags.html`, containing `<div>` elements and other HTML content and
assets.

Create a directory `.popcorn` in your home directory, and in it a file
named `options.json`. The server directory has an example
`options.json` file to copy.  Create an entry for your machine and its
directory path in this file. When popcorn is launched, it will read
this options file and will be able to locate your machine.

To access your machine from the browser, provide the name of your
machine as the "path" portion of your URL, like the word "t2" above.


