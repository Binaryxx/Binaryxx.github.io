---
layout: page  
title: "Professional Projects"  
permalink: /professional-projects  
---

Below are projects which relate to VBA, Python, SQL, and Tableau. I categorize these as prossional projects since they use commonly used technical skills in analytics. In addition, I believe that they also teach universal and transferrable skills, such as the ability to learn in an unguided and independent setting and the ability to leverage available resources to complete a task.  

<hr>

### VBA  
To use and inspect the macros, please download the worksheet.
<iframe src="https://1drv.ms/x/c/4e1a09861c3af1e4/EW8QJ42WORBAmiXwcDzBI0oBqdNMvfg88MM50R9ZUB4dKg?e=JrQeIz" title="Excel Worksheet">
</iframe><br><br>

**Question Auto Fill Macro**  
Populated and formatted a sheet with a character’s info and stats based on the inputted parameters in the user form.  
<video width="320" height="240" controls>
  <source src="professional-projects-assets/auto-fill-demo.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video><br><br>

**Character Creation User Form**  
Automatically answered common questions, such as name and current date, regardless of its location in the selection.  

<video width="320" height="240" controls>
  <source src="professional-projects-assets/character-creation-demo.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video><br><br>

<hr>

### Python  
**Street Fighter 6 Rank Distribution Explorer**  
* Visualized the distribution of 750k players’ ranks based on web scraped data to provide an accurate benchmark
* Leveraged multiprocessing for an 80% runtime reduction to allow for the implementation of a player inactivity check

<embed src="professional-projects-assets/sf6-slides.pdff" type="application/pdf"><br><br>

**Valorant Meta Analysis Series**  
* Built an interactive dashboard to reveal the most popular and successful characters based on the map and skill level
* Evaluated whether performance statistics from past matches, such as accuracy, can be used to predict a player’s rank
* Gathered, stored, and wrangled data requested from a REST API to overcome the limited match data provided

<embed src="professional-projects-assets/valorant-slides.pdf" type="application/pdf"><br><br>

**Winning the Space Race through Data Science**  
* Employed classification algorithms, such as KNN and SVM, to predict if rocket engines will be successfully retrieved and reused after their launch, determining the company’s ability to offer competitive contracts through cost savings
* Performed all the tasks found in a data science project’s life cycle, from data collection to communication of findings

<embed src="professional-projects-assets/capstone-project.pdf" type="application/pdf"><br><br>

<hr>

### SQL  
**Title**  
Descrition
<pre>
  <code>
SELECT  
    CASE   
    WHEN g.grade > 7 THEN s.name   
        ELSE NULL   
    END AS student_identifier,   
    CASE   
        WHEN s.marks BETWEEN g.min_mark and g.max_mark THEN g.grade   
    END AS student_grade,   
    s.marks   
FROM students AS s   
INNER JOIN grades AS g   
ON s.marks BETWEEN g.min_mark AND g.max_mark   
ORDER BY student_grade DESC,   
    CASE   
        WHEN student_identifier IS NULL THEN s.marks   
        ELSE s.name   
    END   
; 
  </code>
</pre>

<hr>

### Tableau  
**Title**  
Descrition
<embed src="file.pdf" type="application/pdf"><br><br>
  
**Title**  
Descrition
<embed src="file.pdf" type="application/pdf"><br><br>
