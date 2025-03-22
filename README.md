Interactive Image Gallery using JavaScript

Date: 22.03.2025

NAME : DHAREENE R K

REG NO : 212222040035

AIM

To create an interactive image gallery with smooth transitions, hover effects, and navigation using JavaScript, HTML, and CSS.

ALGORITHM

STEP 1

Build the HTML structure to define the gallery layout.

STEP 2

Style the gallery using CSS for a visually appealing and responsive design.

STEP 3

Plan the interactivity, including Next and Previous buttons for navigation.

STEP 4

Use JavaScript to add functionality for sliding transitions and hover effects.

STEP 5

Add event listeners to the navigation buttons for smooth scrolling.

STEP 6

Test the application for proper functionality and responsiveness.

STEP 7

Ensure compatibility with different screen sizes using media queries.

STEP 8

Add a footer with your name and register number.

STEP 9

Deploy the application and ensure it works correctly across various browsers.

STEP 10

Upload the project to GitHub Pages for hosting.

PROGRAM
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interactive Image Gallery</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f9;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            flex-direction: column;
            background: linear-gradient(135deg, #6a11cb, #2575fc);
            color: #333;
            margin-bottom: 60px; /* Space for footer */
        }

        .gallery-container {
            display: flex;
            justify-content: center;
            align-items: center;
            position: relative;
            overflow: hidden;
            background-color: #ffffff;
            border-radius: 10px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
            padding: 20px;
            margin-bottom: 20px;
        }

        .gallery {
            display: flex;
            transition: transform 0.5s ease-in-out;
        }

        .image-item {
            position: relative;
            margin: 0 10px;
        }

        .image-item img {
            width: 300px;
            height: 200px;
            object-fit: cover;
            border-radius: 8px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease;
        }

        .caption {
            position: absolute;
            bottom: 10px;
            left: 10px;
            background-color: rgba(0, 0, 0, 0.6);
            color: #fff;
            padding: 5px;
            font-size: 16px;
            opacity: 0;
            transition: opacity 0.3s ease;
            border-radius: 5px;
        }

        .image-item:hover .caption {
            opacity: 1;
        }

        .image-item:hover img {
            transform: scale(1.05);
        }

        button {
            background-color: #444;
            color: white;
            border: none;
            padding: 10px;
            font-size: 18px;
            cursor: pointer;
            border-radius: 50%;
            position: absolute;
            top: 50%;
            transform: translateY(-50%);
            z-index: 1;
            transition: background-color 0.3s;
        }

        button:hover {
            background-color: #333;
        }

        .prev-btn {
            left: 10px;
        }

        .next-btn {
            right: 10px;
        }

        footer {
            position: fixed;
            bottom: 0;
            left: 0;
            right: 0;
            background-color: #222;
            color: #fff;
            text-align: center;
            padding: 10px;
            font-size: 14px;
            box-shadow: 0 -2px 8px rgba(0, 0, 0, 0.2);
        }
    </style>
</head>
<body>
    <div class="gallery-container">
        <button class="prev-btn" id="prevBtn">&#10094;</button>
        <div class="gallery">
            <div class="image-item">
                <img src="c:\Users\SEC\Downloads\image3.jpg" alt="Image 1">
                <div class="caption">Image 1</div>
            </div>
            <div class="image-item">
                <img src="c:\Users\SEC\Downloads\image2.jpg" alt="Image 2">
                <div class="caption">Image 2</div>
            </div>
            <div class="image-item">
                <img src="c:\Users\SEC\Downloads\image1.jpg" alt="Image 3">
                <div class="caption">Image 3</div>
            </div>
            <div class="image-item">
                <img src="c:\Users\SEC\Downloads\image4.jpg" alt="Image 1">
                <div class="caption">Image 4</div>
            </div>
            
        </div>
        <button class="next-btn" id="nextBtn">&#10095;</button>
    </div>

    <footer>
        Dhareene R K 212222040035 | All rights reserved.
    </footer>

    <script>
        const gallery = document.querySelector('.gallery');
        const prevBtn = document.getElementById('prevBtn');
        const nextBtn = document.getElementById('nextBtn');
        let currentIndex = 0;

        function updateGalleryPosition() {
            const totalImages = document.querySelectorAll('.image-item').length;
            const imageWidth = document.querySelector('.image-item').offsetWidth;
            gallery.style.transform = `translateX(-${currentIndex * (imageWidth + 20)}px)`;
        }

        prevBtn.addEventListener('click', () => {
            const totalImages = document.querySelectorAll('.image-item').length;
            currentIndex = (currentIndex === 0) ? totalImages - 1 : currentIndex - 1;
            updateGalleryPosition();
        });

        nextBtn.addEventListener('click', () => {
            const totalImages = document.querySelectorAll('.image-item').length;
            currentIndex = (currentIndex === totalImages - 1) ? 0 : currentIndex + 1;
            updateGalleryPosition();
        });

        updateGalleryPosition();
    </script>
</body>
</html>
```

OUTPUT:

![webactivity](https://github.com/user-attachments/assets/8e04815b-aecd-421f-bb74-bc86ca7f6eff)


RESULT

The interactive image gallery using JavaScript is successfully created and functional.
