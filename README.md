# Ex.07 Design of Interactive Image Gallery
## Date:28.12.2025

## AIM:
To design a web application for an inteactive image gallery for a minimum five images with next and previous buttons.

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

## PROGRAM:
```
gallery.html

<html>
<head>
<title>IPL CAPTIONS Gallery</title>
<link rel="stylesheet" href="gallery.css">
</head>
<body>

<header>IPL CAPTIONS Gallery</header>

<div class="container">
    <div class="gallery-box">
        <img id="galleryImage" src="ipl caption.webp" alt="IPL CAPTIONS">
        <p class="caption" id="caption">IPL CAPTIONS</p>

        <div class="buttons">
            <button onclick="prev()">Previous</button>
            <button onclick="next()">Next</button>
        </div>
    </div>
</div>

<footer>
Designed by SABARINATHAN A(25005972) &copy; 2025
</footer>

<script>
let gallery = [
    "rutu csk.jpg",
    "jadeja rr.jpg",
    "harthik mi.png",
    "rajat rcb.png",
    "shreyas pbks.png"
];

let captions = [
    "ruturaj gaikwad (CSK)",
    "ravindra jadeja (RR)",
    "harthik pandya (MI)",
    "rajat patidar (RCB)",
    "shreyas iyer (PBKS)"
];

let index = 0;

function next(){
    index++;
    if(index >= gallery.length){
        index = 0;
    }
    document.getElementById("galleryImage").src = gallery[index];
    document.getElementById("caption").innerText = captions[index];
}

function prev(){
    index--;
    if(index < 0){
        index = gallery.length - 1;
    }
    document.getElementById("galleryImage").src = gallery[index];
    document.getElementById("caption").innerText = captions[index];
}
</script>

</body>
</html>

gallery.css

body{
    margin:0;
    font-family: Arial, sans-serif;
    background: linear-gradient(rgb(255, 88, 5),rgb(37, 37, 37),rgb(32, 24, 24));
    display:flex;
    flex-direction:column;
    min-height:100vh;
}

header{
    background-color: rgb(1, 250, 71);
    color:rgb(231, 18, 18);
    text-align:center;
    padding:15px;
    font-size:22px;
}

.container{
    flex:1;
    display:flex;
    justify-content:center;
    align-items:center;
}

.gallery-box{
    background-image: rgb(16, 163, 243);
    width:420px;
    padding:20px;
    border-radius:10px;
    box-shadow:0 5px 15px rgba(0,0,0,0.15);
    text-align:center;
}

.gallery-box img{
    width:100%;
    height:260px;
    object-fit:contain;
    background-color:rgb(0, 179, 255);
    border-radius:8px;
}

.caption{
    margin-top:12px;
    font-size:16px;
    color:#0fbe23;
}

.buttons{
    margin-top:15px;
    display:flex;
    justify-content:space-between;
}

.buttons button{
    padding:8px 18px;
    background-color:#6b7280;
    color:white;
    border:none;
    border-radius:6px;
    font-size:14px;
    cursor:pointer;
}

.buttons button:hover{
    background: linear-gradient(black,silver);
}

footer{
    text-align:center;
    padding:10px;
    font-size:13px;
    color:rgb(247, 222, 35);
}
```

## OUTPUT:
![alt text](<Screenshot (70).png>) 
![alt text](<Screenshot (71).png>)
![alt text](<Screenshot (73).png>) 
![alt text](<Screenshot (74).png>) 
![alt text](<Screenshot (75).png>) 



## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
