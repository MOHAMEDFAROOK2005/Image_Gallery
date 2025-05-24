# Ex.08 Design of Interactive Image Gallery

## AIM
  To design a web application for an inteactive image gallery with minimum five images.

## DESIGN STEPS

## Step 1:

Clone the github repository and create Django admin interface

## Step 2:

Change settings.py file to allow request from all hosts.

## Step 3:

Use CSS for positioning and styling.

## Step 4:

Write JavaScript program for implementing interactivit

## Step 5:

Validate the HTML and CSS code

## Step 6:

Publish the website in the given URL.

## PROGRAM
```
<html>
<head>
    <title>IMAGE GALLERY</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: lightsalmon;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            flex-direction: column;
        }
        .gallery-container {
            max-width: 800px;
            margin: 20px auto;
            overflow: hidden;
            position: relative;
        }
        .gallery-slider {
            display: flex;
            transition: transform 0.5s ease;
        }
        .gallery-item {
            min-width: 100%;
            box-sizing: border-box;
        }
        .gallery-item img {
            width: 100%;
            display: block;
            border-radius: 10px;
        }
        .navigation {
            position: absolute;
            top: 50%;
            width: 100%;
            display: flex;
            justify-content: space-between;
            transform: translateY(-50%);
        }
        .navigation button {
            background-color: rgba(0, 0, 0, 0.5);
            color: white;
            border: none;
            padding: 10px;
            cursor: pointer;
            border-radius: 50%;
            font-size: 18px;
        }
        .navigation button:hover {
            background-color: rgba(0, 0, 0, 0.8);
        }
        h1 {
            text-align: center;
            margin-bottom: 20px;
        }
        footer {
            margin-top: 20px;
            font-size: 16px;
            color: #333;
        }
    </style>
</head>
<body>
    <h1>IMAGE GALLERY</h1>
    <div class="gallery-container">
        <div class="gallery-slider" id="slider">
            <div class="gallery-item">
                <img src="ajith.jpeg" alt="AJITH">
            </div>
            <div class="gallery-item">
                <img src="alluarjun.jpeg" alt="ALLUARJUN">
            </div>
            <div class="gallery-item">
                <img src="dhunush.jpeg" alt="DHUNUSH">
            </div>
            <div class="gallery-item">
                <img src="prabhas.jpeg" alt="PRABHAS">
            </div>
            <div class="gallery-item">
                <img src="rajini.jpeg" alt="RAJINI">
            </div>
            <div class="gallery-item">
                <img src="rocky.jpeg" alt="ROCKY">
            </div>
            <div class="gallery-item">
                <img src="vijay.jpg" alt="VIJAY">
            </div>
        </div>
        <div class="navigation">
            <button id="prev">&#10094;</button>
            <button id="next">&#10095;</button>
        </div>
    </div>

    <footer>
        Naresh kumar r 24900973
    </footer>

    <script>
        var slider = document.getElementById('slider');
        var prev = document.getElementById('prev');
        var next = document.getElementById('next');

        var currentIndex = 0;
        var totalItems = slider.children.length;

        function updateSlider() {
            slider.style.transform = 'translateX(-' + (currentIndex * 100) + '%)';
        }

        prev.onclick = function() {
            if (currentIndex > 0) {
                currentIndex--;
            } else {
                currentIndex = totalItems - 1;
            }
            updateSlider();
        };

        next.onclick = function() {
            if (currentIndex < totalItems - 1) {
                currentIndex++;
            } else {
                currentIndex = 0;
            }
            updateSlider();
        };
    </script>
</body>
</html>
```

## OUTPUT
.![image](https://github.com/user-attachments/assets/94a0dddf-ab2b-49ae-8faf-0fe02d4dcff9)



## RESULT
  The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
