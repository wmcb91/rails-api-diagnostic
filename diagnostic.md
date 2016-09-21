# Rails API Diagnostic

Place your responses inside the fenced code-blocks where indicated by comments.

What is the purpose of a backend?

```md
A backend is where the critical data and the functions to retrieve that data
live.  Without a backend, nothing could be stored or accessed and the limitations
on your app would be enormous.
```

Which layer in the MVC pattern is used by the controller to fetch data?

```md
The model
```

Which layer in the MVC pattern communicates with the model?

```md
The controller
```

Why don't we use views in our interpretation of the MVC pattern?

```md
We don't use views because we are building SPAs and won't need them.
```

What does C.R.U.D stand for?

```md
Create, Read, Update, Delete
```

In which part of the MVC pattern can we find C.R.U.D actions?

```md
The communication between the between the client and the server uses CRUD. So
does the communication between the web server and the controller (maybe not), and between the
controller and the model, and between the model and the db.
```

List at least 5 standard actions that C.R.U.D corresponds to?

```bash
create, index, show, update and destrot.
```

A user action fires a `GET` request for `/persons/1`. Explain in detail each step
required for data to be returned to the client. (bullet points or ordered list)

```md
- clients sends GET request to url/persons/1 (server)
- Server tells the persons controller it is looking for /persons#show
- Controller tells the model is needs data on persons/1
- Model uses SELECT on database to find info
- Database gives model info
- Model passes info to controller
- controller passes info to server
- server says cool we found it and sends it to client or sorry we couldn't find it
and send error to client.
```

What is the command to generate a new rails-api app?

```bash
// rails-api new app_name
```

What is the command to start an instance of a rails server?

```bash
// bundle exec rails serve(r)
or
// bundle exec rails s
```

What are the commands to drop, create and migrate a database? (3 bullet points)
(in SQL or in bash?)

```bash
// DROP DATABASE
// CREATE DATABASE
// $ bin/rails generate migration name
```

What is the command to scaffold a pet with a name and age attributes (hint:
Also think of the data types for each attribute)?

```bash
// bundle exec rails-api g scaffold pet name:string age:integer
```
