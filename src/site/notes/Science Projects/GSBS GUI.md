---
{"dg-publish":true,"permalink":"/science-projects/gsbs-gui/"}
---


## What?

A makeshift tkinter GUI for viewing results of the Greedy State Boundary Search algorithm from

[statesegmentation package](https://github.com/lgeerligs/statesegmentation)

Has horrible implementation, but is convenient. I don't know what I'm doing and have no idea how to build a proper GUI. No elegance here.

![](https://private-user-images.githubusercontent.com/60198204/362094519-74192d8d-0f8e-45fd-94a0-848ba51d13e4.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3NTMxOTkxNjUsIm5iZiI6MTc1MzE5ODg2NSwicGF0aCI6Ii82MDE5ODIwNC8zNjIwOTQ1MTktNzQxOTJkOGQtMGY4ZS00NWZkLTk0YTAtODQ4YmE1MWQxM2U0LnBuZz9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNTA3MjIlMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjUwNzIyVDE1NDEwNVomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPTgxYzAyYmVhOTM2ZmZiYWFjMzIwZDgwOTY5YWM4ODdlM2U3OWI1ODIyYmE2YTFjMDJjMzQ3MzhhYTFiMjIyNjUmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0In0.5ecH9WK1nKqfxvth7o78VDiF8I5EoOOYoYeyOeIA7-Q)

---
## Features

- Can perform GSBS if the path of a 2d numpy array of shape (ntimepoints,nchannels) is entered with the given parameters.
- Can also display results of a saved GSBS object.
- Lets you explore segmentation results from the whole search, plotting boundary locations and average state patterns.
    - More specifically, lets you explore segmentation results not only of the best solution, but all solutions.
    - Shows the time by time correlation matrix, time by channel timeseries data with the boundaries overlaid, and a time by channel state averaged timeseries data woth the boundaries overlaid.
- If you have as many images as there are timepoints in your data with 1-1 correspondance, and the images are named 'n.jpg', can show images before and after each boudnary.

---

More here:
https://github.com/drgzkr/GSBS_GUI