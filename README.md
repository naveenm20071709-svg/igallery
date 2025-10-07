# Ex.08 Design of Interactive Image Gallery
## Date:07.10.25

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
image.html

<html>
    <head>
        <title>Gallery</title>
        <link rel="stylesheet" href="style.css">  
    </head>
    <body>
        <div class="image" id="image">
            <img src="image1.jpeg" id="image1">
            <img src="image2.jpeg" id="image2">
            <img src="image3.jpeg" id="image3">
            <img src="image4.jpeg" id="image5">
            <img src="image5.jpeg" id="image4">
        </div>
        <h1>&copy;Image GalleryDESIGNED BY:</h1>
        <h2>NAVEEN M(25017603)</h2>
        <script src="script.js"></script>
    </body>
</html>

style.css


const popup = document.getElementById('popup');
const popupImg = document.getElementById('popupImg');
const closeBtn = document.getElementById('close');

document.querySelectorAll('.gallery img').forEach(img => {
  img.addEventListener('click', () => {
    popup.style.display = 'flex';
    popupImg.src = img.src;
  });
});

closeBtn.addEventListener('click', () => {
  popup.style.display = 'none';
});

popup.addEventListener('click', e => {
  if (e.target === popup) popup.style.display = 'none';
});


body {
  background: #eee;
  font-family: Arial, sans-serif;
  margin: 0;
  display: flex;
  flex-direction: column;
  align-items: center;
}

h2 {
  margin: 20px;
}

.gallery {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 15px;
  padding: 20px;
}

.gallery img {
  width: 200px;
  height: 250px;
  object-fit: cover;
  border-radius: 10px;
  cursor: pointer;
  transition: transform 0.2s;
}

.gallery img:hover {
  transform: scale(1.05);
}


.popup {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.8);
  display: none;
  justify-content: center;
  align-items: center;
}

.popup img {
  width: 60%;
  max-width: 400px;
  border-radius: 12px;
  box-shadow: 0 0 20px #000;
}

.popup span {
  position: absolute;
  top: 20px;
  right: 40px;
  font-size: 30px;
  color: white;
  cursor: pointer;
  font-weight: bold;
}

script.js

const popup = document.getElementById('popup');
const popupImg = document.getElementById('popupImg');
const closeBtn = document.getElementById('close');

document.querySelectorAll('.gallery img').forEach(img => {
  img.addEventListener('click', () => {
    popup.style.display = 'flex';
    popupImg.src = img.src;
  });
});

closeBtn.addEventListener('click', () => {
  popup.style.display = 'none';
});

popup.addEventListener('click', e => {
  if (e.target === popup) popup.style.display = 'none';
});



```
## OUTPUT:
![alt text](<Screenshot 2025-10-07 234457.png>)

![alt text](<Screenshot 2025-10-07 234526.png>)



## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
