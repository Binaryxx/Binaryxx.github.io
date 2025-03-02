---
layout: page  
title: "Professional Projects"  
permalink: /professional-projects  
---

Below are projects that demonstrate my abilities with VBA, Python, SQL, and Tableau. I categorize these as professional projects since they utilize commonly used technical skills in analytics. In addition, I believe that they also teach universal and transferrable skills, such as the ability to learn in an unguided and independent setting and the ability to leverage available resources to complete a task.  

View my certifications at <a href='https://www.credly.com/users/binaryxxsune'>https://www.credly.com/users/binaryxxsune</a>
  
*TIP: Fullscreen/download files for easier readability if necessary. Usually found at the bottom of the media*

<hr>

### VBA  
To use and inspect the macros, please download the worksheet.
<iframe allowfullscreen width=800 height=600 frameborder="0" scrolling="no" src="https://1drv.ms/x/c/4e1a09861c3af1e4/IQNvECeNljkQQJol8HA8wSNKAZd3te-vzIW1JfrWJ_Ioaqo?wdAllowInteractivity=False&ActiveCell='Form%20Completion%20II'!A1&wdHideGridlines=True&wdHideHeaders=True&wdDownloadButton=True&wdInConfigurator=True&wdInConfigurator=True">
</iframe><br><br>

**Question Auto Fill Macro**  
* Designed a user form to populate and format a sheet with a character’s info and stats, based on the inputted parameters.  

<video width=800 height=600 controls>
  <source src="professional-projects-assets/auto-fill-demo.mp4" type="video/mp4">
Your browser does not support the video tag.
</video><br><br>

**Character Creation User Form**  
* Create a macro to automatically answer common questions, such as name and current date, regardless of its location in the selection.  

<video width=800 height=600 controls>
  <source src="professional-projects-assets/character-creation-demo.mp4" type="video/mp4">
Your browser does not support the video tag.
</video><br><br>

<hr>

### Python  
**Street Fighter 6 Rank Distribution Explorer**  
* Visualized the distribution of 750k players’ ranks based on web-scraped data to provide an accurate benchmark
* Leveraged multiprocessing for an 80% runtime reduction to allow for the implementation of a player inactivity check

<embed src="professional-projects-assets/sf6-slides.pdf" type="application/pdf" width = 800 height = 600>
<br><br>

**Valorant Meta Analysis Series**  
* Built an interactive dashboard to reveal the most popular and successful characters based on the map and skill level
* Evaluated whether performance statistics from past matches, such as accuracy, can be used to predict a player’s rank
* Gathered, stored, and wrangled data requested from a REST API to overcome the limited match data provided

<embed src="professional-projects-assets/valorant-slides.pdf" type="application/pdf" width = 800 height = 600>
<br><br>

**IBM Data Science Professional Capstone Project: Winning the Space Race through Data Science**  
* Employed classification algorithms, such as KNN and SVM, to predict if rocket engines will be successfully retrieved and reused after their launch, determining the company’s ability to offer competitive contracts through cost savings
* Performed all the tasks found in a data science project’s life cycle, from data collection to communication of findings

<embed src="professional-projects-assets/capstone-project.pdf" type="application/pdf" width = 800 height = 600>
<br><br>

<hr>

### SQL  
**HackerRank: The Report**  
Completed the following HackerRank challenge: "The Report - write a query to generate a report containing three columns: Name, Grade and Mark."  
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
Completed the following HackerRank challenge: "Top Competitors - query a list of top-scoring hackers."  
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

### Tableau
**Iris Data Set EDA**  
* Established a matrix scatterplot to provide an overall overview of the iris data set and any relationship between its features and the species it belongs to.
* Made separate dashboards for each feature to provide a more detailed summary of the distribution of species per feature.
- The original scatterplots, which compared 2 different features and the resulting species, are also included for a detailed view of the data.  
  
*TIP: View on Tableau Public or Fullscreen at the bottom of the visualization for a complete view since the dimensions for the embedded links are set for browsing purposes.*

__*Multivariate Analysis of the Iris Data Set*__
<iframe allowfullscreen width=800 height=600 src ="https://public.tableau.com/views/MultivariateAnalysisoftheIrisDataSet/MainDash?:showAppBanner=false&:showVizHome=no&:embed=true&:origin=viz_share_link&:device=desktop"></iframe><br>  

__*Distribution of Iris Species Based on Petal Length*__
<iframe allowfullscreen width=800 height=600 src="https://public.tableau.com/views/DistributionofIrisSpeciesBasedonPetalLength/PetalLength?:showAppBanner=false&:showVizHome=no&:embed=true&:origin=viz_share_link&:device=desktop">
</iframe><br>  

__*Distribution of Iris Species Based on Sepal Length*__
<iframe allowfullscreen width=800 height=600 src="https://public.tableau.com/views/DistributionofIrisSpeciesBasedonSepalLength/SepalLength?:showAppBanner=false&:showVizHome=no&:embed=true&:origin=viz_share_link&:device=desktop">
</iframe><br>  

__*Distribution of Iris Species Based on Sepal Width*__
<iframe allowfullscreen width=800 height=600 src="https://public.tableau.com/views/DistributionofIrisSpeciesBasedonSepalWidth/SepalWidth?:showAppBanner=false&:showVizHome=no&:embed=true&:origin=viz_share_link&:device=desktop">
</iframe><br>  

__*Distribution of Iris Species Based on Petal Width*__
<iframe allowfullscreen width=800 height=600 src="https://public.tableau.com/views/DistributionofIrisSpeciesBasedonPetalWidth/PetalWidth?:showAppBanner=false&:showVizHome=no&:embed=true&:origin=viz_share_link&:device=desktop">
</iframe><br>  

__*Distribution of Iris Species Based on Different Features*__  
<sub>NOTE: Please ensure that the "Show Sheets" option is selected in the Settings to be able to access the different sheets.</sub>
<iframe allowfullscreen width=800 height=600 src="https://public.tableau.com/views/DistributionofIrisSpeciesBasedonDifferentFeatures/PLvPL?:showAppBanner=false&:showVizHome=no&:embed=true&:origin=viz_share_link&:device=desktop"></iframe>
