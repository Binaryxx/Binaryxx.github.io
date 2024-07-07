---
layout: page  
title: "Professional Projects"  
permalink: /professional-projects  
---

Below are projects that relate to VBA, Python, SQL, and Tableau. I categorize these as professional projects since they use commonly used technical skills in analytics. In addition, I believe that they also teach universal and transferrable skills, such as the ability to learn in an unguided and independent setting and the ability to leverage available resources to complete a task.  

*TIP: Fullscreen/download files for easier readability if necessary. Improvements to UX is in progress. Sorry for the inconvenience!*

<hr>

### VBA  
To use and inspect the macros, please download the worksheet.
<iframe width="320" height="240" frameborder="0" scrolling="no" src="https://1drv.ms/x/c/4e1a09861c3af1e4/IQNvECeNljkQQJol8HA8wSNKAZd3te-vzIW1JfrWJ_Ioaqo?wdAllowInteractivity=False&ActiveCell='Form%20Completion%20II'!A1&wdHideGridlines=True&wdHideHeaders=True&wdDownloadButton=True&wdInConfigurator=True&wdInConfigurator=True"></iframe><br><br>

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

<embed src="professional-projects-assets/sf6-slides.pdf" type="application/pdf" width = 640 height = 480><br><br>

**Valorant Meta Analysis Series**  
* Built an interactive dashboard to reveal the most popular and successful characters based on the map and skill level
* Evaluated whether performance statistics from past matches, such as accuracy, can be used to predict a player’s rank
* Gathered, stored, and wrangled data requested from a REST API to overcome the limited match data provided

<embed src="professional-projects-assets/valorant-slides.pdf" type="application/pdf" width = 640 height = 480><br><br>

**IBM Data Science Professional Capstone Project: Winning the Space Race through Data Science**  
* Employed classification algorithms, such as KNN and SVM, to predict if rocket engines will be successfully retrieved and reused after their launch, determining the company’s ability to offer competitive contracts through cost savings
* Performed all the tasks found in a data science project’s life cycle, from data collection to communication of findings

<embed src="professional-projects-assets/capstone-project.pdf" type="application/pdf" width = 640 height = 480><br><br>

<hr>

### SQL  
**HackerRank: The Report**  
Completed the following HackerRank challenge: The Report - write a query to generate a report containing three columns: Name, Grade and Mark.  
[https://www.hackerrank.com/challenges/the-report/problem](https://www.hackerrank.com/challenges/full-score/problem)
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

**HackerRank: Top Competitors**  
Completed the following HackerRank challenge: Top Competitors - query a list of top-scoring hackers.  
[https://www.hackerrank.com/challenges/full-score/problem](https://www.hackerrank.com/challenges/full-score/problem)

<pre>
  <code>
SELECT Hackers.hacker_id, Hackers.name  
FROM (
    SELECT Submissions.hacker_id as hacker_id, COUNT(Submissions.submission_id) as challenge_count
    FROM Submissions
    INNER JOIN Challenges ON Challenges.challenge_id = Submissions.challenge_id
    INNER JOIN Difficulty ON Difficulty.difficulty_level = Challenges.difficulty_level
    WHERE Difficulty.score = Submissions.score
    GROUP BY Submissions.hacker_id
    ) AS Perfect
INNER JOIN Hackers ON Hackers.hacker_id = Perfect.hacker_id
WHERE challenge_count > 1
ORDER BY challenge_count DESC, Hackers.hacker_id ASC
;
  </code>
</pre>

<hr>

### SQL
**Iris Data Set EDA**  
Created a matrix scatterplot to provide an overall overview of the iris data set and any relationship between its features and the species it belongs to. A dashboard is also made for each feature to provide a more detailed summary of the distribution of species per feature. The original scatterplots which compared 2 different features and the resulting species is also included for the most detailed view of the data.  

<div class='tableauPlaceholder' id='viz1720316662163' style='position: relative'><noscript><a href='#'><img alt='Main Dash ' src='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;Mu&#47;MultivariateAnalysisoftheIrisDataSet&#47;MainDash&#47;1_rss.png' style='border: none' /></a></noscript><object class='tableauViz'  style='display:none;'><param name='host_url' value='https%3A%2F%2Fpublic.tableau.com%2F' /> <param name='embed_code_version' value='3' /> <param name='site_root' value='' /><param name='name' value='MultivariateAnalysisoftheIrisDataSet&#47;MainDash' /><param name='tabs' value='no' /><param name='toolbar' value='yes' /><param name='static_image' value='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;Mu&#47;MultivariateAnalysisoftheIrisDataSet&#47;MainDash&#47;1.png' /> <param name='animate_transition' value='yes' /><param name='display_static_image' value='yes' /><param name='display_spinner' value='yes' /><param name='display_overlay' value='yes' /><param name='display_count' value='yes' /><param name='language' value='en-US' /></object></div>                <script type='text/javascript'>                    var divElement = document.getElementById('viz1720316662163');                    var vizElement = divElement.getElementsByTagName('object')[0];                    if ( divElement.offsetWidth > 800 ) { vizElement.style.width='1366px';vizElement.style.height='795px';} else if ( divElement.offsetWidth > 500 ) { vizElement.style.width='1366px';vizElement.style.height='795px';} else { vizElement.style.width='100%';vizElement.style.height='3427px';}                     var scriptElement = document.createElement('script');                    scriptElement.src = 'https://public.tableau.com/javascripts/api/viz_v1.js';                    vizElement.parentNode.insertBefore(scriptElement, vizElement);                </script>













