## Meet App
This is the client-side view of an "Events-by-city" application, allowing users to create an account and search to access information about local events by city, including addres, date & time & the ability to add them to a google calendar all within the application.

## Screenshots
![A screenshot of the main landing page](./public/graph.png)
![A screenshot of location data](./public/locations.png)

## Key Features
The initial landing page is a Welcome screen that allows new-user registration and login functions

Upon login authentication, the user is moved to the main page, which will auto-populate with 32 events. If the user searches for an event or changes the number of events displayed, the app will automatically update to accomodate the search queries. 

Events contain the following information, obtianed from the Google Calender API and with data provided by Career Foundry. In the event that an internet connection is not available, the app populates from existing mock data, or the information obtained on last login.


## Technologies Used
*react
*aws
*aws serverless
*axios
*nprogress
*parcel
*google Auth


## Links
Live App: https://singular-ganache-fd70cd.netlify.app/

## Notes
N/A



## USER STORIES
***FEATURE 1: FILTER EVENTS BY CITY***

**Scenario 1:** When user hasn’t searched for a city, show upcoming events from all cities.

**Given**

user hasn’t searched for any city

**When**

the user opens the app

**Then**

the user should see a list of all upcoming events

**Scenario 2:** User should see a list of suggestions when they search for a city.

**Given**

the main page is open

**When**

user starts typing in the city textbox

**Then**

the user should see a list of cities (suggestions) that match what they’ve typed

**Scenario 3:** User can select a city from the suggested list.

**Given**

the user was typing “Berlin” in the city textbox

And the list of suggested cities is showing

**When**

the user selects a city (e.g., “Berlin, Germany”) from the list

**Then**

their city should be changed to that city (i.e., “Berlin, Germany”)

And the user should receive a list of upcoming events in that city

***FEATURE 2: SHOW/HIDE AN EVENT’S DETAILS***

**Scenario 1:** An event element is collapsed by default.

**Given**

the user open the app

**When**

the user lands on the main page

**Then**

the event detail pages are collapsed

**Scenario 2:** User can expand an event to see its details.

**Given**

a user is viewing the main page

**When**

the user clicks the button to see more details

**Then**

the event is expanded to show the details

**Scenario 3:** User can collapse an event to hide its details.

**Given**

the user is viewing an expanded event

**When**

the user clicks the close details button

**Then**

the event collapses back to it's initial state

***FEATURE 3: SPECIFY NUMBER OF EVENTS***

**Scenario 1:** When user hasn’t specified a number, 32 is the default number.

**Given**

the user is viewing the main page

**When**

the user hasn't input a specific number or first visits the app

**Then**

the default number of events to display is 32

**Scenario 2:** User can change the number of events they want to see.

**Given**

the user is on the main page

**When**

the user changes the numerical value in the display box

**Then**

the amount of events shown changes

***FEATURE 4: USE THE APP WHEN OFFLINE***

**Scenario 1:** Show cached data when there’s no internet connection.

**Given**

the useris not connected to the internet

**When**

the user opens the app

**Then**

the user see's a list of events that were stored the last time the app had access to the internet

**Scenario 2:** Show error when user changes the settings (city, time range).

**Given**

the user changes a setting

**When**

there is an error or incorrect syntax within the search filed

**Then**

the app shows an error message

***FEATURE 5: DATA VISUALIZATION***

**Scenario 1:** Show a chart with the number of upcoming events in each city.

**Given**

the user selects a city

**When**

the user clicks to see a chart

**Then**

a chart is displaying showing the variety of events in a given city



- **Given** represents the context of the scenario. In what type of situation would this scenario arise?
- **When** represents the user interaction or behavior. What does the user need to do for this scenario to come into play? Ideally, you should narrow this down to one action per scenario.
- **Then** represents the expected outcomes of the scenario. What should happen when the user performs this specific action in this specific content?
