# Ex.07 Design of Interactive Image Gallery
## Date:12/11/2024

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
index.html

<!DOCTYPE html>
<html lang="en">
<head>
    <h1>Virat Kholi's Batting Style</h1>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Photo Gallery Grid</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>

<div class="gallery">
  <img src="img 1.jpg" alt="Photo 1" onclick="openLightbox(this)">
  <img src="img 2.jpg" alt="Photo 2" onclick="openLightbox(this)">
  <img src="img 3.jpg" alt="Photo 3" onclick="openLightbox(this)">
  <img src="img 4.jpg" alt="Photo 4" onclick="openLightbox(this)">
  <img src="img 5.jpg" alt="Photo 5" onclick="openLightbox(this)">
  <img src="img 6.jpg" alt="Photo 6" onclick="openLightbox(this)">
  
</div>

<div id="lightbox" class="lightbox">
  <span onclick="closeLightbox()" class="close">&times;</span>
  <img id="lightboxImage" class="lightbox-content">
</div>

<script src="script.js"></script>
</body>
</html>
```
```
styles.css

body {
    font-family: Arial, sans-serif;
    background-color: #e43737; /* Match the background color in the screenshot */
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
    margin: 0;
  }
  
  .gallery {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 20px;
    padding: 20px;
  }
  
  .gallery img {
    width: 200px;
    height: 300px;
    object-fit: cover;
    cursor: pointer;
    border: 5px solid black; /* Creates the border effect */
    transition: transform 0.2s;
  }
  
  .gallery img:hover {
    transform: scale(1.05);
  }
  
  .lightbox {
    display: none;
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: rgba(0, 0, 0, 0.8);
    justify-content: center;
    align-items: center;
  }
  
  .lightbox-content {
    max-width: 80%;
    max-height: 80%;
  }
  
  .close {
    position: absolute;
    top: 20px;
    right: 30px;
    font-size: 35px;
    color: rgb(241, 207, 207);
    cursor: pointer;
  }
  
```
```
script.js

function openLightbox(image) {
    const lightbox = document.getElementById('lightbox');
    const lightboxImage = document.getElementById('lightboxImage');
    lightboxImage.src = image.src;
    lightbox.style.display = 'flex';
  }
  
  function closeLightbox() {
    document.getElementById('lightbox').style.display = 'none';
  }
  
```
## OUTPUT:
![alt text](<Screenshot 2024-11-12 222302.png>)

## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
