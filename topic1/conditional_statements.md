<!DOCTYPE html>
<html lang="en-us">

    <head>
        <title>conditional statements</title>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
    </head>
    <body>

    <p>Topic 1: Conditional Statements</p>
    <p id = "printMe1"></p>
    <p id = "printMe2"></p>
    <p id = "printMe3"></p>
    <p id = "printMe4"></p>
    <p id="demo"></p>

        <script>
            //if statement
            var motorcycle1 = "Triumph";
            var motorcycle2 = "Triumph";
            var response = "They are not the same.";

            if (motorcycle1 = motorcycle2) {
                response = "Yes, they are the same brand.";
            }
            document.getElementById("printMe1").innerHTML = response;

            //if else statement
            var motorcycle1 = "Triumph";
            var motorcycle2 = "Moto Guzzi";

            if (motorcycle1 == motorcycle2) {
                response = "Yes, they are the same brand";
            }
            else {
                response = "No, they are not the same brand."
            }
            document.getElementById("printMe2").innerHTML = response;

            //else if statement
            var motorcycle1 = "Triumph";
            var motorcycle2 = "Moto Guzzi";
            var motorcycle3 = "BMW";

            if (motorcycle1 == motorcycle2) {
                response = "Motorcycle1 and motorcycle2 are the same brand";
            }
            else if (motorcycle1 == motorcycle3) {
                response = "Motorcycle1 and motorcycle3 are the same brand.";
            }
            else if (motorcycle2 == motorcycle3) {
                response = "Motorcycle2 and motorcycle3 are the same brand.";
            }
            else {
                response = "No, none are not the same brand."
            }
            document.getElementById("printMe3").innerHTML = response;
            
            //switch statement
            var isita = "BMW";
            var motorcycle1 = "Triumph";
            var motorcycle2 = "Moto Guzzi";
            var motorcycle3 = "BMW";
            var motorcycle4 = "Honda";
            var motorcycle5 = "Ducati"
            
            switch (isita) {
                case "Triumph":
                    response = motorcycle1;
                    break;
                case "Moto Guzzi":
                    response = motorcycle2;
                    break;
                case "BMW":
                    response = motorcycle3;
                    break;
                case "Honda":
                    response = motorcycle4;
                    break;
                case "Ducati":
                    response = motorcycle5;
            }
            document.getElementById("printMe4").innerHTML = "It is a " + response + "!";

        </script>
    </body>
</html>


