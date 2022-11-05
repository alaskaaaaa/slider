

<html>
    <head>

        <title>Image slider</title>
<link rel="stylesheet" href="">

<style>

body{
    margin: 0;
    padding: 0;
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    background: #23e3c9;
}
.slider{
    width: 800px;
    height: 500px;
    border-radius: 10px;
    overflow: hidden;
}
.slides{
    width: 500%;
    height: 500px;
    display: flex;
}
.slides input{
    display: none;
}
.slide{
    width: 20%;
    transition: 2s;
}
.slide img{
   width: 800px;
   height: 500px;
}
.navigation-manual{
    position: absolute;
    width: 500px;
    margin-top: -40px;
    display: flex;
    justify-content: center;

}
.manual-btn{
    border: 2px solid #4803dc;
    padding: 5px;
    border-radius: 10px;
    cursor: pointer;
    transition: 1s;
}
.manual-btn:not(:last-child){
    margin-right: 40px;
}
.manual-btn:hover{
    background: #4803dc;
}
#radio1:checked ~ .first{
    margin-left: 0;
}
#radio2:checked ~ .first{
    margin-left: -20%;
}
#radio3:checked ~ .first{
    margin-left: -40%;
}
#radio4:checked ~ .first{
    margin-left: -60%;
}
.navigation-auto{
    position: absolute;
    display: flex;
    width: 500px;
    justify-content: center;
    margin-top: 460px;
}
.navigation-auto div{
    border:2px solid #4803dc;
    padding: 5px;
    border-radius: 10px;
    transition: 1s;
}
.navigation-auto div:not(:last-child){
    margin-right: 40px;
}
#radio1:checked ~ .navigation-auto .auto-btn1{
    background: #4803dc;
}
#radio2:checked ~ .navigation-auto .auto-btn2{
    background: #4803dc;
}
#radio3:checked ~ .navigation-auto .auto-btn3{
    background: #4803dc;
}
#radio4:checked ~ .navigation-auto .auto-btn4{
    background: #4803dc;
}
</style>
    </head>
    <body>

<div class="slider">
<div class="slides">

    <input type="radio" name="radio-btn" id="radio1">
    <input type="radio" name="radio-btn" id="radio2">
    <input type="radio" name="radio-btn" id="radio3">
    <input type="radio" name="radio-btn" id="radio4">

<div class="slide first">
    <img src="image1.jpg">
</div>


<div class="slide">
    <img src="image2.jpg">
</div>

<div class="slide">
    <img src="image3.jpg">
</div>

<div class="slide">
    <img src="image4.jpg">
</div>


<div class="navigation-auto">
<div class="auto-btn1"></div>
<div class="auto-btn2"></div>
<div class="auto-btn3"></div>
<div class="auto-btn4"></div>
</div>



</div>

<div class="navigation-manual">
    <label for="radio1" class="manual-btn"></label>
    <label for="radio2" class="manual-btn"></label>
    <label for="radio3" class="manual-btn"></label>
    <label for="radio4" class="manual-btn"></label>
</div>


</div>


<script>

var counter = 1;
setInterval(function(){
    document.getElementById('radio' + counter).checked = true;
    counter++;
    if(counter > 4){
        counter = 1;
    }
}, 2500);



</script>



    </body>
    </html>
