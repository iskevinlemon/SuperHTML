# SuperHTML
Bind JavaScript to HTML with minimal syntax.
<br/>

# Installation via CDN
**CDN installation is recommended**
```html
<script src="https://cdn.jsdelivr.net/gh/iskevinlemon/SuperHTML/super-html.js"></script>
```

# Setting up
**How to correctly setup SuperHTML** <br/>
View the docs <a href="superhtml.netlify.app/" target="_blank">here</a>
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SuperHTML</title>
    <!-- STEP 1: Include the script in the head tag -->
    <script src="https://cdn.jsdelivr.net/gh/iskevinlemon/SuperHTML/super-html.js"></script>
</head>
<!-- 
    STEP 2: Attach a superHTMLController in the body and provide a name .
    For this demo, the name is "myController"
-->
<body superHTMLController="myController">

    <!-- 
        STEP 6: bind the data by using @{variable} 
        variable is the "text" defined in STEP 5
    -->
    <h1>@{text}</h1>

    <script>
    // STEP 3: create an instance of SuperHTML
    // For this demo, the instance is "s"
    var s = SuperHTML;

    // STEP 4: Define the controller from the .controller()
    // and pass in "myController"
    s.controller("myController");

    // Step 5: Define a dummy data
    var text = "Hello World from SuperHTML";

    // Step 7: Compile the instance
    // ONLY COMPILE at the end of all the JavaScript
    // Else it will not work.
    s.compile();
    </script>

</body>
</html>
```