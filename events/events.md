<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8">
        <meta name="viewport" content="width=device-width, initial-scale=1">
        <link href="https://johnson-robert.github.io/cit261/images/favicon.ico" type="image/x-icon" rel="shortcut icon">
        <!--<link href="https://johnson-robert.github.io/cit261/css/main.css" rel="stylesheet">-->
        <link href="./events.css" rel="stylesheet">
        <title>CIT 261 Assignment Portal | Rob Johnson | BYU-Idaho</title>
    </head>
    <body>
        <div id="outsideBox">
            <div id="topBox">
                <h2>Changing CSS properties using JavaScript events!</h2>
                <p>Left click this button to change the display and move the image to the right side of the screen.</p>
                <button id="buttonOne" onclick="changeDisplay()">Click Me</button>

                <p>Left click me to add a border.</p>
                <p>Right click to change the border color.</p>
                <p>Use the middle(roller) button to remove the  border</p>
                <button id="buttonTwo" onmousedown="changeBorder(event)">Click Me</button>

                <p>Mouse over the image to change it's shape.</p>

                <p>Then spin the mouse wheel while over the image to start the animation.</p>
                <p id="warning" onmouseover="changeWarning()">Warning: only animate once!</p>

            </div>
            <div id="bottomBox">
                <img id="imgOne" onmouseover="changeImgShape()" src="../images/dazzle_man.png" alt="Dazzle Man"/>
            </div>
        </div>
        <script>
            document.getElementById("buttonOne").style.backgroundColor = "yellowgreen";
            document.getElementById("buttonTwo").style.backgroundColor = "yellowgreen";

            function changeDisplay() {
                document.getElementById("outsideBox").style.display = "flex";
                document.getElementById("outsideBox").style.flexDirection = "row";
            }
            function changeBorder(event) {
                var x = event.buttons;
                if (x === 1) {
                    document.getElementById("imgOne").style.border = "thick solid black";
                } else if (x === 2) {
                    document.getElementById("imgOne").style.borderTopColor = "lightgray";
                    document.getElementById("imgOne").style.borderRightColor = "gray";
                } else if (x === 4) {
                    document.getElementById("imgOne").style.border = "none";
                }
            }
            function changeImgShape() {
                document.getElementById("imgOne").style.transition = "all 2s";
                document.getElementById("imgOne").style.borderRadius = "50%";
                document.getElementById("imgOne").style.cursor = "url(../images/spyro.cur),auto";
            }
            function changeWarning() {
                document.getElementById("buttonTwo").style.backgroundColor = "yellow";
                document.getElementById("warning").style.color = "magenta";
                document.getElementById("warning").style.textDecoration = "underline overline";
                document.getElementById("warning").style.textDecorationColor = "white";
                document.getElementById("warning").style.textDecorationStyle = "wavy";
            }
            function animateImg() {
                document.getElementById("buttonTwo").style.backgroundColor = "green";
            }
            document.getElementById("imgOne").addEventListener("wheel", spinImg);
            document.getElementById("myP").addEventListener("touchstart", spinImg);

            function spinImg() {
                document.getElementById("imgOne").style.animation = "rotateImg 1s 5";
                document.getElementById("ingOne").style.animationTimingFunction = "linear";
            }

        </script>
    </body>
</html>

