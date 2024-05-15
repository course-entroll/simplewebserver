# EX01 Developing a Simple Webserver

## Date: 23/03/2024

## AIM:
To develop a simple webserver to serve html pages.

## DESIGN STEPS:
### Step 1: 
HTML content creation.

### Step 2:
Design of webserver workflow.

### Step 3:
Implementation using Python code.

### Step 4:
Serving the HTML pages.

### Step 5:
Testing the webserver.

## PROGRAM:
```
<!DOCTYPE html>
<html lang="en">
<head>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.11.3/font/bootstrap-icons.min.css">
    <title>Saveetha Home Page</title>
    <style>
    i{
    color:#cc324b;
    font-size: 20px;
    padding: 10px;
}
i:hover {
    color: black;
}
.anchor{
    text-decoration: none;
    color: #cc324b;
    font-size: 15px;
    font-family:Arial ;
    padding: 5px;
}
.aside
{

width:30%;
margin:1% 0% 0% 1%;
background-color: rgb(205, 78, 78);
margin-top: 0%;
padding:2%;
align-items: center;
}
.images {
  display: flex;
  

}
.images > div {
  margin-right: 10px;
  margin-left: 5px;
  margin-inline-start: 10px;         
  
}
.row6 {
display: flex;
align-items: center; 

justify-content: space-between;
}
.row5 {
display: flex;
align-items: center; 
margin-top: 5px;
justify-content: space-between;
}
<style>
</head>
<body>
    <div class="row" style="background-color:#f3f3f3">
        <div class="col-5">
            <a href=""><i class="bi bi-twitter"></i></a>
            <a href=""><i class="bi bi-youtube"></i></a>
            <a href=""><i class="bi bi-facebook"></i></a>
            <a href=""><i class="bi bi-linkedin"></i></a>
            <a href=""><i class="bi bi-pinterest"></i></a>
            <a href=""><i class="bi bi-whatsapp"></i></a>
            <a href=""><i class="bi bi-instagram"></i></a>
          </div>
        <div class="col-4 "> 
            <a href="">Alumni</a><i class="bi bi-three-dots-vertical"></i></a>
            <a href="">Event</a><i class="bi bi-three-dots-vertical"></i></a>
            <a href="">Career</a><i class="bi bi-three-dots-vertical"></i></a>
            <a href="">Login</a><i class="bi bi-three-dots-vertical"></i></a>
            <a href="">SEC portal</a>
          </div>
        <div class="col-3">
             <div style="border: 2px solid;border-radius: 15px">
                <i class="bi bi-search"></i>
                <input type="text" placeholder="search" style="background-color: #f3f3f3;border:0px; outline: none;"/>
            </div>
       </div>
    </div>
    <div class="row m-2" >
        <div class="col-4">
            <img src="assets/images/logo.png" width="450px">
        </div>
        <div class="col-6">
          <nav class="navbar navbar-expand-lg bg-body-tertiary">
            <div class="container-fluid">
              
              <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
              </button>
              <div class="collapse navbar-collapse" id="navbarSupportedContent">
                <ul class="navbar-nav me-auto mb-2 mb-lg-0">
                  <li class="nav-item">
                    <a class="nav-link active" aria-current="page" href="#">Home</a>
                  </li>
                  <li class="nav-item">
                    <a class="nav-link" aria-current="page" href="#">About</a>
                  </li>
                  <li class="nav-item">
                    <a class="nav-link" aria-current="page" href="#">Departments</a>
                  </li>
                  <li class="nav-item">
                    <a class="nav-link" aria-current="page" href="#">Life at SEC</a>
                  </li>
                  <li class="nav-item">
                    <a class="nav-link" aria-current="page" href="#">Admissions</a>
                  </li>
                  <li class="nav-item">
                    <a class="nav-link" aria-current="page" href="#">Placements</a>
                  </li>
                  <li class="nav-item">
                    <a class="nav-link" aria-current="page" href="#">Research</a>
                  </li>
                </ul>  
              </div>
            </div>
          </nav>
        </div>
        <div class="col-2  border-2">
          <div style="width:100%; align-items:right; background-color: gray;">
            <p> FOR ADMISSION <br>
             <i class="bi bi-whatsapp"></i> 9876544678</p>
        </div>
        </div>
    </div>
    <div style="display:flex;">
      <div class="aside" style="width:20%; height:570px;">
          <p id="text">ADMISSION ENQUIRY</p>
          <button>APPLY NOW</button>
          <hr>
          <br>
          <p id="text">Chat with Student Ambassador </p>
          <button>KNOW MORE</button>
          <hr>
          <br>
          <p id="text">BLOGS</p>
          <button>KNOW MORE</button>
          <hr>
        
      </div>

    <div id="carouselExampleIndicators" class="carousel slide" >
      <div class="carousel-indicators">
        <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="0" class="active" aria-current="true" aria-label="Slide 1"></button>
        <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="1" aria-label="Slide 2"></button>
        <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="2" aria-label="Slide 3"></button>
      </div>
      <div class="carousel-inner">
        <div class="carousel-item active">
          <img src="assets/images/nature1.jpg" class="d-block w-100" height="auto" alt="...">
        </div>
        <div class="carousel-item">
          <img src="assets/images/nature2.jpg" class="d-block w-100" alt="...">
        </div>
        <div class="carousel-item">
          <img src="assets/images/nature3.jpeg" class="d-block w-100" alt="...">
        </div>
      </div>
      <button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide="prev">
        <span class="carousel-control-prev-icon" aria-hidden="true"></span>
        <span class="visually-hidden">Previous</span>
      </button>
      <button class="carousel-control-next" type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide="next">
        <span class="carousel-control-next-icon" aria-hidden="true"></span>
        <span class="visually-hidden">Next</span>
      </button>
    </div>
    </div>
    <br>
    <div class="images">
      <div id="img1">
       <img src="assets/images/img1.jpg" alt="" width="250px" ,height="150px">
      </div>
      <div id="img2">
       <img src="assets/images/img2.jpg" alt="" width="250px" ,height="150px">
      </div>
      <div id="img3">
       <img src="assets/images/img3.jpg" alt="" width="250px" ,height="150px">
      </div>
      <div id="img4">
       <img src="assets/images/img4.jpg" alt="" width="250px" ,height="150px">
      </div>
      <div id="img5">
       <img src="assets/images/img5.jpg" alt="" width="250px" ,height="150px">
      </div>
     </div>
    
</div>

<div class="row5">
  <div class="col-3" id="div1">
    <img src="assets/images/img6.png" height="400px" >
  </div>
  <br>
  <div class="col-6" id="div2">
    <img src="assets/images/img7.jpg" alt="" width="600px">
    <p>
      SEC is a leading Engineering College located in Chennai, India., which offers a global approach to education and research, with a focus on global perspectives and expertise. SEC offers a wide range of undergraduate, postgraduate and doctoral programs in Engineering. Some of its Academic Highlights are,

Only Engineering College in India to have 30 students per class.
91% results in University exam.
173 University Ranks.
Compulsory internship every year. 
    </p>
  </div>
  <div class="col-3" id="div3">
    <h4>
      Latest Events
    </h4>
    <br>
    <p class="date">
      19 Mar 2024;
      </p>
      <p class="event">
      A warm welcome to HR Team of 'Foxconn Industrial Internet'.
    </p>
    <hr>
    <p class="date">
      21 Mar 2024;
    </p>
    <p class="event">
     MBA Final Year learners bagged a coveted placement at 'HDB Financial Services'
    </p>
    <hr>
  <p class="date">16 Mar 2024;
    </p>
    <p class="event">
    SEC kick started cultural fest - CELANZA’24 with a Big Bang</p>
  </div>
</div>

<div class="row6" >
  <div class="col-4">
    <img src="assets/images/logo.png" alt="" width="400px" height="65px">
  </div>
  <div class="col-2" id="icon1">
    <a href="#">
      <i class="bi bi-envelope"></i>  Contact Us Today
    </a>
  </div>
  <div class="col-3" id="icon2">
    <a href="#">
      <i class="bi bi-telephone"></i> +91 4466726677
    </a>
  </div>

  <div class="col-3" id="icon3">
    <a href="#">
      <i class="bi bi-telephone"></i> +91 4466726690
    </a>
  </div>

</div>


    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz" crossorigin="anonymous"></script>
</body>
</html>
```


## OUTPUT:
![image](https://github.com/Yugendaran/simplewebserver/assets/128135616/6b93adda-2096-4ef1-b419-bbd3f1b29e01)

![image](https://github.com/Yugendaran/simplewebserver/assets/128135616/06c77402-b6e9-4d33-acf8-0e027c7f1f31)


## RESULT:
The program for implementing simple webserver is executed successfully.
