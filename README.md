# popcornrelease
releases of popcorn

#Installing popcorn

1. Make sure you have NodeJS 8.10 LTS or newer on your PATH, i.e., you
can run "node -v" directly from the command line and it prints a
version number like "v8.10.0".

2. Untar the file popcorn-VERSION.tar.gz in some directory and 'cd' into
the "server" directory inside it. (VERSION is a string like 0.0.2)

3. Execute this command:

node ./launch.js

This should start a web server listening on port 8000. You can connect
to a demo "machine" by typing in your browser:

http://localhost:8000/demo

It should show the word "t2" in the title bar, and a blank page.

4. Tell popcorn where to find your machine:

Create a directory ".popcorn" in your home directory, and in it a file
named "options.json". The server directory has an example file to copy.
Create an entry for your machine and its directory path.

The machine directory should contain at least a file named
`frags.html`, containing `<div>` elements and other HTML content and
assets.

