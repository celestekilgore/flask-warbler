# Warbler

Warbler is a Twitter/X clone that allows users to follow/unfollow other users, like/unlike user's warbles, and view a feed of warbles.

## Live Demo

Here is a [demo](https://warbling-warbler.onrender.com/) of Warbler. 
Feel free to use 'tuckerdiane" and 'password' to log in, or create your own account! 
This is hosted using a free service so please give the server a few minutes to warm up. 

## Technologies

* Flask
* Python
* PostgreSQL
* SQLAlchemy
* Jinja
* WTForms

## Features
Here is an overview of some of the key features

- Users can create an account, log in, and log out. 
- Users can send messages, like and unlike other user's messages, and delete messages. 
- Users can follow and unfollow other users, view their followers, and view who they're following. 
- Users can view a feed, showing the messages from the users they are following.
- Users can update their profile information (profile picture, background image, bio, location, etc).
- Implemented user authorization and authentication using g object, form validation, and CSRF protection. 
- Sessions are used to persist the current user. 

## Local setup instructions
1.) Fork and clone this repository

2.) Once in your local version of this folder, run the following:
```
python3 -m venv venv
source venv/bin/activate
pip3 install -r requirements.txt
```
3.) Set up the database:
```
psql
CREATE DATABASE warbler;
(ctrl+D)
python3 seed.py
```
4.) Setup environment variables in .env
- create a .env file at the root of the project
- copy and paste the following code into your new .env file
  ```
  SECRET_KEY=secret
  DATABASE_URL=postgresql:///warbler
  ```
5.) Run the server:
```
flask run -p 5001
```
Warbler will now be viewable on localhost:5001
