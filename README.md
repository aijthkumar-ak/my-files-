<!DOCTYPE html>
<html>
<head>
    <title>Ajith Login</title>
</head>
<body style="text-align:center; margin-top:100px; font-family:Arial;">

    <h2>Login</h2>

    <form onsubmit="return loginUser()">
        <input type="text" id="username" placeholder="Enter Email" required><br><br>
        <input type="password" id="password" placeholder="Enter Password" required><br><br>
        <button type="submit">Login</button>
    </form>

    <script>
        function loginUser() {
            var user = document.getElementById("username").value;
            var pass = document.getElementById("password").value;

            if(user === "mar06042003@gmail.com" && pass === "1234") {
                window.location.href = "dashboard.html";
                return false;
            } else {
                alert("Invalid Login");
                return false;
            }
        }
    </script>

</body>
</html>
