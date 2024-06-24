---
layout: page  
title: "Professional Projects"  
permalink: /professional-projects  
---

Below are projects which relate to VBA, Python, SQL, and Tableau. I categorize these as prossional projects since they use commonly used technical skills in analytics. In addition, I believe that they also teach universal and transferrable skills, such as the ability to learn in an unguided and independent setting and the ability to leverage available resources to complete a task.  

<hr>

### VBA  
To use and inspect the macros, please download the worksheet.
<iframe src="https://onedrive.live.com/edit?id=4E1A09861C3AF1E4!s1e7a718df12040f784607a5d43b119f3&resid=4E1A09861C3AF1E4!s1e7a718df12040f784607a5d43b119f3&cid=4e1a09861c3af1e4&ithint=file%2Cxlsx&redeem=aHR0cHM6Ly8xZHJ2Lm1zL3gvYy80ZTFhMDk4NjFjM2FmMWU0L0VZMXhlaDRnOGZkQWhHQjZYVU94R2ZNQnE3ZWJ6ajEzZ3pBV3RVZW1QaXFOR3c_ZT01MkpOZTk&migratedtospo=true&wdo=2" >
</iframe><br><br>

**Question Auto Fill Macro**  
Populated and formatted a sheet with a character’s info and stats based on the inputted parameters in the user form  
<video width="320" height="240" controls>
  <source src="auto-fill-demo.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video><br><br>

**Character Creation User Form**  
Automatically answered common questions, such as name and current date, regardless of its location in the selection  

<video width="320" height="240" controls>
  <source src="character-creation-demo.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video><br><br>

<hr>

### Python  
**Title**  
Descrition
<embed src="file.pdf" type="application/pdf"><br><br>

**Title**  
Descrition
<embed src="file.pdf" type="application/pdf"><br><br>

**Title**  
Descrition
<embed src="file.pdf" type="application/pdf"><br><br>
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
