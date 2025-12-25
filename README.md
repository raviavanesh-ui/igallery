# Ex.08 Design of Interactive Image Gallery
## Date:25.12.2025

## AIM:
To design a web application for an inteactive image gallery with minimum five images.

## DESIGN STEPS:

### Step 1:
Clone the github repository and create Django admin interface.

### Step 2:
Change settings.py file to allow request from all hosts.

### Step 3:
Use CSS for positioning and styling.

### Step 4:
Write JavaScript program for implementing interactivity.

### Step 5:
Validate the HTML and CSS code.

### Step 6:
Publish the website in the given URL.

## PROGRAM :
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interactive Image Gallery</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f5f5f5;
            color: #333;
        }
        header {
            text-align: center;
            background-color: #4A90E2;
            color: white;
            padding: 1rem 0;
        }
        h1 {
            margin: 0;
            font-size: 2em;
        }
        .gallery {
            white-space: nowrap;
            overflow-x: auto;
            padding: 1rem;
            background-color: #ffffff;
        }
        .gallery-item {
            display: inline-block;
            margin-right: 10px;
            cursor: pointer;
            transition: transform 0.3s;
        }
        .gallery-item:hover {
            transform: scale(1.05);
        }
        .gallery-item img {
            height: 200px;
            border-radius: 5px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }
        #modal {
            display: none;
            position: fixed;
            z-index: 1;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0,0,0,0.8);
        }
        #modal .close {
            position: absolute;
            top: 15px;
            right: 35px;
            color: white;
            font-size: 40px;
            font-weight: bold;
            cursor: pointer;
        }
        #modal img {
            display: block;
            margin: 5% auto;
            max-width: 80%;
            max-height: 80%;
            border-radius: 5px;
        }
    </style>
</head>
<body>
    <header>
        <h1>Cricket Players</h1>
    </header>

    <div class="gallery">
        <div class="gallery-item" onclick="openModal(this)">
            <img src="Screenshot 2025-12-23 093719.png" alt="Image 1">
        </div>
        <div class="gallery-item" onclick="openModal(this)">
            <img src="Screenshot 2025-12-23 093916.png" alt="Image 2">
        </div>
        <div class="gallery-item" onclick="openModal(this)">
            <img src="Screenshot 2025-12-23 094017.png" alt="Image 3">
        </div>
        <div class="gallery-item" onclick="openModal(this)">
            <img src="Screenshot 2025-12-23 094102.png" alt="Image 4">
        </div>
        <div class="gallery-item" onclick="openModal(this)">
            <img src="Screenshot 2025-12-23 094140.png" alt="Image 5">
        </div>
    </div>

    <div id="modal">
        <span class="close" onclick="closeModal()">&times;</span>
        <img id="modalImage" alt="Modal Image">
    </div>

    <script>
        function openModal(element) {
            var modal = document.getElementById("modal");
            var modalImg = document.getElementById("modalImage");
            modal.style.display = "block";
            modalImg.src = element.querySelector("img").src;
        }

        function closeModal() {
            document.getElementById("modal").style.display = "none";
        }
    </script>
</body>
</html>
```
## OUTPUT:
<img width="1909" height="377" alt="image" src="https://github.com/user-attachments/assets/5cd890bd-8a29-42de-96f9-ecf0ceed1cac" />

## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
