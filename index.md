# Smart Mirror
The smart mirror is a mirror where you can not only look at yourself but have it display different information on the screen such as the date, time, weather, to-do lists, or even have it play music! A monitor, which is run by Raspberry Pi sits behind the mirror and enables information to be displayed onto the screen. I used React to program and customize information on the mirror. 

| **Engineer** | **School** | **Area of Interest** | **Grade** |
|:--:|:--:|:--:|:--:|
| Shragvi S. | Evergreen Valley Highschool | Computer Science | Incoming Sophomore

<img width="1300" alt="Screen Shot 2021-07-23 at 3 26 27 PM" src="https://user-images.githubusercontent.com/86075172/126847158-5e872f55-d849-4bef-9ed7-665411324b3e.png">


# Demo Night Presentation

[![Demo Video](https://res.cloudinary.com/marcomontalbano/image/upload/v1627078559/video_to_markdown/images/youtube--JUzOucNVUH4-c05b58ac6eb4c4700831b2b3070cd403.jpg)](https://www.youtube.com/watch?v=JUzOucNVUH4&ab_channel=BlueStampEng "Demo Video")

**Reflections:** Overall, my time at Bluestamp has shown me that I really enjoy the software side of engineering and the designing aspect as well and has really given me the confidence to pursue it in the future. I also learned that as long as you are determined and willing to stick to something, you can make it happen.


  

# Final Milestone
My third milestone was just to glue the mirror screen to the monitor and to get my mirror display to load onto the monitor. To do this, I first simply hot glued my mirror screen to the monitor. Then, I used a couple of git commands such as ‘git pull’ and ‘git push’ to push my code to my github repository and then pull it onto my Raspberry Pi. I also changed the port numbers from 3000 to 8080 and after using ‘npm run build’ and ‘npm install’ I was able to load all my code and display it on the monitor.

<img width="500" alt="Screen Shot 2021-07-23 at 2 55 56 PM" src="https://user-images.githubusercontent.com/86075172/126845515-0d6aad48-87af-4bdb-9bc7-55ceafb947f2.png">

My mirror displayed on my monitor.



# Second Milestone
My second milestone was to code the features and modifications that I wanted to add onto the Smart Mirror. The features I added are the time, date, weather, to-do list, motivational quotes, and music. To do this, I used React and since this was my first encounter with React, I had a lot to learn. But after getting the hang of it, it wasn’t so bad. The first component that I worked on was the time and date. For this I used the javascript date object to be able to display the current time, month, day, and year. The second component I worked on was the todo list component. For this component, I used a google calendar api so my mirror would display my tasks and events from my google calendar and update accordingly. The next component was the Weather component. Similarly to the todo list, I used openWeather map to generate an api and display the current weather according to my location. For my quotes component which displays different motivational quotes every hour, I used zenquotes API to generate the different quotes. My last and most complicated component was the spotify component. For this I followed part of a video tutorial and used a spotify API to essentially display whatever song I am playing from my spotify account onto the mirror.

[![Milestone 2](https://res.cloudinary.com/marcomontalbano/image/upload/v1627078604/video_to_markdown/images/youtube--hCnLPmuhs88-c05b58ac6eb4c4700831b2b3070cd403.jpg)](https://www.youtube.com/watch?v=hCnLPmuhs88&ab_channel=BlueStampEng "Milestone 2")


<br>
**Sketch with Modifications:**

<img width="333" alt="Screen Shot 2021-07-20 at 9 41 06 AM" src="https://user-images.githubusercontent.com/86075172/126363091-9d4c29ba-d785-402d-b12b-961159c416d5.png">


**Time and Date component:**

<img width="265" alt="Screen Shot 2021-07-16 at 10 01 37 AM" src="https://user-images.githubusercontent.com/86075172/125988120-6c600fe3-46fd-4871-8e2d-11bf8ac1b452.png">
```javascript
const interval = setInterval( ()=>setCurrentTime(new Date()),1000); 
```
I set the time and date to update every second using an interval function so it would be current.

**To-do List component:**

<img width="261" alt="Screen Shot 2021-07-16 at 10 01 51 AM" src="https://user-images.githubusercontent.com/86075172/125989061-d3151aec-78fc-42df-bbd2-ac801d8ad63e.png">
<img width="700" alt="Screen Shot 2021-07-16 at 10 03 23 AM" src="https://user-images.githubusercontent.com/86075172/125989072-2c3bcbba-7f33-4afc-bb7d-d93bc603307e.png">

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
<img width="852" alt="Screen Shot 2021-07-16 at 11 32 22 AM" src="https://user-images.githubusercontent.com/86075172/125993316-7624c77a-32ed-4e4a-8368-07f245ee7909.png">

The song playing on Spotify displayed onto my mirror.




# First Milestone
My first milestone was setting up the Raspberry Pi and getting the base project working. To set up the Raspberry Pi, I had to download the Raspbian Software and work with and connect different components like a mouse, keyboard, and SD card to the monitor. I also set up SSH and VNC in order to be able to view everything on my computer screen. After setting up the Raspberry Pi, I moved onto installing the Smart Mirror software from a gitHub respository created by my instructor along with installing node.js and npm. Now with the first milestone completed, I can move onto coding and adding modifications.

<img width="400" alt="Screen Shot 2021-07-20 at 9 17 52 AM" src="https://user-images.githubusercontent.com/86075172/126359552-1502e893-f934-489f-8890-c76a77f5bccd.png">

The Raspberry Pi all set up.

[![First Milestone]([![Shragvi S Milestone 1](https://res.cloudinary.com/marcomontalbano/image/upload/v1624638749/video_to_markdown/images/youtube--_fVD8Imxluw-c05b58ac6eb4c4700831b2b3070cd403.jpg)](https://www.youtube.com/watch?v=_fVD8Imxluw "Shragvi S Milestone 1")){:target="_blank" rel="noopener"}
