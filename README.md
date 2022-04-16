<!DOCTYPE html>
<html>
    <head>
        <meta name="viewport" content="width=device-width, initial-scale=1">
        <title>Seedling</title>
        <link rel="icon" type="image/x-icon" href="https://cdn-icons-png.flaticon.com/512/708/708503.png?w=826">
        <link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Patrick Hand|Luckiest Guy|Boogaloo&effect=3d">
        <style>
            header{
                margin: 0;
                padding: 0;
            }

            nav{
                width: 100%;
                padding-top: 15px;
                padding-bottom:15px;
                background: #344436;
                overflow: auto;
            }
            
            ul{
                padding: 0;
                margin: 0 0 0 150px;
                list-style: none;
            }

            li{
                float: right;
                font-size: 15px;
                font-family: 'Boogaloo', sans-serif;
            }

            .logo{
                position: absolute;
                margin-top: 20px;
                margin-left: 20px;
                font-size: 30px;
                font-weight: bold;
                font-family: 'Patrick Hand', sans-serif;
            }

            nav a{
                width: 100px;
                display: block;
                padding: 15px 15px;
                color: black;
                text-align: center;
            }

            nav a:hover{
                background-color: rgba(165, 192, 171);
                color: black;
                transition: 0.5s;
                cursor: grab;
            } 

            body, html {
                height: 100%;
                margin: 0;
            }

            .hero-image {
                background-image: linear-gradient(rgba(0, 0, 0, 0.2), rgba(0, 0, 0, 0.3)), url("https://img.freepik.com/free-photo/child-hands-holding-caring-young-green-plant_1150-12738.jpg?t=st=1648271909~exp=1648272509~hmac=fe37ecfb941ef62c904cb3c1e74fd42d8e93bce5dddd335df9f020a5aac85c09&w=1380");
                height: 50%;
                background-position: center;
                background-repeat: no-repeat;
                background-size: cover;
                position: relative;
            }

            .hero-text {
                text-align: left;
                position: absolute;
                top: 40%;
                left: 75%;
                transform: translate(-55%, -45%);
                color: white;
                font-family: 'Luckiest Guy',sans-serif;
                font-size: 35px;
            }

            .hero-text button {
                border: none;
                outline: 0;
                display: inline-block;
                padding: 10px 25px;
                color: rgb(255, 255, 255);
                background-color: #344436;
                text-align: center;
                cursor: grab;
                font-size: 12px;
            }

            .hero-text button:hover {
                background-color: rgba(165, 192, 171);
                color: rgb(0, 0, 0);
            }

            .Div {
                border: none;
                background-color: white;    
                margin: 0 auto;
                width: 1358px;
                height: 828px;
             }

            .grid-container {
                display: grid;
                grid-template-columns: auto auto auto ;
                gap: 20px;
                background-color: white;
                padding: 20px;
            }

            .grid-container > div {
                background-color: rgba(165, 192, 171);
                border: 8px solid #344436;
                text-align: center;
                font-size: 30px;
                width:426px;
                height:247px;
            }

            .image{
                    width: 426px;
                    height: 247px;
            }

            .container {
                position: relative;
                width: 50%;
            }

            .overlay {
                position: absolute;
                top: 0;
                bottom: 0;
                left: 0;
                right: 0;
                height: 100%;
                width: 100%;
                opacity: 0;
                transition:.5s ease;
                background-color: rgba(165, 192, 171);
            }

            .container:hover .overlay {
                opacity: 1;
            }

            .text {
                color: b;
                font-size: 30px;
                position: absolute;
                top: 50%;
                left: 50%;
                transform: translate(-50%,-50%);
                text-align: center;
                font-family: 'Boogaloo',sans-serif;
            }

            .mySlides {display: none}

            img {vertical-align: middle;}

            .slideshow-container {
                max-width: 1000px;
                position: relative;
                margin: auto;
            }

            .prev, .next {
                cursor: pointer;
                position: absolute;
                top: 50%;
                width: auto;
                padding: 16px;
                margin-top: -22px;
                color: white;
                font-weight: bold;
                font-size: 18px;
                transition: 0.6s ease;
                border-radius: 0 3px 3px 0;
                user-select: none;
            }

            .next {
                right: 0;
                border-radius: 3px 0 0 3px;
            }

            .prev:hover, .next:hover {
                background-color: rgba(0,0,0,0.8);
            }

            .numbertext {
                color: #f2f2f2;
                font-size: 12px;
                padding: 8px 12px;
                position: absolute;
                top: 0;
            }

            .Overlay {
                position: absolute; 
                bottom: 0;
                padding: 20px;
                background: rgb(0, 0, 0, 0);
                background: rgba(0, 0, 0, 0.5);
                width: 96%;
                color: #f1f1f1;
                transition: .5s ease;
                opacity: 0;
                color: white;
                font-size: 25px;
                text-align: center;
                font-family: 'Luckiest Guy',sans-serif;
            }

            .slideshow-container:hover .Overlay{
                opacity: 1;
            }

            .dot {
                cursor: pointer;
                height: 15px;
                width: 15px;
                margin: 0 2px;
                background-color: #bbb;
                border-radius: 50%;
                display: inline-block;
                transition: background-color 0.6s ease;
            }

            .active, .dot:hover {
                background-color: #717171;
            }

            .fade {
                animation-name: fade;
                animation-duration: 1.5s;
            }

            @keyframes fade {
                from {opacity: .4} 
                to {opacity: 1}
            }

            @media only screen and (max-width: 300px) {
            .prev, .next,.text {font-size: 11px}
            }

            h2{
                font-family: 'Luckiest Guy', sans-serif;
            }
            .bg-img {
                background-image: url("https://images.unsplash.com/photo-1503610594381-aed30c818b8e?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1469&q=80");
                min-height: 500px;
                background-position: center;
                background-repeat: no-repeat;
                background-size: cover;
                position: relative;
            }

            .Container {
                position: absolute;
                right:0;
                margin: 17px;
                max-width: 500px;
                padding: 50px;
                background-color: white;
            }

            .btn {
                background-color: #344436;
                color: aliceblue;
                padding: 24px 28px;
                border: none;
                cursor: grab;
                width: 100%;
                opacity: 0.8;
                font-family:'Boogaloo', sans-serif;
            }

            .btn:hover {
                opacity: 1;
            }

            label {
                font-family: 'Boogaloo', sans-serif;
            }

            .DIV{
                background-color:#344436;
                color:black;
                padding: 10px 28px;
            }
            DIV dl{
                font-size: 20px;
                font-family: 'Boogaloo', sans-serif;
            }

            DIV p{
                text-align: right;
                font-size: 18px;
                font-family: 'Boogaloo', sans-serif;
            }
         </style>
    </head>
    <body>
        <header>
            <div class="logo"><img src="https://cdn-icons-png.flaticon.com/512/708/708503.png?w=826" width="40" height="40">Seedling</div>
            <nav>
                <ul>
                    <li><a>Contact</a></li>
                    <li><a>Our Project</a></li>
                    <li><a>What We Do</a></li>
                    <li><a>Home</a></li>
                </ul>
            </nav>
        </header>
        <div class="hero-image">
            <div class="hero-text font-effect-3d">
                EVERY CHILD IS<br> 
                <strong><MARK>INNOCENT</MARK></strong>.<br>
                SAVE THEM FROM DARKENESS AND DESPAIR.<br><br>
                <button>read more ...</button>
            </div>
        </div>

        <br>
        <br>

        <div class="Div">
            <div class="grid-container">
                <div class="container">
                    <div><img src="https://images.unsplash.com/photo-1542810634-71277d95dcbb?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1632&q=80"class="image">
                        <div class="overlay">
                            <div class="text">Rights</div>
                        </div>
                    </div>
                </div>    
        
                <div class="container">
                    <div><img src="https://images.unsplash.com/photo-1547082661-71362fc3969c?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1632&q=80"class="image">
                        <div class="overlay">
                            <div class="text">Education</div>
                        </div>
                    </div>
                </div>    
        
                <div class="container">
                    <div><img src="https://images.unsplash.com/photo-1576381394626-53b3d2d48145?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1470&q=80"class="image">
                        <div class="overlay">
                            <div class="text">Protection</div>
                        </div>
                    </div>
                </div>    
        
                <div class="container">
                    <div><img src="https://images.unsplash.com/flagged/photo-1555251255-e9a095d6eb9d?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1470&q=80"class="image">
                        <div class="overlay">
                            <div class="text">Advocacy</div>
                        </div>
                    </div>
                </div>    
        
                <div>
                    <h3 style="text-align:center;line-height:170px;font-family:Luckiest Guy,sans-serif" >What We Do</h3>
                </div>
        
                <div class="container">
                    <div><img src="https://images.unsplash.com/photo-1635929114944-8bab23b98e74?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1534&q=80"class="image">
                        <div class="overlay">
                            <div class="text">Survival</div>
                        </div>
                    </div>
                </div>    
        
                <div class="container">
                    <div><img src="https://images.unsplash.com/photo-1523881374236-dd34f6ac1226?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1630&q=80"class="image">
                        <div class="overlay">
                            <div class="text">Healths</div>
                        </div>
                    </div>
                </div>    
        
                <div class="container">
                    <div><img src="https://images.unsplash.com/photo-1547496614-54ff387d650a?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1470&q=80"class="image">
                        <div class="overlay">
                            <div class="text">Care</div>
                        </div>
                    </div>
                </div>    
        
                <div class="container">
                    <div><img src="https://images.unsplash.com/photo-1599059813005-11265ba4b4ce?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1470&q=80"class="image">
                        <div class="overlay">
                            <div class="text">Emergency Response</div>
                        </div>
                    </div>
                </div>    
        
            </div>
        </div>
        <br>
        <br>
        <br>
        <br>
        <div class="slideshow-container">
            <div class="mySlides fade">
                <div class="numbertext">1 / 3</div>
                <img src="https://images.unsplash.com/photo-1488521787991-ed7bbaae773c?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1470&q=80" style="width:100%">
                <div class="Overlay">Child Sponsorship Program</div>
            </div>

            <div class="mySlides fade">
                <div class="numbertext">2 / 3</div>
                <img src="https://images.unsplash.com/photo-1636202339022-7d67f7447e3a?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1471&q=80" style="width:100%">
                <div class="Overlay">Rural Teacher Support Program</div>
            </div>

            <div class="mySlides fade">
                <div class="numbertext">3 / 3</div>
                <img src="https://images.unsplash.com/photo-1617450365226-9bf28c04e130?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1470&q=80" style="width:100%">
                <div class="Overlay">Volunteer Recruitment Program</div>
            </div>

            <a class="prev" onclick="plusSlides(-1)">❮</a>
            <a class="next" onclick="plusSlides(1)">❯</a>

        </div>
        <br>
        <div style="text-align:center">
            <span class="dot" onclick="currentSlide(1)"></span> 
            <span class="dot" onclick="currentSlide(2)"></span> 
            <span class="dot" onclick="currentSlide(3)"></span> 
        </div>

        <script>
        let slideIndex = 1;
        showSlides(slideIndex);

        function plusSlides(n) {
        showSlides(slideIndex += n);
        }

        function currentSlide(n) {
        showSlides(slideIndex = n);
        }

        function showSlides(n) {
        let i;
        let slides = document.getElementsByClassName("mySlides");
        let dots = document.getElementsByClassName("dot");
        if (n > slides.length) {slideIndex = 1}    
        if (n < 1) {slideIndex = slides.length}
        for (i = 0; i < slides.length; i++) {
            slides[i].style.display = "none";  
        }
        for (i = 0; i < dots.length; i++) {
            dots[i].className = dots[i].className.replace(" active", "");
        }
        slides[slideIndex-1].style.display = "block";  
        dots[slideIndex-1].className += " active";
        }
        </script>
        <br>

        <footer>
            <div class="bg-img">
                <form action="/action_page.php" class="Container">
                    <h2>Leave Us A Massage</h2>
                    <label for="yourname">First Name</label>
                    <br>
                    <input type="text"id="yourname"name="yourname">
                    <br>
                    <br>
                    <label for="yourname">Last Name</label>
                    <br>
                    <input type="text"id="yourname"name="yourname">
                    <br>
                    <br>
                    <label for="yourname">Message</label>
                    <br>
                    <textarea rows=“20” id=”remarks”></textarea>
                    <br>
                    <br>
                    <br>
                    <button type="submit" class="btn">Submit</button>
                </form>  
            </div>
            <br>
            <br>
            <div class="DIV">
                <div>
                    <h2>Contact Us</h2>
                    <dl>
                        <dt>Telephone</dt>
                        <dd>+60112978356</dd>
                    </dl>
                </div>

                <div>
                    <h2>BUSINESS HOURS</h2>
                    <dl>
                        <dt>Sunday-Thruday</dt>
                        <dd>0800-2200</dd>
                    </dl>
                </div>
                
                <div>
                    <p>Copyright Ⓒ 2022 | Seedling All Rights Reserved | Design by KTTC</p>
                </div>
            </div>
        </footer>   
    </body>
</html>
