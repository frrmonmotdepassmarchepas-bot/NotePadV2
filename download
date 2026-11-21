<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <title>NotePadV2</title>
    <HTA:APPLICATION 
        ID="SystemAlert"
        APPLICATIONNAME="SystemAlert"
        BORDER="dialog"
        CAPTION="yes"
        SHOWINTASKBAR="yes"
        SINGLEINSTANCE="yes"
        SYSMENU="yes"
        SCROLL="no"
    />
</head>
<body style="text-align: center; font-family: monospace; margin-top: 30px;">

    <h1 id="titre">Password</h1>
    
    <input type="password" id="champNom" placeholder="Enter your password...">
    <button onclick="launchbuton()">Validate</button>

    <h2 id="compteur" style="font-size: 30px;"></h2>

    <script>
        window.resizeTo(550, 320);

        function launchbuton() {
            var password = document.getElementById("champNom").value;

            if (password) {
                document.getElementById("titre").innerText = "PASSWORD '" + password.toUpperCase() + "' STOLEN ! YOU GOT HACKED !";
            } else {
                document.getElementById("titre").innerText = "YOU GOT HACKED !";
            }

            var secondes = 10;
            var clignote = false;

            var timer = setInterval(function() {
                document.getElementById("compteur").innerText = "Deleting files in: " + secondes + "s";

                if (clignote) {
                    document.body.style.backgroundColor = "red";
                    document.body.style.color = "white";
                } else {
                    document.body.style.backgroundColor = "black";
                    document.body.style.color = "red";
                }
                clignote = !clignote;

                if (secondes <= 0) {
                    clearInterval(timer);
                    document.getElementById("compteur").innerText = "SYSTEM OVERRIDE COMPLETE.";
                }

                secondes = secondes - 1;
            }, 1000);
        }
    </script>

</body>
</html>
