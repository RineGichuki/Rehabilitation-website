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
        <h1>Free Courses</h1>
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
        <h1>Course Details</h1>
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

