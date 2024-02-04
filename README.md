<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Helping Young People Overcome Drug Abuse Through Upskilling</title>
</head>
<body>
    <h1><h1 style="background-color:rgb(255, 244, 30);">Helping Young People Overcome Drug Abuse Through Upskilling</h1>
</body>
</html>


<html>
   <head>
      <title> </title>
   </head>
   <body>
   </body>
   <!DOCTYPE html>
   <html lang="en">
   <head>
       <meta charset="UTF-8">
       <meta name="viewport" content="width=device-width, initial-scale=1.0">
       <title>Free Courses</title>
       <link rel="stylesheet" href="styles.css">
   </head>
   <body>
       <header>
           <h2><h2 style="background-color:rgb(30, 218, 255);">Free Courses</h2>
       </header>
       <main id="courses-list">
           <!-- Courses will be dynamically added here -->
       </main>
       <script src="script.js"></script>
   </body>
   </html>
   <!DOCTYPE html>
   <html lang="en">
   <head>
       <meta charset="UTF-8">
       <meta name="viewport" content="width=device-width, initial-scale=1.0">
       <title>Course Details</title>
       <link rel="stylesheet" href="styles.css">
   </head>
   <body>
       <header>
        <a href="https://skillsbuild.org/">Take the IBM Skills Build courses</a>
           <h3><h3 style="background-color:rgb(125, 244, 74);">These courses are designed to equip you with the digital skills required to navigate the job market.</h3>
       </header>
       <main id="course-details">
           <!-- Course details will be dynamically added here -->
           
       </main>
       <script src="script.js"></script>
       <script>
           // Function to display course details
           function displayCourseDetails() {
               const urlParams = new URLSearchParams(window.location.search);
               const title = urlParams.get('title');
               const courseDetails = courses.find(course => course.title === decodeURIComponent(title));
               const courseDetailsElement = document.getElementById('course-details');
               const courseElement = document.createElement('div');
               courseElement.classList.add('course');
               courseElement.innerHTML = `
                   <h2>${courseDetails.title}</h2>
                   <p><strong>Instructor:</strong> ${courseDetails.instructor}</p>
                   <p><strong>Duration:</strong> ${courseDetails.duration}</p>
                   <p>Description: Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed vitae egestas risus. Phasellus eleifend, nisl sit amet ullamcorper feugiat, metus diam elementum nunc, id gravida lorem felis non ex.</p>
               `;
               courseDetailsElement.appendChild(courseElement);
           }
   
           // Call the displayCourseDetails function when the page loads
           window.onload = displayCourseDetails;
       </script>
   </body>
   </html>
      
