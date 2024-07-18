<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Digital clock</title>
    <link rel="stylesheet" href="styl.css">
</head>
<body>
    <div class="hero">
        <div class="container">
            <div class="clock">
               <span id="hrs">00</span>
               <span>:</span>
               <span id="min">00</span>
               <span>:</span>
               <span id="sec">00</span>
            </div>
        </div>
    </div>
    
    <script>
        let hrs = document.getElementById("hrs");
        let min = document.getElementById("min");
        let sec = document.getElementById("sec");

        setInterval(()=>{
            let CurrentTime = new Date();

            hrs.innerHTML = (CurrentTime.getHours()<10?"0":"") + CurrentTime.getHours();
            min.innerHTML = (CurrentTime.getMinutes()<10?"0":"") + CurrentTime.getMinutes();
            sec.innerHTML = (CurrentTime.getSeconds()<10?"0":"") + CurrentTime.getSeconds();

        },1000)
      

    </script>
</body>
</html>
