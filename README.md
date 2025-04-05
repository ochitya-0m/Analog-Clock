/*# Analog-Clock
A simple and responsive analog clock built using HTML and CSS. This project showcases how to create a visually appealing analog clock using pure CSS for styling and animations, without any JavaScript.*/
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Clock</title>
    <link rel="icon" type="image/x-icon" href="https://www.freeiconspng.com/thumbs/clock-png/clock-png-32.png">
    <link rel="stylesheet" href="style.css">
    
</head>

<body>
    <div class="container">
        <div class="clock">
            <div class="circle" id="sc" style="--clr:#000000;" ><i></i></div>
            <div class="circle circle2" id="mn" style="--clr:#000000;" ><i></i></div>
            <div class="circle circle3" id="hr" style="--clr:#000000;" ><i></i></div>

            <span style="--i:1;"><b>1</b></span>
            <span style="--i:2;"><b>2</b></span>
            <span style="--i:3;"><b>3</b></span>
            <span style="--i:4;"><b>4</b></span>
            <span style="--i:5;"><b>5</b></span>
            <span style="--i:6;"><b>6</b></span>
            <span style="--i:7;"><b>7</b></span>
            <span style="--i:8;"><b>8</b></span>
            <span style="--i:9;"><b>9</b></span>
            <span style="--i:10;"><b>10</b></span>
            <span style="--i:11;"><b>11</b></span>
            <span style="--i:12;"><b>12</b></span>
            
        </div>
    </div>
    <script type="text/javascript">
        // const deg= 6; 
        const hr = document.querySelector('#hr');
        const mn = document.querySelector('#mn');
        const sc = document.querySelector('#sc');
    setInterval(()=>{
        let day = new Date();
        let hh= day.getHours() *30;
        let mm= day.getMinutes() *6;
        let ss= day.getSeconds() *6;

        hr.style.transform=`rotateZ(${hh+(mm/12)}deg)`;
        mn.style.transform=`rotateZ(${(mm)}deg)`;
        sc.style.transform=`rotateZ(${(ss)}deg)`;
    })
    </script>
</body>
</html>
