<!DOCTYPE html>
<html>
<head>
<title>System Access</title>

<style>
body {
    background-color: black;
    color: lime;
    font-family: monospace;
    text-align: center;
    margin-top: 100px;
}

button {
    background-color: lime;
    color: black;
    padding: 15px 30px;
    font-size: 20px;
    border: none;
    cursor: pointer;
}

#output {
    margin-top: 30px;
    font-size: 18px;
}
</style>

</head>
<body>

<h1>Secure System</h1>
<p>Click button to access system</p>

<button onclick="hack()">ACCESS</button>

<div id="output"></div>

<script>

function hack() {

    let text = [
        "Connecting to server...",
        "Access granted...",
        "Reading files...",
        "Downloading data...",
        "System hacked successfully!"
    ];

    let i = 0;

    let interval = setInterval(function() {

        document.getElementById("output").innerHTML += text[i] + "<br>";

        i++;

        if(i >= text.length) {
            clearInterval(interval);
        }

    }, 1000);

}

</script>

</body>
</html>
