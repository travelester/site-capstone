# Project Plan

Pod Members: **Shayan Sarnevesht, Elias Arghand, William Huang**

## Problem Statement and Description

Insert the latest summary of your problem statement and app description.

In a world where Uber and Lyft makes automobile rides uncomfortable with random strangers taking you in their car, we want to make it easier for like-minded or similarly-situated people to carpool together in their activities and form new friendships

## User Roles and Personas

#### User roles:
"College student": a university student that likes to go on trips to the beach, to national parks hiking, or other excursions with fellow college student

"Driver": A car enthusiast who likes driving and socializing and enjoys going on recreational excursions and doesn’t mind meeting new people to go with.
#### User Personas 
-Greg is an incoming freshman at XYZ college. He recently moved to XYZ college from ABC town and does not have a form of transportation. Grey knows he will need transportation to travel to and from school. Rather than using Uber/Lyft with random strangers to go from place to place he wants to make friends with people at XYZ college so he can carpool with them from time to time. He wishes there was an easier way to find people who go to XYZ college that are in his area.

-Doug is an adventurous person and loves sharing his experience. Since his friends all hate trips, Doug wants to meet new people and take them along for a journey. He wishes there was an easier way to find people who enjoy trips to the beach, to other cities, etc and that are in his area.

-Maria is a student at UCSD that just finished her fall quarter finals. She wants to go back to her family over winter break in Los Angeles. She figures that taking an Uber or Lyft would be too expensive and dangerous for her. She needs to find a way to carpool with other students that are going back to LA over break as well.

-Billy is a student at UCLA that is going to visit family over spring break. His family lives in San Francisco and he knows that the drive will be long and cost a good amount of gas money. He figures that carpooling with other people that can pitch in gas money and provide him company would allow for a better trip.

## User Stories

List the current user stories you will implement.

1. ability to see the email, phone number, and images of riders to know who will be riding with me.
2. ability to update information regarding my trip to let people know that I am going on my trip on a different day or time
3. ability to view all my trips to see all the active events created
4. ability to see own profile and add a description to it and update contact information in case it changes.
5. create a profile with school email to connect with drivers that attend the same school that I do
6. ability to access the application on any device and login to my own account.
7. ability to see peer-given ratings of potential riders to know that they don’t have behavioral issues and that they can be trusted.
8. ability to see all the featured rides on a bulletin board to determine which ride I want to take.
9. see the information of the driver, including a picture of them and their contact information before I ride with them.
10. ability to create a post to share current location and destination and how many people one can bring.

## Pages/Screens

List all the pages and screens in the app. Include wireframes for at least 3 of them.

- Wireframe: https://www.figma.com/file/x2bmeXmXuJJHeOPMazRvjy/Travelster?node-id=0%3A1

- Wireframe Prototype: https://www.figma.com/proto/x2bmeXmXuJJHeOPMazRvjy/Travelster?node-id=0%3A1&scaling=min-zoom&page-id=0%3A1

## Data Model

Describe your app's data model using diagrams or tables

### Users Table
Holds user data

| name | type | other constraints |
| ---- | --------- | ----------- |
| id | primary key | serial |
| name | text | not null |
| email | text | not null, must have '@' after first position |
| password | text | not null |
| imgurl | text | not null |
| created_at | timestamp | not null, defaulted to now |

### Groups Table
Holds groups data (same thing as a "trip" or "event")

| name | type | other constraints |
| ---- | --------- | ----------- |
| id | primary key | serial |
| trip_id | integer | not null |
| created_at | timestamp | not null, defaulted to now |

### Groups-Users Joiner Table
Serves as table to make the many-to-many relationship between users and groups work.
Allows a group to have multiple users, and user to be in multiple groups.

| name | type | other constraints |
| ---- | --------- | ----------- |
| id | primary key | serial |
| group_id | integer | foreign key: references groups.id |
| user_id | integer | foreign key: references users.id |
| is_driver | boolean |  |
| created_at | timestamp | not null, defaulted to now |


## Endpoints

List the API endpoints you will need to implement.

| CRUD | HTTP Verb | Description | User Stories |
| ---- | --------- | ----------- | ------------ |
| Create | POST | User signs up and id is created. Details are stored | 1 |
| Create | POST | User logs in and receives authentication token | 4 |
| Read | GET | User gets all events on the bulletin board. Page also displays current logged in user’s icon | 3 |
| Read | GET | User gets more details about the event clicked on in the bulletin board. | 2 |
| Create | POST | Create an event on the bulletin. POSTS the current user id, date, From, Destination, number of riders, time | 6 |
| Read | GET | User profile page gets the current user clicked on. Gets the name, school, about me, ratings (stretch). | 5,8 |
| Read | GET | Gets all trips for a specific user (trip contains information with time between two points and source/destination) | 7 |
| Update | GET | Allow driver to update information regarding their trip. Requires current user id, date, From, Destination, number of riders, time. | 9 |
| Update | PUT | Allow the user to update information regarding their account, including description, contact information, and social medias. | 5 |


***Don't forget to set up your Issues, Milestones, and Project Board!***
