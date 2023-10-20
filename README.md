<!--html version 5-->
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>  random number generator </title>
        <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.1/dist/css/bootstrap.min.css" rel="stylesheet"
            integrity="sha384-4bw+/aepP/YC94hEpVNVgiZdgIC5+VKNBQNGCHeKRQN+PtmoHDEXuppvnDJzQIu9" crossorigin="anonymous">
    
        <script type="text/javascript" src="https://www.gstatic.com/charts/loader.js"></script>
    
    </head>
    
    <body>
        <div class="container">
            <!-- Content here -->
    
            <nav class="navbar navbar-expand-lg navbar-light bg-light">
                <a class="navbar-brand" href="https://sci.skru.ac.th/science/index.php">คอมพิวเตอร์ศึกษา</a>
                <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent"
                    aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
                    <span class="navbar-toggler-icon"></span>
                </button>
    
                <div class="collapse navbar-collapse" id="navbarSupportedContent">
                    <ul class="navbar-nav mr-auto">
                        <li class="nav-item active">
                            <a class="nav-link" href="#">Home <span class="sr-only">(current)</span></a>
                        </li>
                        <li class="nav-item">
                            <a class="nav-link" href="#">Link</a>
                        </li>
                        <li class="nav-item dropdown">
                            <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button"
                                data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
                                Dropdown
                            </a>
                            <div class="dropdown-menu" aria-labelledby="navbarDropdown">
                                <a class="dropdown-item" href="#">Action</a>
                                <a class="dropdown-item" href="#">Another action</a>
                                <div class="dropdown-divider"></div>
                                <a class="dropdown-item" href="#">Something else here</a>
                            </div>
                        </li>
                        <li class="nav-item">
                            <a class="nav-link disabled" href="#">Disabled</a>
                        </li>
                    </ul>
                    <form class="form-inline my-2 my-lg-0">
                        <input class="form-control mr-sm-2" type="search" placeholder="Search" aria-label="Search">
                        <button class="btn btn-outline-success my-2 my-sm-0" type="submit">Search</button>
                    </form>
                </div>

            </nav>
            <h1>random number generator Calculator</h1>
           <h6> This version of the generator creates a random integer. It can deal with very large integers up to 
           a few thousand digits.</h6>
           
           <head>
<meta name="viewport"
content="width=device-width, initial-scale=1.0" />
<title>Random Number Generator</title>
<!-- Google Font -->
<link
href="https://fonts.googleapis.com/css2? family-Poppins:wght@400;600&display=swap"
rel="stylesheet"
/>
<!--Stylesheet -->
<link rel="stylesheet" href="style.css" />
</head>
<body>
<div class="container">
    <div class="wrapper">
        <div class="input-wrapper">
        <label for="min"class="col-sm-1 col-form-label" >Lower Limit : </label>
        <input type="number" id="min" value="0" />
        </div>
        <div class="input-wrapper">
            <label for="max"class="col-sm-1 col-form-label">Upper Limit :</label>
            <input type="number" id="max" value="10" />
        </div>
    </div>
    <button id="generate"  class="btn btn-success">Generate</button>
    <h2> resault </h2> <h3><div id="result">0</div></div></h3>
</div>

<!-- script -->
<script src="script.js"></script>

</body>
    </html>

let generateBtn = document.getElementById("generate")
;

function randomNum() {
    let min = document.getElementById("min");
    let max = document.getElementById("max");
    let minValue = Number(min.value);
    let maxValue = Number (max.value);
    if (minValue> maxValue) {
    minValue = maxValue + minValue;
    maxValue = minValue - maxValue;
    minValue = minValue - maxValue;
    min.value = minValue;
    max.value = maxValue;
    }
let num = Math.floor (Math.random() *  (maxValue -
    minValue + 1)) + minValue;
    document.getElementById("result").innerText = num;
}
window.addEventListener ("load", randomNum());
generateBtn.addEventListener("click", randomNum)
