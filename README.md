##How To Run
This is a Django application and with postgres required the first thing you'll need to do it setup postgres db on your end.
Digitalocean offers a nice tutorial that includes how to install postgres on ubuntu assuming the OS your using is linux based and has the same architecture you should be able to setup this easily.
https://www.digitalocean.com/community/tutorials/initial-server-setup-with-ubuntu-18-04

Next step is setting up a virtualenv like so "virtualenv venv --python=python3"
There's one above this folder (the folder that contains this folder) but just incase it doesn't work, try "pip freeze" then delete that and create a new one.

Install dependencies using "pip install -r requirements.txt" the file is located inside this folder.

then run "python manage.py makemigrations" && "python manage.py migrate" after creating the postgresql db to make sure the db is created successfully and django can use it.

Now run "python manage.py runserver" and it should run on your end.

The answers to the questions have been listed on the homepage of the site "127.0.0.1:8000" assuming you don't change the port

##What about Docker you say?
Yes, yes, I did try to setup a docker image but so far haven't got it work (on docker) I've never used this so I've gone from tutorial to production and given time I'd get it to work, currently it's crashing at installing pandas with a dependency issue which I assume has to do with permissions when not using a virtualenv in docker. 

I think it worked before (creating a docker instance) but crashed at running the server when I realised the script didn't setup postgresdb and I'm sure currently even without running a migration it would crash/hiccup. I'm sure I can get it to work but I'd rather not edge towards the deadline for this.

##How long did it take you to make this bad boy of a project?
This bad boy took me about 3 or 4 days of time to develop, and I plan to use it again to figure out if you can automate full deployment of a django site to digitalocean.