# Work at Ukkobox

Ukkobox is a company that offers secure and private data storage using multiple clouds.

The Ukkobox development team consists of developers who love what they do. Our
agile development processes and our search for the best development practices
provide the perfect environment for professionals who like to create quality
software.

We are always looking for good programmers who love to improve their work and
we give preference to small teams with qualified professionals to large teams
with average professionals.

This repository contains a small test used to evaluate if the candidate has the
basic skills to work with us.

You should implement a Java or Python application that exposes an API to store and retrieve
files on the cloud.



## How to participate

1. Make a fork of this repository on Github. If you can't create a public
   fork of this project at Github, make a private repository in 
   [bitbucket.org](https://bitbucket.org) (for free) and add read permission
   for user [@rafox](https://bitbucket.org/rafox) on project.
2. Follow the instructions of `README.md`.
3. Deploy you project on Heroku
4. Apply for the position sending an e-mail to libardi@ukkobox.com with:
  - Link to the fork on Github.
  - Link to the project in Heroku.
  - Brief description of the work environment used to run this project
    (Computer/operating system, text editor/IDE, libraries, etc.).
  - Curriculum Vitae attached to the email (avoid .doc files) or link to Linkedin profile.


## Specification

As we already said, Ukkobox is a company that provides secure and private data storage 
using multiple clouds.

One of our services is to store and retrieve data from multiple clouds with encryption using
data dispersal techniques. a.k.a. Cloud of clouds data storage.

Your applicaton should implement the following stories using HTTP REST APIs:

#1-UPLOAD A FILE
An user might be able to upload a file using the endpoint "/upload" that will:
1-receive a file;
2-replicate the file on two cloud providers (Amazon/DigitalOcean/Google/Dropbox/FTP/others);
3-store the information to retrieve the file on a SQLite database (name, type, provider, date);
4-send a response to the user (STATUS 200 if no error, or 500 if there is an error).

#2-DOWNLOAD A FILE
An user might request to download a file from the stored database using the endpoint "/download" that will:
1-receive the filename;
2-check the SQLite database for the filename;
3-using the SQLite database information from the file, the application should retrieve the file from any of the cloud providers;
4-send the file back to the user or send an error if there is any problem or the file is not found;


## Project Requirements

The project must implement the following features:

- Python or Java.
- Use PEP-8 for code style.
- The data should be stored in a relational database.
- The command to start the applcation should receive no arguments.




> Tip #1:
> Optimize for data read/write performance!

> Tip #2:
> Optimize for big files!

- English documentation of API.
- Variables, code and strings must be all in English.


## Recommendations

- Write tests.
- Avoid exposing database implementation details in the API (eg. do not expose model ID at URLs)
- Practice the [12 Factor-App] (http://12factor.net) concepts.
- Make small and atomic commits, with clear messages (written in English).
- Use good programming practices.
