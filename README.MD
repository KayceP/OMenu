![Part of the Udacity Front-End Web Development Nanodegree](https://img.shields.io/badge/Udacity-Front--End%20Web%20Developer%20Nanodegree-02b3e4.svg)
> Developed for project 3 of 6 as part of the **Udacity Front-End Web Developer Nanodegree**.

# OMenu

A web app made for the [Udacity Full Stack Nanodegree program](https://www.udacity.com/uconnect/intensive/full-stack-web-developer-nanodegree), with Python. 

![screenshot](http://i.imgur.com/qmrrOPj.png)

## Features

 - Full CRUD functionality
 - Google oAuth user verification
 - Python generated HTML interface

## Requirements
**[Python 2.7.13](https://www.python.org/downloads/)** *(Included with Vagrant)*

**[VirtualBox](https://www.virtualbox.org/)**

**[Vagrant](https://www.vagrantup.com/)**

The vagrant file contained within this repository will automatically configure the remaining requirements, which are listed below for reference. 

- SQL Alchemy
- postgresql
- psycopg2
- flask
- flask-login
- oauth2client
- requests
- werkzeug
- httplib2

## Configuration

- Install VirtualBox and Vagrant, using the default installation options.
- Open a command terminal in the folder you extracted this repository in.
- Bring Vagrant online by executing the following commands in a command terminal. 

```
$ vagrant up
$ vagrant ssh
```
- Information on how to configure the system will be automatically imported from the Vagrantfile and pg_config.sh.

- Run database_setup.py:
```
python database_setup.py
```

- Populate the database by running lotsofmenus.py,:
```
python lotsofmenus.py
```

## Running

 - Finally, launch the program by executing project.py:
```
python project.py
```
 - Open your web browser and navigate to:
```
http://localhost:8000/
```
 

 - By default, you will not be able to edit the base resturant menus, as you are not the admin/original user.
 - To test the program and CRUD operations, press 'Add New Restaurant' and make a new entry.
 - Once created, navigate to your new Restaurant on the main menu and you can now create, edit and delete freely.

## API Documentation

All restaurants:

```
http://localhost:8000/restaurant/JSON
```

All menu items for a specific RESTAURANT_ID:

```
http://localhost:8000/restaurant/<RESTAURANT ID>/menu/JSON
```

Single menu item:

```
http://localhost:8000/restaurant/<RESTAURANT ID>/menu/<ITEM ID>/JSON
```
## Credits

Skeleton / base code from multiple Udacity sources:
  - [Original UD330 Repository](https://github.com/udacity/ud330)
  - [Updated UD330 Repository from FSND Connect](https://github.com/NoMan2000/ud330)
  - [Full Stack Foundations (ud088)](https://github.com/udacity/Full-Stack-Foundations)
