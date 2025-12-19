# Ex.07 Design of Interactive Image Gallery
## Date:19-12-2025

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
    <title>Interactive Image Gallery</title>
    <link rel="stylesheet" href="styles.css">

    <script>
        const gallery = [
            { src: "vijayi1.jpg", caption: "VIJAY" },
            { src: "sk.jpg", caption: "SIVA KARTHIKEYAN" },
            { src: "surya.jpg", caption: "SURYA" },
            { src: "ajith.jpg", caption: "AJITH" },
            { src: "dhanush.jpg", caption: "DHANUSH" },
            { src: "arjun das.jpeg", caption: "ARJUN DAS" }
        ];

        let index = 0;

        function updateImage()
         {
            document.getElementById("img").src = gallery[index].src;
            document.getElementById("text").innerHTML = gallery[index].caption;
        }

        function next()
         {
            index++;
            if(index >= gallery.length){
               index = 0;
             }
            updateImage();
        }

        function previous()
         {
            index--;
            if(index < 0){
               index = gallery.length - 1;
            }
            updateImage();
        }
    </script>
</head>
<body>
    <div class="title">
        <h1>INTERACTIVE IMAGE GALLERY</h1>
    </div>
    <div class="allign">
        <div class="image">
            <img id="img" src="vijayi1.jpg" alt="Gallery Image">
            <h2 id="text">VIJAY</h2>
            <div class="button1">
                <button onclick="previous()">Previous</button>
                <button onclick="next()">Next</button>
            </div>
        </div>
    </div>
    <footer class="copyrights">
        <p>Designed and developed by Shanmuga Priya K (25004352) &copy; 2025</p>
    </footer>
</body>
</html>

styles.css
.title {
    height: 60px;
    width: 100%;
    background-color: rgb(126, 240, 236);
    color: black;
    text-align: center;
    line-height: 60px;
}

.allign {
    display: flex;
    justify-content: center;
    align-items: center;
    margin-top: 80px;
}

.image {
    width: 320px;
    background-color: rgb(254, 232, 203);
    border: 1px solid black;
    border-radius: 12px;
    padding: 20px;
    box-shadow: 0 8px 18px rgba(0, 0, 0, 0.2);

    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 15px;
}

.image img {
    height: 220px;
    width: 200px;
    border-radius: 10px;
    object-fit: cover;
}

.image h2 {
    font-size: 20px;
    margin: 0;
    text-align: center;
}

.button1 {
    display: flex;
    gap: 25px;
}

button {
    background-color: rgb(236, 58, 58);
    color: white;
    padding: 10px 18px;
    font-size: 15px;
    border: none;
    border-radius: 8px;
    cursor: pointer;
}

button:hover {
    background-color: rgb(200, 40, 40);
}

.copyrights {
    background-color: rgb(146, 115, 176);
    color: white;
    padding: 10px;
    position: fixed;
    bottom: 0;
    width: 100%;
    font-size: 14px;
    text-align: center;
}

```

## OUTPUT:
![alt text](<Screenshot (49).png>)
![alt text](<Screenshot (50)-1.png>)
![alt text](<Screenshot (51).png>)
![alt text](<Screenshot (52).png>)
![alt text](<Screenshot (53).png>)
![alt text](<Screenshot (54).png>)
## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
