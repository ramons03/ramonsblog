title: python django utils
author: Ramon Sanchez
author_id: ramons
language: en-US
publisher: Ramon Sanchez
date: 2017-07-16 09:53:05
tags:
---
another easy way to do this is to run:

[user@host]$screen
[user@host]$python manage.py runserver 0.0.0.0:8000
Now press Ctrl+A and then press d to exit from this screen.

This creates the server in a screen and then detaches it. This way you can simply go back in and type:

[user@host]$screen -r

https://jeffknupp.com/blog/2012/02/09/starting-a-django-project-the-right-way/



248
down vote
accepted
This works for me:

$ pip install -r requirements.txt --no-index --find-links file:///tmp/packages
--no-index - Ignore package index (only looking at --find-links URLs instead).

-f, --find-links <URL> - If a URL or path to an html file, then parse for links to archives. If a local path or file:// URL that's a directory, then look for archives in the directory listing.


ps auxw | grep runserver








 A fully functional Django project
2. All resources under source control (with git)
3. An environment independent install of your project (using virtualenv)
4. Automated deployment and testing (using Fabric)
5. Automatic database migrations (using South)
6. A solid start to your new site



$ virtualenv env
or, if virtualenv isn't in your $PATH (though it should be):

$ python virtualenv.py --distribute env


Now that we have a virtualenv environment, we need to activate it. This sets up various environment variables to effectively bypass the system's Python install and uses our env one instead. Activate like so:

$ source ./env/bin/activate
You should see (env) $ at your prompt, letting you know that you're running under the 'env' virtualenv install. At any time, just type:

$ deactivate
to stop using virtualenv.