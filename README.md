# Dashboard - Youtube Trending 2017 & 2018 USA
<img width="797" height="379" alt="Dashboard gif" src="https://github.com/user-attachments/assets/676c349c-6ce6-47f4-8b26-515b745640af" />


## Introduction
In this project I created a dashboard that makes able to look among the top different stats of a Youtube video during trending as:
- **_Views_**
- **_Tags_**
- _**Category**_

The data which I worked with was got from [Kaggle](https://www.kaggle.com/) where the property grab just the data during the period where the video stay on trending in the region of USA.

## Dashboard File:
[Project #1 - Youtube Trending 2017 & 2017 USA](./Project%20%231%20-%20Youtube%20Trending%202017%20%26%202017%20USA.xlsx)

## What questions did I answered?
For be able to have an objective to follow in this project, I asked myself the next questions:  

**1. _What's the difference between the first and last day in their period of Youtube Trending?_**

**2. _Which year was better 2017 or 2018 on Youtube Trending?_**
     
**3. _What tags were the most used by creators on Youtube Trending?_**
     
**4. _What categories were the most dominant of Youtube Trending?_**

## What skills did I used for get these questions answered?
For make this questions answered I used a combination of powerful skills as:

- **_Powerquery (ETL)_**
- **_Power Pivot & Dax (Data Analysis Expressions)_**
- **_PivotTable_**
- _**PivotChart**_
- **_Formulas & Functions_**

## How did I use these skills?

**1. Power Query**
  - **Extract & Transform**  
    First I've loaded the original dataset, convert the trending date to an appropiate formated date by extracting every single value and put them all as one and removed those rows where the data wasn't caught
    correctly. After all of this I proceed to create differents querys where:
    - Loaded a query from website with different categories names of Youtube by ID and then I merge it with the original dataset.
  
      <img width="1920" height="868" alt="image" src="https://github.com/user-attachments/assets/1c4daef9-f23c-40b9-873a-511931d00969" />
  
    - Created a special query for separate and count every single tag without repeating for the same video on the same date

      <img width="1738" height="888" alt="image" src="https://github.com/user-attachments/assets/97761ef8-214c-4bc5-8b5e-814eb9938635" />

    - Created a special query for separate and count every single category that appeared on the original dataset without repeating for the same video

      <img width="1735" height="870" alt="image" src="https://github.com/user-attachments/assets/dbcaff2e-41f5-402c-9499-ce4b32cb1d3e" />
- **Load**  
  In the end I just loaded all my queries to only connection and make'em ready by adding the data to Data Model for work with Power Pivot
  
  <img width="337" height="305" alt="image" src="https://github.com/user-attachments/assets/60b48a3d-f90c-4c3a-bd22-cb26e820da05" />

**2. Power Pivot**  
  - **Model Table**  
    Created a relational table allowing me to have a full control on them by connecting them by index, a column that I created before on Power Query
    
    <img width="1148" height="571" alt="image" src="https://github.com/user-attachments/assets/28ab6056-b80c-4444-9a06-eef8bd77379a" />

  - **DAX (Data Analysis Expressions)**  
    Created different measures for get the values that I'm looking for
    
    <img width="367" height="75" alt="image" src="https://github.com/user-attachments/assets/8ecefff5-776a-4f2f-a982-5a32276a63f8" />

**3. Pivot Table**  
  Created different PivotTables from Power Pivot for get a certain amount of videos and see their values using explicit measures (DAX) and implicit measures.  
  - **Views Table**  
  
    <img width="556" height="223" alt="image" src="https://github.com/user-attachments/assets/a864e9e0-89b4-4670-8ead-913693b7ec31" />

    - **Analysis**  
      We can see how some videos started with a startup before they glow up meanwhile other video could started near to 0 but ended being close to those that had a startup.
    

  - **Count of Tags Table** 

    <img width="137" height="241" alt="image" src="https://github.com/user-attachments/assets/213c2807-c290-47ef-9710-e8eacdb5cc62" />

    - **Analysis**  
    We could conclude that content creators prefer to create content oriented to make people laugh as we see the amount that entertaiment category appeared.

  - **Count of Categories Table**  

    <img width="320" height="264" alt="image" src="https://github.com/user-attachments/assets/ff7cf816-3142-46b8-b1e9-676b36aff113" />

    - **Analysis**  
    As I said before, people tends to create videos to entertain and make people laugh.

  **4. Pivot Chart**  
  To have a clearly visualization of my tables, I created different charts where I can see the relation on their increase and amount between the years

  - **Videos**  
  
  <img width="812" height="396" alt="image" src="https://github.com/user-attachments/assets/9ac175da-9c67-4f0a-9b87-cb6a613e6d4c" />

  - **Categories**
  
  <img width="693" height="396" alt="image" src="https://github.com/user-attachments/assets/bfc3d246-ef5a-404b-b0c3-63f779363cbd" />


  - **Tags**  
  
  <img width="691" height="353" alt="image" src="https://github.com/user-attachments/assets/21e11dcc-8f30-4b0b-8553-162171404b76" />

  **So what?**  
  We can say with accuracy that 2018 was better than their previous year and even though music isn't the highest when it's about tag and category, music is the one that tends to goes to most viral considering the high competition this industry brings

  **5. Formula & Functions**  
  I used different formulas and function to get the values that I'm looking for as:
  
  1. **MAX & MIN**  
     Used these functions on my measures to brings only one title to my table because it has repetitive as the data caught was through a period of time.  
    <img width="193" height="22" alt="image" src="https://github.com/user-attachments/assets/f35b34eb-24c5-42f8-ae6b-339b3c8a44e6" />  
    <img width="193" height="24" alt="image" src="https://github.com/user-attachments/assets/c6a664f2-a951-417d-a0de-a9d601a925b3" />


  2. **VLOOKUP**  
     Used this function to brings always the values from the highest row in the table for my KPIs without considering their sorting and this special case I used V as it has the lookup value on the furthest left.
     
     <img width="1427" height="132" alt="image" src="https://github.com/user-attachments/assets/2416182a-f8b8-421a-9265-c1b43d22b946" />

  3. **Math Equation**  
     I got the amount of views earned on a single title for my KPIs by substracting their highest view obtained with their lowest view obtained.

     <img width="312" height="41" alt="image" src="https://github.com/user-attachments/assets/ce9d8964-350d-43de-b59c-10d249b5088c" />

  4. **Statistic Equation**  
     I got the increase rate of views on a single title for my KPIs by substracting their highest view obtained with their lowest view obtained and then dividing this result by their lowest view obtained.

     <img width="159" height="41" alt="image" src="https://github.com/user-attachments/assets/70960423-30d0-467e-ab5d-c50e4b3cba09" />
     *Instead of multiplying the result by 100 for get te percentage, I used % format as it does the job for me.*

## **KPIs (Key Performance Indicators)**
For have a more detailed about the stats I created some KPIs referencing the result of my formulas and functions used before.

<img width="831" height="349" alt="image" src="https://github.com/user-attachments/assets/2f2150d3-8aaa-4ebf-a29d-f29ba4fcaad5" />

## Conclusion
On my first project on excel with two weeks of learning Excel, I realized the importance of have a good management and mindfulness of the tools to use as well as be awared about the questions that you need to respond. 
Sometimes is better to do the simply solution than the hardest and lose a lot of time trying to get there.

Anyways, I hope that the information showed here could help to see the evolution of how viral could went a video with just one year of difference.
  

     
     
  


  

  
   
    

