[<- Return To Home...](./)

# Event Recommendation Using Data Mining

### [](#header-3)Introduction

Event Recommendation system is a system to predict interest of a user in nearby events. There are a lot of events happening all over the world in various fields. Some users might be interested in events based on their preferences or as suggested by their friends. In this project, I have to predict what events users will be interested, based on events they’ve responded to in the past, user demographic information, and what events they have seen and clicked on. This project is based on a competition posted on kaggle.com.

### [](#header-3)Dataset

Data for this project is taken from kaggle.com. There are six files in all: train.csv, test.csv, users.csv, user_friends.csv, events.csv, and event_attendees.csv.

**### [](#header-4)Event.csv** This file contains all the information about every event present in the system. It has approx. 2 mil rows and 110 columns. Columns are as follows :

* Event-id, unique id of event
* User-id, user who has created the event
* Start time, start time of event
* City, state, country and zip, are location of event(if known)
* Lat and lng, are latitude and longitude of the location of event
* Next 101 columns are for the 100 most common words throughout the application and count of each of 100 words in this event.

**### [](#header-4)Users.csv** This file contains all the information about all users in the system. It has about 30000 rows and 7 columns. Columns are as follows :

* user_id, unique id of each user
* locale, string representing users locale
* birthyear, birth year of user
* gender, gender of user
* joinedAt, when user has joined the system
* location, user’s location
* timezone, user’s time-zone

**### [](#header-4)user_friends.csv** This file has just two columns user and friend. Friend is a list of friends of user which is space separated.

**### [](#header-4)event_attendees.csv** This file has information about which user attended which events. Columns are as follows :

* event_id, identifies the event
* yes, space separated list of user who indicated that they are going to event
* maybe, space separated list of user who indicated maybe
* invited, space separated list of user who indicated that they were invited
* no, space separated list of user who indicated that they are not going to event

**### [](#header-4)train.csv** This file is used for training the model. It has six columns :

* user, id of user
* event, id of event
* invited, is a binary variable, whether the user is invited to event (1) or not (0)
* timestamp, when user saw the event
* interested, is a binary variable, if user is interested in event (1)
* not_interested, is a binary variable, if user is not interested in event (1)

**### [](#header-4)test.csv** This file is used to test the data. Same as train.csv but is used to predict interested or not.


