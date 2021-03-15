# CPlayers - A Case Study

## Problem Statement

Test the existing system which searches for a cricket player, get player statistics and add players to favourite list.

## Requirements specifications of Application Under test

- The application needs to fetch cricket players from the following API.
https://www.cricapi.com/

Refer the following URLs to explore more on the cricket player APIs.
- https://www.cricapi.com/how-to-use.aspx
- https://www.cricapi.com/how-to-use/player-stats-api.aspx
- https://www.cricapi.com/how-to-use/player-finder.aspx

	- A frontend where the user can register/login to the application, find cricket player, get player statistics and add player to favourite list.
	- User can add a player to favourite list and should be able view the favourite list.

## Microservices/Modules
- UserService - should be able to manage user accounts.
- UI (User interface) -  should be able to
* Search a player by name
* View player statistics
* Add a player to favourite list
* should be able to see favourite players
* UI should be responsive which can run smoothly on various devices 
- FavouriteService - should be able to store all the favourite players for a user

## Tech Stack
- Spring Boot
- Angular
- CI (Gitlab Runner)
- Docker, Docker Compose

## Flow of Modules

### Building Frontend 
- Building responsive views: 
* Register/Login
* Search for a player
* Player list - populating from external API
* Build a view to show favourite players
- Using Services to populate these data in views
- Stitching these views using Routes and Guards
- Making the UI Responsive
- Writing CI configuration file
- Dockerize the frontend

### Building the UserService
- Creating a server in Spring Boot to facilitate user registration and login using JWT token and MySQL 
- Writing swagger documentation
- Write CI Configuration
- Dockerize the application
- Write docker-compose file to build both frontend and backend application

### Building the Favourite Service 
- Building a server in Spring Boot to facilitate CRUD operation over favourite players stored in MySQL
- Writing Swagger Documentation
- Write CI Configuration 
- Dockerize the application
- Update the docker-compose

## Added functionality to be implemented

Create Profile Page
- Create Edit Profile / Change Password page (Email address cannot be changed)
- Upload profile image while register & displaying the same in toolbar after login

## Test the entire application 

- Unit Testing for UserService and FavoriteService 
- Web application has to be tested using Selenium-Cucumber framework
- Angular front end has to be tested using Protractor
- REST API - UserService and FavoriteService should be tested using REST Assured.





