<!DOCTYPE html>
<html>
    <body>
        <h2>Your JSON weather object from openweather.org</h2>
        <div id="objectText"></div>
        <script>
            var requestURL = "http://api.openweathermap.org/data/2.5/weather?zip=97132,us&APPID=c3259b476fba8880191b6e087f87f2e9";
            var request = new XMLHttpRequest();
            request.open("GET", requestURL);
            request.responseType = "text";
            request.send();
            request.onreadystatechange = function () {
                var jsonObj = request.response;
                document.getElementById("objectText").innerHTML = jsonObj;
            }
        </script>

        <h2>Your location from the weather object.</h2>
        
        <button type="button" onclick="getObject()">Location Button</button>
        
        <div>Longitude: <span id="lon"></span></div>
        <div>Latitude: <span id="lat"></span></div>

        <script>
            function getObject() {
                var requestURL = "http://api.openweathermap.org/data/2.5/weather?zip=97132,us&APPID=c3259b476fba8880191b6e087f87f2e9";
                var request = new XMLHttpRequest();
                request.open("GET", requestURL);
                request.responseType = "json";
                request.send();
                request.onreadystatechange = function () {
                    var jsonObj = request.response;
                    document.getElementById("lon").innerHTML = jsonObj.coord.lon;
                    document.getElementById("lat").innerHTML = jsonObj.coord.lat;
                }
            }
        </script>

        <br><a id="newaccount" href="https://johnson-robert.github.io/cit261/index.html">Click me and go Home!</a>
    </body>
</html>