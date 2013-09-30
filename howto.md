Deploying Python Code Online
=====

The question here, in general, is how to take a piece of Python code
that depends on libraries like numpy and implement it online.  My
initial thought was to use Brython (http://www.brython.info), but
Brython apparently can't import any libraries.  This means we probably
have to run the Python code server side and have a web server
interface between the code and the webpage.

The Basic Architecture
------

Since we're doing things server side, we'll imagine that we're using
EC2.  The only experience I have with this in the past is using the
PsiTurk package, which uses a Python based web server called
`gunicorn`.  A good first step for me would probably be to start a web
server that can do the following:

1. Load a file
2. Run some Python stuff on it
3. Print the results

Undoubtedly, this is going to have some security implications.  That's
something to think about as we progress!


