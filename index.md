# Smart Mirror
The smart mirror is a mirror where you can not only look at yourself but have it display different information on the screen such as the date, time, weather, to-do lists, or even have it play music! A monitor, which is run by Raspberry Pi sits behind the mirror and enables information to be displayed onto the screen. I used React to program and customize information on the mirror. 

| **Engineer** | **School** | **Area of Interest** | **Grade** |
|:--:|:--:|:--:|:--:|
| Shragvi S. | Evergreen Valley Highschool | Computer Science | Incoming Sophomore

![Headstone Image]()
  
# Final Milestone
My final milestone is the increased reliability and accuracy of my robot. I ameliorated the sagging and fixed the reliability of the finger. As discussed in my second milestone, the arm sags because of weight. I put in a block of wood at the base to hold up the upper arm; this has reverberating positive effects throughout the arm. I also realized that the forearm was getting disconnected from the elbow servo’s horn because of the weight stress on the joint. Now, I make sure to constantly tighten the screws at that joint. 

[![Final Milestone]("){:target="_blank" rel="noopener"}

# Second Milestone
My second milestone was to code the features and modifications that I wanted to add onto the Smart Mirror. The features I added are the time, date, weather, to-do list, motivational quotes, and music. To do this, I used React and since this was my first encounter with React, I had a lot to learn. But after getting the hang of it, it wasn’t so bad. The first component that I worked on was the time and date. For this I used different javascript objects to be able to display the current time, month, day, and year. The second component I worked on was the todo list component. For this component, I used a google calendar api so my mirror would display my tasks and events from my google calendar and update accordingly. The next component was the Weather component. Similarly to the todo list, I used openWeather to generate an api and display the current weather according to my location. For my quotes component which displays different motivational quotes every hour, I used zenquotes API to generate the different quotes. My last and most complicated component was the spotify component. For this I followed part of a video tutorial and used a Spotify API to essentially display whatever track I was playing from my spotify account onto the mirror.

<br>
**Time and Date component:**

<img width="265" alt="Screen Shot 2021-07-16 at 10 01 37 AM" src="https://user-images.githubusercontent.com/86075172/125988120-6c600fe3-46fd-4871-8e2d-11bf8ac1b452.png">
```javascript
const interval = setInterval( ()=>setCurrentTime(new Date()),1000); 
```
I set the time and date to update every second using an interval function so it would be current.

**To-do List component:**

<img width="261" alt="Screen Shot 2021-07-16 at 10 01 51 AM" src="https://user-images.githubusercontent.com/86075172/125989061-d3151aec-78fc-42df-bbd2-ac801d8ad63e.png">
<img width="1438" alt="Screen Shot 2021-07-16 at 10 03 23 AM" src="https://user-images.githubusercontent.com/86075172/125989072-2c3bcbba-7f33-4afc-bb7d-d93bc603307e.png">

A side-by-side view of my tasks on my google calendar displayed onto the mirror.

```javascript
    const getEvents = async()=>{
        const key = 'API KEY'
        const date = ISODateString()
        console.log(date)
        const data = await axios.get(`https://www.googleapis.com/calendar/v3/calendars/EMAIL/events?orderBy=startTime&singleEvents=true&timeMin=${date}&key=${key}&maxResults=5`
            )
```
The code I used to pull an API key from google calendar. 
<br>

**Music component:**

<img width="265" alt="Screen Shot 2021-07-16 at 11 21 54 AM" src="https://user-images.githubusercontent.com/86075172/125992485-8c95c2f9-4dc1-4ffd-ad3c-f41fd92cccd0.png">
<img width="1130" alt="Screen Shot 2021-07-16 at 11 24 38 AM" src="https://user-images.githubusercontent.com/86075172/125992494-7c1fc0ed-b767-4d3f-aae4-0ac7fc7def5b.png">

The song playing on spotify displayed onto my mirror.



# First Milestone
My first milestone was setting up the Raspberry Pi and getting the base project working. To set up the Raspberry Pi, I had to download the Raspbian Software and work with and connect different components like a mouse, keyboard, and SD card to the monitor. I also set up SSH and VNC in order to be able to view everything on my computer screen. After setting up the Raspberry Pi, I moved onto installing the Smart Mirror software from a gitHub respository created by my instructor along with installing node.js and npm. Now with the first milestone completed, I can move onto coding and adding modifications.

[![First Milestone]([![Shragvi S Milestone 1](https://res.cloudinary.com/marcomontalbano/image/upload/v1624638749/video_to_markdown/images/youtube--_fVD8Imxluw-c05b58ac6eb4c4700831b2b3070cd403.jpg)](https://www.youtube.com/watch?v=_fVD8Imxluw "Shragvi S Milestone 1")){:target="_blank" rel="noopener"}
