<!DOCTYPE html>

<html>
    <head>
        <meta charset="utf-8">
        <meta name="viewport" content="width=device-width, initial-scale=1">
        <link href="https://johnson-robert.github.io/cit261/images/favicon.ico" type="image/x-icon" rel="shortcut icon">
        <link href="https://johnson-robert.github.io/cit261/css/main.css" rel="stylesheet">
        <title>CIT 261 Assignment Portal | Rob Johnson | BYU-Idaho</title>
    </head>
    <body>
        <h3>Input New TaeKwonDo Pattern</h3>
        <h4>Change each field for the new pattern.</h4>
        <input type="text" id="newPattern" placeholder="Pattern Name" value="CHON-JI" required><br>
        <input type="text" id="style" placeholder="ITF or WTF" value="ITF" required><br>
        <input type="text" id="belt" placeholder="Belt Color" value="White" required><br>
        <input type="text" id="movements" placeholder="Number of Movements" value="19" required><br>
        <input type="text" id="ready_stance" placeholder="Ready Stance" value="Parallel" required><br>

        <button onclick="AddPattern()">Add New Pattern</button>

        <p>Pattern Name : <span id="printMe1"></span></p>
        <p>Pattern Style: <span id="printMe2"></span></p>
        <p>Pattern Belt: <span id="printMe3"></span></p>
        <p>Movements: <span id="printMe4"></span></p>
        <p>Ready Stance: <span id="printMe5"></span></p>
        <p>Pattern JSON: <span id="printMe6"></span></p>
        <h4>Pattern Retrieved From Local Storage</h4>
        <p>Pattern Name: <span id="printMe7"></span></p>
        <p>Pattern Style: <span id="printMe8"></span></p>
        <p>Pattern Belt: <span id="printMe9"></span></p>
        <p>Movements: <span id="printMe10"></span></p>
        <p>Ready Stance: <span id="printMe11"></span></p>

        <script>
            function AddPattern() {
                var a = document.getElementById("newPattern").value;
                var b = document.getElementById("style").value;
                var c = document.getElementById("belt").value;
                var d = document.getElementById("movements").value;
                var e = document.getElementById("ready_stance").value;

                var chon_ji = new Form(b, c, d, e);

                //create new object. 
                function Form(style, belt, movements, stance) {
                    this.style = style;
                    this.belt = belt;
                    this.movements = movements;
                    this.stance = stance;
                }
                document.getElementById("printMe1").innerHTML = a;
                document.getElementById("printMe2").innerHTML = b;
                document.getElementById("printMe3").innerHTML = c;
                document.getElementById("printMe4").innerHTML = d;
                document.getElementById("printMe5").innerHTML = e;
   
   
                //convert chon_ji to text
                var patternJSON = JSON.stringify(chon_ji);
                document.getElementById("printMe6").innerHTML = patternJSON;

                //save chun_ji to localStorage
                localStorage.setItem("patternText", patternJSON);

                //retrieve chun_ji from localStorage
                var text = localStorage.getItem("patternText");
                var chun_ji_tul = JSON.parse(text);

                document.getElementById("printMe7").innerHTML = "CHUN-JI-TUL";
                document.getElementById("printMe8").innerHTML = chun_ji_tul.style;
                document.getElementById("printMe9").innerHTML = chun_ji_tul.belt;
                document.getElementById("printMe10").innerHTML = chun_ji_tul.movements;
                document.getElementById("printMe11").innerHTML = chun_ji_tul.stance;
            }
        </script>
    </body>
</html>

