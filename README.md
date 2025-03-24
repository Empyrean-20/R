<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Slideshow</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: black;
            color: white;
            font-family: Arial, sans-serif;
            text-align: center;
        }
        .slideshow-container {
            position: relative;
            max-width: 80%;
        }
        .slide {
            display: none;
            position: relative;
        }
        img {
            width: 100%;
            border-radius: 10px;
        }
        .text {
            position: absolute;
            bottom: 10px;
            left: 50%;
            transform: translateX(-50%);
            background: rgba(0, 0, 0, 0.6);
            padding: 10px;
            border-radius: 5px;
        }
        .love-message {
            display: none;
            font-size: 1.5em;
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <div class="slideshow-container">
        <div class="slide">
            <img src="IMG_5953.jpeg" alt="Slide 1">
            <div class="text">I’ll bury u in a bed full of flowers… yet, no matter how many flowers… you’re still much more prettier than any cosmos out there… (PS: ik they’re not cosmos but get the emotions””)</div>
        </div>
        <div class="slide">
            <img src="IMG_6019.jpeg" alt="Slide 2">
            <div class="text">Our duo… is the perfect drama couple… koi bhi bakchodi, no one can do better than us… hehe</div>
        </div>
        <div class="slide">
            <img src="IMG_6092.jpeg" alt="Slide 3">
            <div class="text">When u rocked the stage… cuz I drew the perfect eyeliner for my baby</div>
        </div>
        <div class="slide">
            <img src="IMG_5931.JPG" alt="Slide 4">
            <div class="text">With us… we don’t need location or any fancy place… we need us and Vento to call it a date…</div>
        </div>
        <div class="love-message" id="loveMessage">Babe, I love you so much and do as much nakhre as u want, mei hai idhar sambhalne keliye…<br>PS: This is my first time… so please don’t judge me love ❤️</div>
    </div>
    
    <script>
        let slideIndex = 0;
        const slides = document.querySelectorAll(".slide");
        const loveMessage = document.getElementById("loveMessage");
        
        function showSlides() {
            if (slideIndex < slides.length) {
                slides.forEach(slide => slide.style.display = "none");
                slides[slideIndex].style.display = "block";
                slideIndex++;
                setTimeout(showSlides, 3000); 
            } else {
                slides.forEach(slide => slide.style.display = "none");
                loveMessage.style.display = "block";
            }
        }
        
        showSlides();
    </script>
</body>
</html>
