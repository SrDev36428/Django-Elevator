# Elevator System  #

!(https://github.com/SrDev36428/Django-Elevator)

A elevator system which goes up, down and stops built with Django(Django Rest Framework including Viewsets, Serializers and etc.)

## Architecture ##
 - When a user logs in, the frontend downloads the elevator list set already. In first case, there will be no elevator set in elevator list
 - So, users can set the number of elevators by clicking format button bellow login button. Then this elevator system is initialized.
   While using this system, users can initialize system like this.
 - After that, elevators are displayed in interface.
 - Each elevator is divided into two status: opened or closed
 - Each elevator contains follow things:
   . floor that elevator is located
   . floor to go up or down based on request of user
   . status to mark whether elevator is in maintenance or not
   . status to mark whether elevator is operational or not
   . status to mark whether elevator has to go up or down
   . status to mark whether elevator is running or not
 - Users can change all of these things by clicking Edit button
 - Users can use only elevator that is operational and not in maintenance, not in running and set clear destination

### Database ###
For this system, I have used postgreSQL.
In using this, you has to consider about version of postgreSQL and django. I used django 5.0 and postgreSQL 16.1

## Assumptions ##

Because of time constraints this project lacks of:

- User Sign-Up / Forgot Password
- Good Test Coverage
- Better Comments / Documentation Strings
- Frontend & Backend Tests
- Modern Frontend Framework (like React)
- Proper UX / UI design (looks plain bootstrap)

## Run ##

0. Download and Install latest version of python and get-pip.py in the Internet
   Open and command prompt and install requirements as follow:
   . pip install django==5.0 psycopg2 djangorestframework and etc.

Move to the location to install django project and open command prompt there
1. Create django project
```bash
django-admin startproject elevator_system
```
2. Go into the installed project folder
```bash
cd elevator_system
```
3. Install needed app
```bash
python manage.py startapp elevators
```
4. Init database
```bash
python manage.py migrate
```
5. Run tests
```bash
python manage.py test
```
6. Create admin user
```bash
pythoin manage.py createsuperuser
```
7. Run development server
```bash
python manage.py runserver
