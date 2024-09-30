<!DOCTYPE html>
<html>
<head>
    
    <link rel="stylesheet" href="styles.css">
    <title>analog clock</title>
</head>
<body>
       <div class="container">
           <div class="clock">

           
            <div style="--clr:#ff3d58;" class="hand"><i></i></div>
            <div style="--clr:#00a6ff;" class="hand"><i></i></div>
            <div style="--clr:#ffffff;" class="hand"><i></i></div>
            <span style="--i:1;"><b>1</b></span>
            <span style="--i:1;"><b>2</b></span>
            <span style="--i:1;"><b>3</b></span>
            <span style="--i:1;"><b>4</b></span>
            <span style="--i:1;"><b>5</b></span>
            <span style="--i:1;"><b>6</b></span>
            <span style="--i:1;"><b>7</b></span>
            <span style="--i:1;"><b>8</b></span>
            <span style="--i:1;"><b>9</b></span>
            <span style="--i:1;"><b>10</b></span>
            <span style="--i:1;"><b>11</b></span>
            <span style="--i:1;"><b>12</b></span>
       </div>
    </div>

    <script src="script.js"></script>
</body>
</html>

 style.css
 
*{
   margin: 0;
   padding: 0;
   box-sizing: border-box;
   font-family: sans-serif;
   color: #fff;
}

body{
       display: flex;
       justify-content: center;
       align-items: center;
       min-height: 100vh;
       background-color: #212121;
}

.container{
    position: absolute;
}

.clock{
    width: 300px;
    height: 300px;
    border-radius: 50%;
    background-color: rgba(255, 255, 255, 0.1);
    border: 2px solid rgba(255, 255, 255, 0.25);
    box-shadow: 0px 0px 30px rgba(0, 0, 0, 0.9);
    display: flex;
    justify-content: center;
    align-items: center;
}

.clock span{
    position: absolute;
    transform: rotate(calc(30deg * var(--i)));
    inset:12px;
    text-align: center;
}

.clock span b{
    transform: rotate(calc(-30deg * var(--i)));
    display: inline-block;
    font-size: 20px;
}

.clock::before{
    content: '';
    position: absolute;
    width: 8px;
    height: 8px;
    border-radius: 50%;
    background-color: #fff;
}

.hand{
    position: absolute;
    display: flex;
    justify-content: center;
    align-items: flex-end;
}
.hand i{
    position: absolute;
    background-color: var(--clr);
    width: 4px;
    height: 70px;
    border-radius: 8px;
    
}
