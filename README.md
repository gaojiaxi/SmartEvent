# Introduction
This is a full stack event search and recommendation Engine powered by TicketMaster. 
The high level idea is to recommend events based on logged in user's current geo-location. 
The ticket information are obtained from Ticket Master API.  
This project has already been deployed to Amazon EC2, click [demo link](http://54.202.63.63/Event-Search-Recommendation-Engine/) to visit the demo.

## Reason of building this website
When I need to attend some events, I often search on google and randomly go to one website for ticket purchasing. 
As I observed that existing ticket selling websites do not have a recommendation engine and most of them are ticket listing websites.
There are a few reasons we may need a ticket selling with recommendation engine, as listed below.
1. Personalized recommendation: Different customer may like different events, we may recommend accordingly.
2. Price really matters: There are events that some customer may like but too expensive for them to afford.
3. Distance really matters: There are events that some customer may like but too far to go.
Based on listed reasons, I used my spare time to make this ticket selling website with personalized recommendation system.

## Tech Stack
* JAVA/HTML/CSS/JavaScript
* MYSQL/MongoDB

## Content-based Recommendation Algorithm in Details
In this project, I recommend events based on user liked categories and distance to the user.
To be more specific, user are able to like each events using the dynamic website and we can obtain the events' catogories using TICKET MASTER API.  
After we know the category of the eventes that the user have favorited, 
The events within user liked categories are then sorted by their distance to user and shown to user. 
Detailed algorithms are shown below. <br>
1. Fetch all the events that the user has liked or visited. 
2. Given user liked/visited events, obtain the categories of those events. 
3. Given user liked/visited categories, fetch all the events that belone to those categories. 
4. Remove events that this user has visited. 
5. Sort the recommendation list on ascending order of distance between recommended events's locations and user's location.

## Requirements
* Apache Tomat v9.0
* Eclipse for Java EE
* JAVA 8 or above
* MySQL/MangoDB

## Installation
Clone the GitHub repository and then import Smart-Event.war into your eclipse.

```
git clone https://github.com/gaojiaxi/SmartEvent.git
```
In order to import the WAR file into Eclipse JEE, click on File -> Import. Select Web -> WAR File.
* **WAR** file: Provide the full path of the WAR file on your computer.
* **Web project**: This will be auto-filled based on the WAR file name. You may change it depends on your own settings.
* **Target runtime**: You will need to select “Apache Tomcat 9.0”. The first time you import a WAR
file (or create new “Dynamic Web Project”) you will need to declare the new runtime environment. Do this by clicking on “New” and filling in the form as follows:
	* **Apache Tomat v9.0**, then click “Next”
	* Provide the Tomcat installation directory by giving the full pathname of the directory
containing your unzipped version of Tomcat 9.0.
	* Click “Finished”.
* Click "Finished".

Run the imported project by “right-clicking” on the new project and selecting “Run As -> Run on Server. <br>


## Screenshots
logic/high level structure of this project
![](https://github.com/gaojiaxi/SmartEvent/tree/master/demoPictures/highLevelStructure.jpg)
nearby page
![](https://github.com/gaojiaxi/SmartEvent/tree/master/demoPictures/nearby.jpg)
favorite page
![](https://github.com/gaojiaxi/SmartEvent/tree/master/demoPictures/favorite.jpg)
recommendation page
![](https://github.com/gaojiaxi/SmartEvent/tree/master/demoPictures/recommendation.jpg)


## Todo list
1. The login system
2. The registration system.
3. Booting front page using AugularJS or React.

## Deployment
Deployment Environment: Amazon EC2 <br>
(Please contact me at jiaxig@ece.ubc.ca if any issue happend)

## Change Log
v1.0.0(11/02/2019)<br>
* user can see nearby events based on their geo-location
* user can like/unlike events by clicking the 'Heart' symbol on front page.
* System will recommend events to user based on users liked events and geo-location.

